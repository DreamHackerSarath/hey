# hey
hey dapp for social 
Requirements
To start working with the Hey monorepo, ensure the following tools are installed:

Node.js (v22 or higher) - the JavaScript runtime used in this project.
pnpm - the package manager used throughout this repository.
Postgres App - the Postgres database used in development.
Installation
This repository uses pnpm workspaces to manage multiple packages within a monorepo structure.

Clone the Repository
git clone git@github.com:bigint/hey.git
Install NVM and pnpm
On macOS, you can install both with Homebrew:

brew install nvm pnpm
Install Node.js
Use nvm to install the required Node.js version:

nvm install
Install Dependencies
From the repository root, install dependencies with pnpm:

pnpm install
Set up Environment Variables
Copy the .env.example file to .env for each package or application that requires configuration:

cp .env.example .env
Repeat this process for all relevant packages and applications in the monorepo.

Environment Variables
The example environment files define the following variables:

API (apps/api/.env.example)
PRIVATE_KEY - Private key used to sign Lens requests.
SHARED_SECRET - Token for internal API authorization.
Start the Development Server
To run the application in development mode:

pnpm dev
Build
Build the application
Compile the application:

pnpm build
Type-check the project
Validate the codebase with the TypeScript type checker:

pnpm typecheck
Lint and Format Code
Check code quality and formatting with Biome:

pnpm biome:check
Automatically fix linting and formatting issues:

pnpm biome:fix
Maintenance Scripts
Convenient Node.js helpers are in the script directory:

node script/clean.mjs removes all node_modules, .next directories, pnpm-lock.yaml, and tsconfig.tsbuildinfo files.
node script/update-dependencies.mjs updates packages across the monorepo, removes old installs and commits the changes in a new branch.
node script/sort-package-json.mjs sorts all package.json files in the repository.
License
This project is released under the GNU AGPL-3.0 license. See the LICENSE file for details
