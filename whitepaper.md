# RCoinX

A decentralized peer-to-peer cryptocurrency.

## Table of Contents

1. Basic Coin Information
2. Anonymous Messaging Protocol

## 1. Basic Coin Information

RCoinX is a cryptonote-based coin. This means it uses the CryptoNight hashing algorithm and has strong privacy and anonymity features.

RCoinX is limited to 100 kilobytes (100,000 bytes) for transaction sizes. It has an expected block time of 10 seconds and miners' rewards are "unlocked" instantly.

RCoinX will never have master nodes.

## 2. Anonymous Messaging Protocol

### Introduction

RCoinX's anonymous messaging system uses payment ids as a carrier for messages.

### Format

```
packed struct MessageFragment {
	magic = 0xFEFE,
	id = (integer between 0 and 65535),
	seq = (integer between 0 and 255),
	message = (string),
	padding = (null bytes added to make the message 27 bytes long)
} // 32 bytes
```

The "magic" is a magic number that identifies a message fragment. The id is the message's id and seq is the sequence number of a fragment.
Because all payment ids must be ONLY 32 bytes, messages are fragmented when being sent. All messages are reassembled by the receiver using the seq number in each fragment.

Messages may have headers: only one is currently defined: "Subject"
The subject header must be on the first line and contains the message subject.

There is no way to identify who sent a message.

### Notes

Only TkWallet3X supports the anonymous messages.
