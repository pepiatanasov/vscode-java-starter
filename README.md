# VS Code Java Backend Platform Starter

This repository provides a ready-to-use Visual Studio Code configuration for Java backend projects using Gradle and Spring Boot.

## Features

- **Pre-configured launch settings** for running and debugging Java applications and tests.
- **Custom tasks** for building, assembling, formatting, linting, and testing your project with Gradle.
- **Support for environment-specific builds** using `.env.test` and `.env.prod`.
- **Java-specific settings** for improved code analysis and productivity.

## Included Files

- `.vscode/launch.json`  
  Launch and debug configurations for your Java application and tests.

- `.vscode/tasks.json`  
  Custom build, test, format, lint, and dependency update tasks using Gradle and environment variables.

- `.vscode/settings.json`  
  Java language and analysis settings for VS Code.

## Usage

1. **Clone this repository or copy the `.vscode` folder into your Java project.**

2. **Open your project in VS Code.**

3. **Install recommended extensions:**
   - [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
   - [Gradle for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-gradle)

4. **Configure environment variables as needed:**
   - Place your development/test environment variables in a `.env.test` file at the project root.
   - For production builds, use a `.env.prod` file.
   - Lines starting with `#` are ignored as comments.
   - **Do NOT store production secrets in `.env.test`.**
   - You can duplicate tasks for other environments (e.g., `.env.dev`, `.env.staging`) if needed.

5. **Use the VS Code Run & Debug panel** to start or debug your application, or run tasks from the Command Palette (`Cmd+Shift+P` → `Tasks: Run Task`).

## Example Tasks

- **Assemble Project (No Tests):**  
  Compiles your project without running tests.

- **Build: Run Build with all tests:**  
  Runs a full Gradle build with tests using `.env.test`.

- **Build: Production Env Example:**  
  Runs a full Gradle build with production environment variables from `.env.prod`.

- **Clean Project:**  
  Cleans build artifacts.

- **Check: Run All Checks:**  
  Runs all verification tasks (tests, lint, etc.).

- **Format: Apply Code Formatter:**  
  Applies code formatting using Spotless (if configured).

- **Lint: Run Static Analysis:**  
  Runs static code analysis (if configured).

- **Test: Debug All Tests / Unit / Integration / Feature Services:**  
  Runs tests in debug mode for all, unit, integration, or feature service tests.

- **Test: Debug Single Test Class:**  
  Debug a single test class (edit class name as needed).

- **Test: Run All Tests:**  
  Runs all tests without debugger.

- **Dependency Updates:**  
  Checks for dependency updates (requires [Gradle Versions Plugin](https://github.com/ben-manes/gradle-versions-plugin)).

## Customization

- Edit `launch.json` to change main class, VM arguments, or environment variables.
- Edit `tasks.json` to add or modify Gradle tasks for your workflow.
- Edit `settings.json` for Java language preferences.

## Roadmap

- [ ] Add a sample Java backend app to demonstrate usage of this starter kit
- [ ] Add GitHub Actions workflow for building and testing the sample Java app
- [ ] (other planned features...)

## Notes

- The `.env.test` and `.env.prod` files are not included in this repository.  
  Create them at your project root as needed.
- For the `dependencyUpdates` task, ensure the [Gradle Versions Plugin](https://github.com/ben-manes/gradle-versions-plugin) is applied in your `build.gradle`.

## License

MIT License

---

**Happy coding!**
