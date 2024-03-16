**@cross - Cross-Runtime JavaScript Libraries**

*Filling the gaps of @std/ on jsr.io* - [https://jsr.io/@cross](https://jsr.io/@cross)

We develop essential cross-runtime libraries for Deno, Bun, and Node.js, extending the foundation of @std on JSR.io.  Our libraries are designed for seamless cross-platform development, offering intuitive APIs and clear documentation.

* **@cross/env:** Simple and consistent environment variable management across runtimes.
* **@cross/runtime:** Easily detect the current JavaScript runtime (Deno, Bun, Node.js, or browser) and its version.
* **@cross/test:** A truly cross-runtime minimal testing framework in collaboration with @std/assert.
* **@cross/deepmerge** Deeply merge objects with flexibility and customizability across JavaScript environments.
* **@cross/base64:** Efficient base64/base64url encoding, decoding, and validation for multiple runtimes.
* **@cross/utils:** A toolbox of helpful cross-runtime utility functions.

**Quick Examples**

**@cross/env**

```typescript
import { get } from '@cross/env';

const port = get('PORT') || '3000';
console.log(`Server listening on port ${port}`);
```

**@cross/runtime**

```typescript
import { CurrentRuntime } from '@cross/runtime';

if (CurrentRuntime === 'deno') {
  console.log("You're running Deno!");
}
```

**@cross/utils**

```typescript
import { args, Colors } from '@cross/utils';

console.log(Colors.bgGreen(Colors.bold('Success!')))

const commandLineArgs = args();
console.log(commandLineArgs);
```

**Get Involved**

We welcome contributions! Here's how:

* **Raise an issue:** Report bugs or suggest new features.
* **Submit a pull request:**  Directly improve our code.
* **Join our community:**  Discussions are open for questions and collaborations. (Consider adding a link if you have a Discord, Slack, etc)

**License**

MIT License (See each libraries LICENSE file for details)
