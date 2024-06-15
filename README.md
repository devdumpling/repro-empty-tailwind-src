# Reproduction create next-app@rc --empty

Steps to reproduce:

```bash
npx create-next-app@rc --empty
```

Follow prompts to use `src` and `tailwind`. 

Observe that scaffolded `tailwind.config.ts` has the following:

```ts
import type { Config } from "tailwindcss";

const config: Config = {
  content: ["./app/**/*.{ts,tsx,mdx}"],
  theme: {},
  plugins: [],
};
export default config;
```

Expected behavior:

- `content` should be `["./src/**/*.{ts,tsx,mdx}"]`
