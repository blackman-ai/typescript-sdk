# @blackman-ai/sdk

Official TypeScript/JavaScript SDK for [Blackman AI](https://www.useblackman.ai) - The AI API proxy that optimizes token usage to reduce costs.

## Features

- 🚀 Drop-in replacement for OpenAI, Anthropic, and other LLM APIs
- 💰 Automatic token optimization (save 20-40% on costs)
- 📊 Built-in analytics and cost tracking
- 🔒 Enterprise-grade security with SSO support
- ⚡ Low latency overhead (<50ms)
- 🎯 Semantic caching for repeated queries

## Installation

```bash
npm install @blackman-ai/sdk
```

## Quick Start

```typescript
import { Configuration, CompletionsApi } from '@blackman-ai/sdk';

const config = new Configuration({
  basePath: 'https://api.useblackman.ai',
  accessToken: 'sk_your_blackman_api_key'  // Get from https://app.useblackman.ai
});

const api = new CompletionsApi(config);

const response = await api.completions({
  provider: 'OpenAI',
  model: 'gpt-4o',
  messages: [
    { role: 'user', content: 'Explain quantum computing in simple terms' }
  ]
});

console.log(response.choices[0].message.content);
console.log(`Tokens saved: ${response.usage.prompt_tokens}`);
```

## Authentication

Get your API key from the [Blackman AI Dashboard](https://app.useblackman.ai/settings/api-keys).

## Documentation

- [Full API Reference](https://docs.useblackman.ai/api-reference)
- [Getting Started Guide](https://docs.useblackman.ai/getting-started)
- [TypeScript Examples](https://github.com/blackman-ai/typescript-sdk/tree/main/examples)
- [Migration from OpenAI](https://docs.useblackman.ai/migration/openai)

## Support

- 📧 Email: [support@blackman.ai](mailto:support@blackman.ai)
- 💬 Discord: [Join our community](https://discord.gg/blackman-ai)
- 🐛 Issues: [GitHub Issues](https://github.com/blackman-ai/typescript-sdk/issues)

## License

MIT © Blackman AI
