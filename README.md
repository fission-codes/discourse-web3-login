![](https://github.com/fission-suite/PROJECTNAME/raw/master/assets/logo.png?sanitize=true)

# Discourse Web3 Login

A [Discourse forum](https://discourse.org) plugin that enables authentication / login via a Web3 account.

_Note: this is an empty repo, and is where the code for this project will go. Please join our Discord chat for more info._

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/fission-suite/blob/master/LICENSE)
[![Built by FISSION](https://img.shields.io/badge/⌘-Built_by_FISSION-purple.svg)](https://fission.codes)
[![Discord](https://img.shields.io/discord/478735028319158273.svg)](https://discord.gg/zAQBDEq)
[![Discourse](https://img.shields.io/discourse/https/talk.fission.codes/topics)](https://talk.fission.codes)

# Scope

Discourse supports extensibile authentication plugins. The goal is to be able to link a "Web3 account" aka Ethereum account / address / wallet to use it as an authentication mechanism for Discourse.

This will need a web3 JS provider. Since Discourse uses Ember, looks like [ember-ethers](https://www.npmjs.com/package/ember-ethers) is the right thing. Might need updating.

A connection to the blockchain to check signatures or other interactions will get handled by either EtherScan API calls, Infura, or a similar node-as-a-service. Ideally, this is configurable so that people who run forums can choose to run their own nodes. As far as Discourse is concerned, this is like an API call to any other service.

## Present a "Login with Ethereum" button

This should work with most EVM-compatible chains, so it might be configurable to say "Login with X".

## Associate addresses with a Discourse account

For new signups, like with Twitter login, will need to prompt for email address.

Should be able to store the address logged in with in the database as part of the user profile, and optionally disply as a part of the user profile.

# Future

_These are some future / stretch goals_

## WalletConnect

Enable login with [WalletConnect](https://walletconnect.org/), with QR code display. This may also mean [Web3Connect](https://github.com/web3connect/web3connect).

## 3Box integration

Extend this so that profile details -- email address, bio, image, etc. -- can be pulled in from 3Box.
