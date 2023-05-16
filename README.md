# **TypeScript Node Setup**

This repository provides a ready-to-use TypeScript Node.js setup, allowing developers to quickly start their projects without the need for extensive setup. By cloning this repository, developers will have a preconfigured environment with scripts that handle the compilation and execution of TypeScript code.

## **Getting Started**

To get started with this TypeScript Node setup, follow these steps:

1. Clone the repository to your local machine:

   ```
   git clone https://github.com/your-username/your-repo.git
   ```

2. Navigate to the project's root directory:

   ```
   cd your-repo
   ```

3. Install the required dependencies:
   ```
   npm install
   ```
4. Build the TypeScript code:
   ```
   npm run build
   ```
   This command compiles the TypeScript code located in the src folder and generates JavaScript files in the dist folder.
5. Start the application:
   ```
   npm start
   ```

Alternatively, if you want to enable development mode, which includes automatic recompilation upon file changes, use the following command instead:

```
npm run dev
```

This command runs the TypeScript compiler in watch mode (`-w` flag) and starts the application using Nodemon. Any changes made to the TypeScript files in the `src` folder will trigger an automatic recompilation and restart of the application.

## **Project Structure**

The project follows a specific structure:

- The TypeScript source code resides in the `src` folder.
- After compiling the TypeScript code, the resulting JavaScript - files are stored in the `dist` folder.
- The main entry point of the application is `dist/index.js`.

## **Available Scripts**

This setup includes the following scripts in the `package.json` file:

- build: Removes the dist folder and compiles the TypeScript code using npx tsc.
- prestart: Executes the build script before starting the application.
- start: Runs the compiled JavaScript code in dist/index.js.
- predev: Executes the build script before running the development mode.
- dev: Uses concurrently to simultaneously run the TypeScript compiler in watch mode (npx tsc -w) and Nodemon (nodemon dist/index.js).

Feel free to customize or expand these scripts to fit your project's specific requirements.
