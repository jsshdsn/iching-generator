# Solana I Ching Hexagram Generator

This project implements an on-chain I Ching hexagram generator on the Solana blockchain. It uses Rust for the smart contract and integrates with a Verifiable Random Function (VRF) for secure randomness.

## Project Overview

The I Ching (Book of Changes) is an ancient Chinese divination text. This project brings this traditional practice to the blockchain, ensuring:

- True randomness through VRF
- Immutable record of readings
- Decentralized operation

## Project Structure

- `program/` - Contains the Rust code for the Solana program
- `app/` - Contains the frontend web application
- `scripts/` - Contains deployment and testing scripts

## How It Works

1. The Solana program (smart contract) is written in Rust using the Anchor framework
2. The program uses a VRF (Verifiable Random Function) to generate secure random numbers
3. These random numbers are used to create I Ching hexagrams
4. Users can request a new hexagram through the web interface
5. The program stores the generated hexagrams on-chain, making them immutable and verifiable

## Technical Details

- The program uses Switchboard's VRF for secure randomness
- Hexagram data is stored on-chain in a Solana account
- The frontend interacts with the program using the Solana web3.js library

## Development

### Prerequisites

- Rust and Cargo
- Solana CLI tools
- Node.js and npm
- Anchor framework

### Setup

1. Clone the repository
```bash
git clone https://github.com/jsshdsn/solana-iching-generator.git
cd solana-iching-generator
```

2. Install dependencies
```bash
npm install
```

3. Build the Solana program
```bash
cd program
anchor build
```

4. Deploy to a Solana cluster (devnet for testing)
```bash
anchor deploy --provider.cluster devnet
```

5. Run the frontend
```bash
npm run dev
```

## Future Enhancements

- Add changing lines interpretation
- Implement token-gated access
- Create an NFT for each reading
- Add historical reading storage and retrieval

## License

MIT

## Author

[jsshdsn](https://github.com/jsshdsn)
