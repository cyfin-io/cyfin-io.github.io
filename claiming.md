---
title: Claiming
layout: default
permalink: /claiming/
---
    
<section class="wrapper style1">
  <div class="container">
    <div class="row">
      <div class="2u"><p></p></div>
      <div class="8u skel-cell-important">

        <div id="content">    
          <article>

<header>
  <h2>Claiming and Spending Crypto-Conditions</h2>
  <p>Making the IoT work for me, and paying the bill.</p>
</header>

<span class="image featured"><img src="{{ site.baseurl }}/assets/images/city.jpg" alt="" /></span>
<p> Whenever an economic relationship begins, the underlying asset and the rules of exchange have to be defined. CyFin proposes crypto-conditions for this negotiation. Two approaches are possible:
  <ul>
    <li>Upon payment, the issuer can create a crypto-condition of a specific value to the paying customer. When the crypto-condition is claimed by the customer the amount stated in the condition is added to his account balance.<br><br></li>
    <li>The issuer can create an open crypto-condition, claimable by anyone. Open conditions can be put as digital downloads into an online store, or behind a payment wall. The Buyer can complete the condition with his account address and claim the balance.</li>
  </ul>
</p>

<h3>An Example of Delivery through Online Store.</h3>

Cosign.io, an oracle service for identity on the ethereum blockchain offers a payed API. Prepaid credit can be purchased in the online store as crypto-conditions:


  <div class="row">
    <section class="4u">
      <iframe style="width:300px;height:360px" src="https://holvi.com/shop/ocolin/product/b64ad1f615f35cefdaae65897c669801/embedded/" frameborder="0"></iframe>
    </section>
    <section class="4u">
      <iframe style="width:300px;height:360px" src="https://holvi.com/shop/ocolin/product/51c9a0789df1ff91f0e0c15a242ca55f/embedded/" frameborder="0"></iframe>
    </section>
    <section class="4u">
      <iframe style="width:300px;height:360px" src="https://holvi.com/shop/ocolin/product/b2dca040c101ff239802a703cfdc8ac5/embedded/" frameborder="0"></iframe>
    </section>
  </div>

<h3>Claiming a Crypto-Condition</h3>

<p>After the purchase, you will receive and email with a crypto-condition, similar to this:</p>

<div markdown="1">

> Dear Sir or Madam, 
> <br>This is your €20 crypto­-condition: 
> 
> cf:37:dDI1NiI6MTAwM...DB9LH
> 
> To claim this condition for...

To claim the condition you need to:

1. [Install and start CyFin-CLI](#).
2. [Load your key-pair in the CyFin-CLI](#). 
3. Claim the crypto-condition.

</div>
<div markdown="1">
Once you are able to display key-pair status information, including the balance, you are ready to claim. Proceed to use the `claim <condition>` command. A successful claim will result in a notice sent to your email and your balance updated.
</div>
<div markdown="1">

```
cyfin$ claim cf:37:dDI1NiI6MTAwM...DB9LH
```
> crypto-condition loaded successfully.
> <br>new account balance: 20.0

```
cyfin$ info
```
> cyfin-id: 0092a8ff
> <br>balance: 20.0
> <br>email: your@email.com

  </div>

          </article>  
        </div>
      </div>
      <div class="2u"><p></p></div>
    </div>
  </div>
</section>