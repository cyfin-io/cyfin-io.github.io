---
title: Getting Started
layout: default
permalink: /instructions/
---
    
<section class="wrapper style1">
  <div class="container">
      <div class="row">
      <div class="2u"><p></p></div>
      <div class="8u skel-cell-important">
        <div id="content">    
          <article>
          <header>
            <h2>Getting Started</h2>
            <p>CLI installation, key-pair-management, and key-pair registration.</p>
          </header>
          <span class="image featured"><img src="{{ site.baseurl }}/assets/images/started.jpg" alt="" /></span>
          <p> CyFin has no centralized account system. Rather cryptographic key-pairs and digital signatures are used for all communication. CyFin offers a command-line interface (CyFin-CLI) to simplify the management of key-pairs and the execution of business processes. 
          </p>

          <h2>CyFin-CLI Installation</h2>
          <span class="image"><img src="{{ site.baseurl }}/assets/images/cyfin.png" alt="" /></span>
<div markdown="1">

you should get a print like above with the following steps:

```
$ npm install cyfin-cli
$ cyfin-cli
```
<br><br>

## Key-Pair Management

To create a working setup, you need to execute the following steps:

1. generate a key-pair
2. register the key-pair
3. read the key-pair balance


### Generating a Key-Pair

Install the CyFin-CLI as described, then run the `generate` command. A secret seed for your key-pair will be generated and displayed as mnemonic.

```
cyfin$ generate
```
> Your mnemonic is:
> 
>  `***** ***** ******* ***** ******* **** ******* ****** ****** ****** ******* *****`
> 
> confirm to remove from screen:


Make sure to note the mnemonic. The mnemonic will be removed from the terminal history after you press any key and will be lost after restart of the CLI.


### Register a Key-Pair

Now that you have generated a key-pair in the previous step, continue to register it with this command:

```
cyfin$ register your@email.com
```
> Email verification requested. A crypto-condition will be sent to you.



You will receive an email similar to this one:

>Dear customer, 
>
>We have received a request to authorize this email address for CyFin.io. If you requested this verification, please return the following crypto-condition: 
>
>cf:0:RoFF18igQ7msaEjUKU21zw


Note the line starting with **cf:0:**, this is a crypto-condition. Return it to the CyFin-CLI with the `confirm` command. You should receive status information about your registered key-pair.

```
cyfin$ confirm cf:0:RoFF18igQ7msaEjUKU21zw
```
> cyfin-id: 0092a8ff
> <br>balance: 0.0
> <br>email: your@email.com


As you see, your key-pair starts with a 0.0 balance. You can top-up your balance by [claiming a crypto-condition](#claim-a-crypto-condition).


### Loading a Key-Pair

When restarting the CyFin-CLI, all state is reset. You need to load your key-pair again by using the `load` command. A password-like prompt will ask for a mnemonic or ECDSA hex private key.

```
cyfin$ load
```
> Please enter a mnemonic or hex string to load your key-pair:
> <br>mnemonic/hex: `******************************************`
> 
> key-pair loded successfully.

```
cyfin$ info
```
> cyfin-id: 0092a8ff
> <br>balance: 0.0
> <br>email: your@email.com

Once your keypair is loaded, run the `info` command. If you are able to retrieve your balance, your key-pair setup is complete.


</div>



            </article>  
          </div>
        </div>
        <div class="2u"><p></p></div>
    </div>
  </div>
</section>
