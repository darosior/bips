```
  BIP: ?
  Layer: API/RPC
  Title: getblocktemplate Updates for Consensus Cleanup
  Author: Antoine Poinsot <mail@antoinep.com>
  Comments-Summary: No comments yet.
  Comments-URI: https://github.com/bitcoin/bips/wiki/Comments:BIP-?
  Status: Draft
  Type: Standards Track
  Created: ?
  License: CC0-1.0
```

## Abstract

This BIP describes modifications to the `getblocktemplate` JSON-RPC call ([bip-0022][BIP22]) to
support the Consensus Cleanup as defined by bip-?.

## Motivation

The Consensus Cleanup constrains some fields of a block's coinbase transaction. Update the
`getblocktemplate` specifications to also convey these values.

## Specification

### Block Template

The template Object is revised to include two new keys:

Key              | Required | Type   | Description                                           |
-----------------|----------|--------|-------------------------------------------------------|
coinbaselocktime | No       | Number | `nLockTime` value to use for the coinbase transaction |
coinbasesequence | No       | Number | `nSequence` value to use for the coinbase transaction |

## Copyright

This document is licensed under the Creative Commons CC0 1.0 Universal license.

[BIP22]: https://github.com/bitcoin/bips/blob/master/bip-0022.mediawiki
