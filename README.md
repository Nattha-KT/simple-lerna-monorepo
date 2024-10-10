
# Simple Lerna Monorepo

This repository is a case study project that demonstrates how to structure a monorepo using Lerna and Yarn Workspaces, along with TypeScript. It also includes a simple Node.js/Express API. This project showcases how to efficiently manage multiple packages under one repository while leveraging the strengths of modern development tools.

## Key Features

- **Monorepo Management with Lerna**: Lerna simplifies the management and orchestration of multiple packages in a monorepo.
- **Yarn Workspaces**: Provides fast, minimal, and consistent dependency management, optimizing how packages are installed and shared across the repository.
- **TypeScript Integration**: Ensures strong typing and improves development efficiency.
- **Node.js and Express.js**: A simple API is built with Express to demonstrate how backend services can be part of the monorepo.

## Lerna and Yarn Workspaces: A Seamless Collaboration

This project leverages both **Lerna** and **Yarn Workspaces** to create a well-structured monorepo:

### **Lerna**:
Lerna is responsible for organizing and managing multiple packages within the repository. It automates the process of bootstrapping, linking, and managing versions across packages, enabling a clean and efficient workflow.

Key benefits of using Lerna in this project:
- **Automatic linking** of dependencies between packages.
- **Efficient version control** and release process management.
- **Optimized script running** across all packages, ensuring tasks like building or testing can be run on specific or all packages.

### **Yarn Workspaces**:
Yarn Workspaces, on the other hand, is used to manage dependencies in a way that avoids duplication. It ensures that shared dependencies between packages are installed only once, improving both speed and disk space efficiency.

Key benefits of Yarn Workspaces:
- **Single installation of shared dependencies**, which reduces node_modules size.
- **Smooth integration** with Lerna for dependency management across multiple packages.
- **Centralized workspace management**, allowing all packages to be handled as part of a single repository.

Together, **Lerna** and **Yarn Workspaces** enable a streamlined workflow. Lerna handles the orchestration of packages, while Yarn Workspaces ensures that dependencies are efficiently managed without redundancy, making the combination a powerful tool for large-scale or multi-package projects.

## Project Structure

The project is organized into the following packages:

- `/packages/node-server`: A Node.js/Express API service.
- `/packages/react-app`: React Application for rendering.
<!-- - `/packages/shared-utils`: A utility library that can be shared across other packages. -->

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18.10 or later)
- [Express](https://expressjs.com/) (v4.21 or later)
- [Yarn](https://yarnpkg.com/) (v1.22 or later)
- [Lerna](https://lerna.js.org/) (v5 or later)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Nattha-KT/simple-lerna-monorepo.git
   cd simple-lerna-monorepo
   ```

2. Install dependencies using Yarn:

   ```bash
   yarn install
   ```
`Notice: ` Adjust the version of typescript in each module to be consistent.

### How to add dependencies in workspace root
   ```bash
   yarn add lodash -W
   ```
The `-W` flag (which stands for "workspace root") adds the dependency to the root `package.json` of your monorepo.

`practical fact: ` Lodash is a popular JavaScript utility library that provides a wide range of helpful functions for working with arrays, objects, strings, numbers, and more

### Running the Project

To start the Express.js API:

```bash
yarn workspace @packages/react-app start
```

The API will run on `http://localhost:3000`.

### Scripts

- `yarn build`: Build all packages in the monorepo.
- `yarn test`: Run tests for all packages.
- `yarn start`: Start the Express.js API.

## Learnings and Takeaways

This project serves as a learning tool for setting up a monorepo with Lerna and Yarn Workspaces. The integration of these tools provides a robust solution for managing multiple packages in a single repository, improving developer experience and reducing duplication of dependencies.

## Future Enhancements

- Add more utility packages to extend functionality.
- Implement automated CI/CD for monorepo management.
- Add more comprehensive tests and improve code coverage.

## License

This project is licensed under the MIT License.

---
