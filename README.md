# Motoko SvelteKit Starter

A minimal, ready-to-customize starter template for building decentralized applications (dApps) on the Internet Computer using Motoko and SvelteKit.

## Features

- Pre-configured backend-to-frontend communication
- Motoko canister backend
- SvelteKit frontend with SCSS support
- Local development environment
- Candid interface generation
- Hot reload for frontend development

## Quick Start

```bash
# Clone this repository
git clone https://github.com/Quantum-Leap-Labs-Inc/motoko-sveltekit-starter.git
cd motoko-sveltekit-starter

# Install dependencies
npm install

# Start the local replica
dfx start --background

# Deploy your canisters
dfx deploy
```

Once deployed, your application will be available at:
- `http://localhost:4943?canisterId={asset_canister_id}`

## Development Workflow

### Backend Development (Motoko)

The main backend code is in `src/backend/main.mo`. This file contains your canister code written in Motoko.

Example of the default greeting function:
```motoko
actor {
  public query func greet(name : Text) : async Text {
    return "Hello, " # name # "!";
  };
};
```

After making changes to your backend:

```bash

# Redeploy your canisters
dfx deploy
```

### Frontend Development (SvelteKit)

The frontend code is in the `src/frontend` directory. The main page is in `src/frontend/routes/+page.svelte`.

To start the frontend development server with hot reloading:

```bash
npm start
```

This will start a server at `http://localhost:4943`, proxying API requests to the replica at port 4943.

## Resources

- [Internet Computer Documentation](https://internetcomputer.org/docs/current/)
- [Motoko](https://internetcomputer.org/docs/current/motoko/main/motoko)
- [SvelteKit Documentation](https://kit.svelte.dev/docs)
- [DFINITY Examples Repository](https://github.com/dfinity/examples)

