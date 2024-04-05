# GraphQL Integration with Etherscan APIs

## Getting Started

To begin utilizing the GraphQL Etherscan API, adhere to the following steps:

Clone the repository containing the GraphQL Etherscan API.
Execute npm install to install essential dependencies.
Generate an API key from Etherscan (detailed below).
Initiate the Apollo server (instructions provided below).
Execute GraphQL queries against the server (refer to the example provided).

## Advantages of GraphQL API
The GraphQL API offers several advantages when interfacing with Etherscan REST APIs:

- Enables querying of multiple interconnected resources in a single API call.
- Incorporates a robust typing system for enhanced data integrity.
- Utilizes an intuitive query language for seamless data retrieval.
- Provides built-in documentation for ease of understanding and implementation.
  
## Generating an Etherscan API Key

In order to access the Etherscan APIs, it is necessary to acquire an API key. Follow these steps:

1. Register for an account on Etherscan via https://etherscan.io/register.
2. Navigate to https://etherscan.io/myapikey to generate your unique API key.
3. Store the generated API key in a .env file under the variable ETHERSCAN_API=your_api_key.

## Overview of GraphQL Etherscan API endpoints

The GraphQL API encompasses the following Etherscan REST endpoints:

- `etherBalanceByAddress` - Retrieves the ETH balance for a specified address.
- `totalSupplyOfEther`    - Retrieves the total supply of ETH.
- `latestEthereumPrice`   - Fetches the latest ETH price.
- `blockConfirmationTime` - Provides an estimation of block confirmation time.

Refer to the schema.graphql file for comprehensive details.

## Running the Apollo Server

To launch the Apollo GraphQL Server:

1. Access your terminal within VSCode.
2. Execute the following command to initiate the server: node index.js.
3. Upon successful startup, a confirmation message will be displayed: 🚀 Server ready at http://localhost:9000/.
4. Access the Apollo Server by navigating to http://localhost:9000 in your web browser.

## Sample GraphQL Query

Below exemplifies a GraphQL query designed to retrieve pertinent data from Etherscan:

```graphql
query {
  etherBalanceByAddress {
    message
    result
  }
  totalSupplyOfEther {
    message
    result
  }
  latestEthereumPrice {
    message
    result {
      ethbtc
      ethusd
      ethusd_timestamp
    }
  }
  blockConfirmationTime {
    message
    result
  }
}
```

