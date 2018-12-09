    BSIP:       TODO
    Title:      Introduce the only_issuer_limit_orders_allowed flag for assets
    Authors:    Fabian Schuh <https://github.com/xeroc>
                Dmitrij Vinokour <https://github.com/dimfred>
    Status:     Draft
    Type:       Protocol
    Created:    2018-12-09
    Discussion: TODO
    Worker:     <Id of worker proposal>

# Abstract

In terms of an ICO the ICO-holder is offering his tokens. This tokens can
be sold in more rounds, where in each round after a certain time the price
per token is increased. 

Someone who bought tokens in an older round, could start selling them in a
later round by offering them for a price just slightly under the current ICO
price.

To protect the ICO-holder of loosing potential buyers the 'only_issuer_limit_orders_allowed`
is introduced. This means only the creator of the asset would be able to 
create limit orders.

# Motivation

To make the BitShares Blockchain more interesting for ICO-holders, by 
strengthening and extending the possibilities, when it comes to the setup 
of an ICO, is the main focus of this BSIP.

# Rational

TODO

# Specifications

This BSIP comes with only minimal modifications that, however, change
the behavior of the protocol and thus need a protocol upgrade.

The change is implemented in such a way that a `only_issuer_limit_orders_allowed`
flag is added to the `asset_issuer_permission_flags`. When a non asset issuer trys to
create a limit order the `limit_order_create_evaluator` asserts to false and ignores the 
limit order.

An examplary implementation can be found here: 
https://github.com/bitshares/bitshares-core/compare/develop...blockchainprojects:feature/asset-disable-limit-order-create-flag 

# Discussion

TODO

# Summary for Shareholders

This BSIP proposes a way to protect ICO-holders of loosing potential customers
through undercutting of earlier participants in a more round ICO.

# Copyright

This document is placed in the public domain.

# See Also


