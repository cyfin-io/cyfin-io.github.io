---
title: Getting Started
layout: default
---
    
<section class="wrapper style1">
  <div class="container">
    <div id="content">    
      <article>
        <header>
          <h2>Getting Started</h2>
          <p>CLI installation, key management, and registration.</p>
        </header>
        <span class="image featured"><img src="{{ site.baseurl }}/assets/images/started.jpg" alt="" /></span>

<div markdown="1">

```
                 _               _       
                (_)             (_)      
    ___ ___  ___ _  __ _ _ __    _  ___  
   / __/ _ \/ __| |/ _` | '_ \  | |/ _ \
  | (_| (_) \__ \ | (_| | | | |_| | (_) |
   \___\___/|___/_|\__, |_| |_(_)_|\___/ 
                    __/ |
   An open, secure |___/ identity platform.

type `help`, if you like ;)

cosign$
```

## Installation

you should get a print like above with the following steps:

```
$ npm install cosign-cli
$ cosign-cli
```

After installing cosign-cli, continue to:

* [generate and register a key](#generate-and-register-a-key)
* purchase a voucher from the [shop](https://holvi.com/shop/ocolin/)
* [claim the voucher](#claim-a-voucher)

## Generate and Register a Key

To create a working setup, you need to execute the following steps:

1. generate a key
2. register the key
3. read the key balance


### Generating a Key

Install the cosign-cli as described, then run the `generate` command. A secret seed for your key will be generated and displayed as mnemonic.

```
cosign$ generate
```
> Your mnemonic is:
> 
>  `***** ***** ******* ***** ******* **** ******* ****** ****** ****** ******* *****`
> 
> confirm to remove from screen:


Make sure to note the mnemonic. The mnemonic will be removed from the terminal history after you press a key and will be lost after restart of the CLI.

### Register a Key

Now that you have generated a key in the previous step, continue to register it with this command:

```
cosign$ register your@email.com
```
> Email verification requested. A crypto-fulfillment will be sent to you.



You will receive an email similar to this one:

```
Dear customer, 

We have received a request to authorize this email address for Cosign.io. If you requested this verification, please return the following crypto fulfillment: 

cf:0:RoFF18igQ7msaEjUKU21zw
```

Note the line starting with **cf:0:**. This is a crypto-fulfillment. Return it to the CLI with the `confirm` command. You should receive status information of your registered key.

```
cosign$ confirm cf:0:RoFF18igQ7msaEjUKU21zw
```
> cosign-id: 0092a8ff
> <br>balance: 0.0
> <br>email: your@email.com


As you see, your key starts with a 0.0 balance. You can top-up your balance by [claiming a voucher](#claim-a-voucher).

### Loading a Key

When restarting the CLI, all state is reset. You need to load your key again by using the `load` command. A password-like prompt will ask for a mnemonic or ECDSA hex private key.

```
cosign$ load
```
> Please enter a mnemonic or hex string to load your key:
> <br>mnemonic/hex: `******************************************`
> 
> Key loded successfully.


</div>
        </article>  
    </div>
  </div>
</section>
