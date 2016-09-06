---
layout: default
title: FAQ
permalink: /faq/
---
<section class="wrapper style1">
  <div class="container">
    <div class="row">
      <div class="2u"><p></p></div>
      <div class="8u">
        <div id="content">    
          <article>
            <header>
              <h2>Frequently Asked Questions</h2>
              <p>on key-pairs, crypto-conditions and payment-channels.</p>
            </header>
          <span class="image featured"><img src="{{ site.baseurl }}/assets/images/questions.jpg" alt="" /></span>
<div markdown="1">

## What are key-pairs?

[Public key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) is a system that uses pairs of keys: public keys that may be distributed widely and private keys which are known only to the owner.

Specifically, we use the [ECDSA algorithm](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm) with the secp256k1 curve parameters. This is the same algorithm that is used with [Ethereum](http://ethereum.org) accounts.

## How are key-pairs used with CyFin?

The [getting-started section](/instructions) will take you through the setup of a key-pair.

At CyFin all services are defined by crypto-conditions. Key-pairs, controlled by IoT agents, smart-cards, oracles, and sometimes humans can sign crypto-conditions. Hence, they can initiate and participate in services like issuance, claiming, payment, and metering.

## What are crypto-conditions?

A crypto-condition is a standardized way to describe an event that is expected to happen. Once the event occured, a cryptographically verifyable message, the fulfillment, proves that the event happened. Read more in the [crypto-condition specification](https://interledger.org/five-bells-condition/spec.html){:target="_blank"}.

## What is an example for a crypto-condition?

Take a `transfer` function as an example for a crypto-condition. A ledger managing the € balance of Alice and Bob is able to issue and verify events described by such conditions.

```
transfer(txId, from, to, amount)
```
<br>
Bob wants to offer a payed API. He issues a crypto-condition stating the price of €25 payable by anyone for his service to be used:

```
transfer(*, *, bob, 25) + signature by Bob
```
<br>
Alice could decide to use Bob's service. She fills in the missing parameters and signs, creating a crypto-fullfilment to the previous condition.

```
transfer(1, alice, bob, 25) + signature by Alice
```
<br>
Bob can collect such fulfillments in exchange for the access to his API and periodically submit them to the ledger to claim the total of € payments.

## What are more exciting use-cases for crypto-conditions?

Check the [interledger project](https://interledger.org/) to get an idea of some protocols that can be build with crypto-conditions.

## What are payment-channels?

[Payment-channels](http://raiden.network/) allow users to rapidly exchange crypto-conditions for the transfer of value, as small as fractions of a cent. This allows to effectively monetize APIs and M2M payments.

</div>
          </article>
        </div>
      </div>
      <div class="2u"><p></p></div>
    </div>
  </div>
</section>