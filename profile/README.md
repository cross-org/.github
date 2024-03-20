**@cross - Cross-Runtime JavaScript Libraries**

*Filling the gaps of @std/ on jsr.io* - [https://jsr.io/@cross](https://jsr.io/@cross)

We develop essential cross-runtime libraries for Deno, Bun, and Node.js, extending the foundation of @std on JSR.io.  Our libraries are designed for seamless cross-platform development, offering intuitive APIs and clear documentation.

* **[@cross/utils](https://jsr.io/@cross/utils):** A toolbox of helpful cross-runtime utility functions like `exit()`, `spawn()`, `args`, `ArgumentParser` and more.
* **[@cross/env](https://jsr.io/@cross/env):** Simple and consistent environment variable management across runtimes.
* **[@cross/runtime](https://jsr.io/@cross/runtime):** Easily detect the current JavaScript runtime (Deno, Bun, Node.js, or browser), along with version, OS and more.
* **[@cross/test](https://jsr.io/@cross/test):** Write cross-runtime tests utilizing the build in test runners of Deno, Node and Bun. Works great with @std/assert and Sinon.
* **[@cross/deepmerge](https://jsr.io/@cross/deepmerge):** Deeply merge objects with flexibility and customizability across JavaScript environments.
* **[@cross/base64](https://jsr.io/@cross/base64):** Efficient cross-runtime base64/base64url validation.
* **[@cross/log](https://jsr.io/@cross/log):** Flexible cross-runtime logging with customizable console styling, file output, log levels, and pluggable transports.
* **[@cross/service](https://jsr.io/@cross/service):** Cross-runtime service installer library for Systemd, Upstart, Sysvinit usable in Node, Deno and Bun.
* **[@cross/dir](https://jsr.io/@cross/dir):** Cross-platform mechanism for retrieving the paths to standard user directories in Deno, Bun and Node.js

**Quick Examples**

**@cross/env**

```typescript
import { getEnv } from "@cross/env";

const port = getEnv("PORT") || "3000";
console.log(`Server listening on port ${port}`);
```

**@cross/runtime**

```typescript
import { CurrentRuntime } from "@cross/runtime";

if (CurrentRuntime === "deno") {
  console.log("You're running Deno!");
}
```

**@cross/utils**

```typescript
import { args, Colors } from "@cross/utils";

console.log(Colors.bgGreen(Colors.bold("Success!")))

const commandLineArgs = args();
console.log(commandLineArgs);
```

**Get Involved**

We welcome contributions! Here's how:

* **Raise an issue:** Report bugs or suggest new features.
* **Submit a pull request:**  Directly improve our code.
* **Join our community:**  Discussions are open for questions and collaborations.

**License**

MIT License (See each libraries LICENSE file for details)
