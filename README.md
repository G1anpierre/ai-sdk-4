<a href="https://chat.vercel.ai/">
  <img alt="Next.js 14 and App Router-ready AI chatbot." src="app/(chat)/opengraph-image.png">
  <h1 align="center">Next.js AI Chatbot with Vercel AI SDK 4</h1>
</a>

<p align="center">
  A modern AI chatbot implementation built with Next.js 14 and Vercel AI SDK 4, showcasing advanced AI integration techniques.
</p>

<p align="center">
  <a href="#features"><strong>Features</strong></a> ·
  <a href="#model-providers"><strong>Model Providers</strong></a> ·
  <a href="#custom-implementations"><strong>Custom Implementations</strong></a> ·
  <a href="#deploy-your-own"><strong>Deploy Your Own</strong></a> ·
  <a href="#running-locally"><strong>Running Locally</strong></a> ·
  <a href="#project-structure"><strong>Project Structure</strong></a>
</p>
<br/>

## Features

- **Advanced Next.js Implementation**
  - Next.js 14 App Router architecture
  - React Server Components (RSCs) for improved performance
  - Server Actions for secure server-side operations
  - Optimized routing with parallel routes and intercepting routes
  
- **Vercel AI SDK 4 Integration**
  - Unified API for multiple AI model providers
  - Streaming responses with minimal latency
  - Tool calling capabilities for external integrations
  - Type-safe structured output for predictable AI responses
  
- **Modern UI/UX**
  - Responsive design with Tailwind CSS
  - Accessible components from shadcn/ui
  - Dark/light mode theming
  - Real-time typing indicators
  
- **Advanced Chat Features**
  - Multi-turn conversations with context management
  - File upload and processing capabilities
  - Code highlighting and formatting
  - Markdown rendering with syntax highlighting
  
- **Data Persistence**
  - Vercel Postgres for conversation history
  - Vercel Blob for efficient file storage
  - Secure data handling with proper authorization

- **Authentication & Security**
  - NextAuth.js for multi-provider authentication
  - Rate limiting to prevent abuse
  - Proper token management for API calls

## Model Providers

This implementation supports multiple AI model providers through the Vercel AI SDK:

- **OpenAI** (default): Access to GPT-4o, GPT-4, and other models
- **Anthropic**: Claude 3 Opus, Sonnet, and Haiku models
- **Cohere**: Command and other specialized models
- **Custom Provider Integration**: Framework for adding additional providers

The application is configured to use OpenAI's `gpt-4o` by default, but can be easily switched to any other supported model.

## Custom Implementations

This project includes several customizations beyond the standard Vercel AI Chatbot template:

- **Specialized Agents**: Custom AI agents for specific tasks like data analysis or creative writing
- **Enhanced Prompt Engineering**: Optimized system prompts for better AI responses
- **Memory Management**: Improved context handling for longer conversations
- **Custom Tool Integrations**: Integration with external APIs for expanded capabilities
- **Advanced Error Handling**: Graceful recovery from rate limits and other API issues

## Deploy Your Own

You can deploy your own version of this chatbot to Vercel with one click:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FG1anpierre%2Fai-sdk-4&env=AUTH_SECRET,OPENAI_API_KEY&envDescription=Learn%20more%20about%20how%20to%20get%20the%20API%20Keys%20for%20the%20application&envLink=https%3A%2F%2Fgithub.com%2Fvercel%2Fai-chatbot%2Fblob%2Fmain%2F.env.example&demo-title=Next.js%20AI%20Chatbot&demo-description=An%20Advanced%20AI%20Chatbot%20Built%20With%20Next.js%2014%20and%20Vercel%20AI%20SDK%204&demo-url=https%3A%2F%2Fchat.vercel.ai&stores=[{%22type%22:%22postgres%22},{%22type%22:%22blob%22}])

## Running Locally

You will need to use the environment variables [defined in `.env.example`](.env.example) to run the application. It's recommended you use [Vercel Environment Variables](https://vercel.com/docs/projects/environment-variables) for this, but a `.env` file is all that is necessary.

> Note: You should not commit your `.env` file or it will expose secrets that will allow others to control access to your various OpenAI and authentication provider accounts.

1. Install Vercel CLI: `npm i -g vercel`
2. Link local instance with Vercel and GitHub accounts (creates `.vercel` directory): `vercel link`
3. Download your environment variables: `vercel env pull`

```bash
npm install
npm run dev
```

Your app should now be running on [localhost:3000](http://localhost:3000/).

## Project Structure

```
.
├── app/                   # Next.js App Router pages and layouts
│   ├── (auth)/            # Authentication-related routes
│   ├── (chat)/            # Chat interface and functionality
│   ├── api/               # API routes for backend operations
│   └── ...
├── components/            # Reusable UI components
│   ├── chat/              # Chat-specific components
│   ├── ui/                # General UI components
│   └── ...
├── lib/                   # Utility functions and helpers
│   ├── actions/           # Server actions
│   ├── auth/              # Authentication utilities
│   ├── db/                # Database utilities
│   └── ...
├── public/                # Static assets
└── ...
```

## Further Customization

The core architecture allows for extensive customization:

- **Model Switching**: Easily switch between different AI providers
- **New Tool Creation**: Add custom tools by implementing the tool calling interface
- **UI Customization**: Modify the UI components to match your brand
- **Prompt Engineering**: Refine system prompts for specialized use cases

## License

This project is based on the Vercel AI Chatbot template and maintains the same licensing.

## Acknowledgements

- Vercel team for the AI SDK and chatbot template
- OpenAI and other model providers for their APIs
- The Next.js community for continuous innovation