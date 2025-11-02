**@cross - Cross-Runtime JavaScript Libraries**

*Filling the gaps of @std/ on jsr.io* - [https://jsr.io/@cross](https://jsr.io/@cross)

We develop essential cross-runtime libraries for Deno, Bun, and Node.js, extending the foundation of @std on JSR.io.  Our libraries are designed for seamless cross-platform development, offering intuitive APIs and clear documentation.

* **[@cross/fs](https://github.com/cross-org/fs):** Complete cross-runtime utility library offering functions for file system operations, such as `diskusage()`, `size()`, `readFile()`, `stat()`, `mktempdir()`.
* **[@cross/utils](https://github.com/cross-org/utils):** A toolbox of helpful cross-runtime utility functions like `exit()`, `spawn()`, `args`, `ArgumentParser` and more.
* **[@cross/env](https://github.com/cross-org/env):** Simple and consistent environment variable management across runtimes.
* **[@cross/runtime](https://github.com/cross-org/runtime):** Easily detect the current JavaScript runtime (Deno, Bun, Node.js, or browser), along with version, OS and more.
* **[@cross/test](https://github.com/cross-org/test):** Write cross-runtime tests utilizing the build in test runners of Deno, Node and Bun. Works great with @std/assert and Sinon.
* **[@cross/deepmerge](https://github.com/cross-org/deepmerge):** Deeply merge objects with flexibility and customizability across JavaScript environments.
* **[@cross/base64](https://github.com/cross-org/base64):** Efficient cross-runtime base64/base64url validation.
* **[@cross/log](https://github.com/cross-org/log):** Flexible cross-runtime logging with customizable console styling, file output, log levels, and pluggable transports.
* **[@cross/service](https://github.com/cross-org/service):** Cross-runtime service installer library for Systemd, Upstart, Sysvinit usable in Node, Deno and Bun.
* **[@cross/dir](https://github.com/cross-org/dir):** Cross-platform mechanism for retrieving the paths to standard user directories in Deno, Bun and Node.js
* **[@cross/jwt](https://github.com/cross-org/jwt):** A versatile JSON Web Token (JWT) library.
* **[@cross/kv](https://github.com/cross-org/kv):** A fast, file based Key/Value Database with in-memory index for Node, Deno and Bun.
* **[@cross/workers](https://github.com/cross-org/workers):** Cross-runtime worker pool with TypeScript support
  
**We have also...**

... created a set of common reusable and configurable GitHub workflows to streamline cross-runtime compatibility testing with Deno, Node, and Bun. Find them at [github.com/cross-org/workflows](https://github.com/cross-org/workflows).

**Quick Examples**

**@cross/env**

```typescript
import { getEnv } from "@cross/env";

const port = getEnv("PORT") || "3000";
console.log(`Server listening on port ${port}`);
```

**@cross/log**

```typescript
import { Log } from "@cross/log";

const logger = new Log();

log.log("This is a log");
log.warn("This is a warning");
log.debug("This is not shown by default");
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
