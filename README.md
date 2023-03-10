# loco (name pending)

This document is still very much a work in progress.

## Problem Statement

Geolocation data has a multitude of uses cases from Yelp! reviews and Pokemon Go all the way down to a corporate website's "find a location near you" page. These location services are often either custom made or come by way of API's provided by large coorporations like Google and Bing.  To build your own requires time, money, and expertise, but to rely on corporate API providers subjects you to vendor risk. In a perfect world, the geolocation data and services would exist as an open source protocol that lives on public database with a public API. To make this a reality, we proposed the creation of an EVM smart contact that will allow users to input location data, read it back from the contract, and to search for locations near a given coordinate. Because this is on-chain, other EVM smart contracts will be able to have access to geolocation services without the need for an oracle. 

## ETHGlobal - Scaling Ethereum 2023

This project will be our entry into the ETHGlobal hackathon

## Features

* EVM Smart Contract (hackathong goal)
  *  Deployed to one or many L2s.
  *  Will stored basic fields on chain: id, name, description, latitude, longitude, geohash
  *  Location will be retrievalble directly by id and geohash
  *  Separate indices will allow grouping of locations by level according to geohash length for querying (for example, locations at 9q5ctr9j & 9q5ctr98 would both be returned in a query for locations in 9q5ct
  *  Clients will pay gas to add a new location to the contract
  *  Clients can read data from the contract for free.
* Sample Frontend (hackathon goal)
  * Web3 site using ethers.js to connect directly with the contract
  * Site will allow users to add location data to the contract and pay for gas using Metamask
  * Site will display a map showing locations that it queries from the contract.
* Client EVM Contract (future roadmap)
  * Create another EVM contract that calls the geolocation contract as a proof of concept

We welcome input. If there are any other use cases you can think of that we haven't mention, please create a `use case` issue. If there are features that might be helpful, create a `feature` issue.

Thanks
