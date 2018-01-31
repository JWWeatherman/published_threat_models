# Conributing To Threat Models

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Page Layout](#page-layout)
  - [Threat Model Sections](#threat-model-sections)
    - [1. Heading Page Section](#1-heading-page-section)
    - [2. Introduction Section](#2-introduction-section)
    - [3. Body Section](#3-body-section)
- [Heading Information](#heading-information)
- [Deploying Changes](#deploying-changes)
  - [1. Push updated Markdown](#1-push-updated-markdown)
  - [2. Create Config and Add it](#2-create-config-and-add-it)
  - [3. Update server](#3-update-server)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Page Layout

### Threat Model Sections

> There are 3 required sections to the threat model 
>
> 1) Heading page
> 2) Introduction
> 3) Body 
>
>Sections are divided by `---` located at the bottom of sections 1 and 2

#### 1. Heading Page Section

> First page of the document.

         ![alt text](http://res.cloudinary.com/loristeeth/image/upload/c_scale,w_800/v1510175135/tm_big_logo_wxtnbt.png "Bitcoin code vortex")
       
         # Bitcoin Threat Model
        
         ### A security review of the Bitcoin cryptocurrency
        
         ---
> * Requirements
>    * A single image
>    * A single H1 (Title)
>    * A single H4 (Description)
>    * Do not add anything else to this section
    
#### 2. Introduction Section

Everything between the heading page and the table of contents.

    # Motivation
    
    The Bitcoin threat model is intended to help developers, investors and users better understand the security of Bitcoin. Threats are assumed to be any activity designed to prevent Bitcoin from accomplishing its mission to become cash (including a unit of account). Under each threat is a description of the threat, the safety features designed to protect against the threat, and any past examples of attacks executing the threat. Bitcoin can be attacked directly by making the software behave in a way that is ineffective as cash or by attacking the humans that are needed to support the software.
    
    # Conclusion
    
    Currently there are no threats that have been identified that could prevent or significantly slow adoption of Bitcoin as cash. However, new threats could be discovered or existing threats may prove to be more impactful. Given the impact Bitcoin is likely to have, and the frequency and intensity of past attacks, this remains a real possibility.
    
    # Introduction
    
    The Bitcoin threat model is intend to help developers, investors and users better understand the security of Bitcoin. Threats are assumed to be any activity designed to prevent Bitcoin from accomplishing its mission to become cash (including a unit of account).
    
    Under each threat is a description of the threat, the safety features designed to protect against the threat, and any past examples of attacks executing the threat. Bitcoin can be attacked directly by making the software behave in a way that is ineffective as cash or by attacking the humans that are needed to support the software.
    
    Threats are categorized as one of the following:
    
    * **Prevent Adoption** - These threats have a reasonable chance of preventing Bitcoin from being adopted as cash.
    * **Significantly Slow Adoption** - These threats have a reasonable chance of significantly slowing the adoption of Bitcoin as cash.
    * **No Impact on Adoption** - These threats do not have a reasonable chance of significantly slowing the adoption of Bitcoin as cash.
    
    Currently there are no threats that have been identified that could prevent or significantly slow adoption of Bitcoin as cash. However, new threats could be discovered or existing threats may prove to be more impactful. Given the impact Bitcoin is likely to have, and the frequency and intensity of past attacks, this remains a real possibility.
    ___

 > * Requirements
 >   * Must contain at least one H1 
 >   * Rest is up to you
 
 #### 3. Body Section
 
    # Software Threats
    Software threats are threats that take advantage of security flaws within the software to prevent Bitcoin from becoming cash.
    
    ## Creating a transaction
    Owners of Bitcoin can send their Bitcoin to another user by creating a digitally signed transaction and broadcasting it to the Bitcoin network. The piece of software that creates transactions is called a "wallet." For a transaction to be accepted by the network it must be digitally signed using the owners private key. Keeping the private keys secret is also handled by the Bitcoin wallet software.
    
    ### An attacker could steal a users private keys to steal their bitcoin.
    If an attacker can gain access to a users private key he can send the associated bitcoin to himself.
    
    **Safety Features**
    * Because each Bitcoin user maintains his own private keys an attacker can only steal from one person at a time. This greatly reduces the incentive for a attacker because in most centralized systems such as banks, credit reporting agencies and brokerages a successful attack could result in access to the funds of thousands of users.
    
    * As long as thefts of private keys is not systemic it will not prevent the adoption of Bitcoin as cash. This is especially true as long as theft of private keys remains more difficult than the theft government money.
    
    * Hardware wallets are gaining in popularity and they make theft of private keys nearly impossible without physical access to the device and password or pin number. This is a level of security that is far higher than is common in banking.
    
    **Past Attacks**
    * Bitcoin owner has private keys stolen in 2011 when keeping private keys safe was much harder,
    https://bitcointalk.org/index.php?topic=16457.msg214423#msg214423
    * Bitcoin owners give away their private keys on Sheep (that is the name of the service,
    https://www.theverge.com/2013/12/2/5167670/sheep-marketplace-bitcoin-heist-nets-at-least-5-million-owners-blamed
    * Bitcoin owners give away their private keys on MtGox, https://www.wired.com/2014/03/bitcoin-exchange/
    
    **No Impact on Adoption**
    * Although users need to be careful to keep their private keys safe, Bitcoin remains the most secure digital asset.
    
    ### An attacker could use a quantum computer to guess everyone's private keys.
    If an attacker could gain access to everyone's private keys he could steal every bitcoin.
    
    **Safety Features**
    * The private key is so large that it would take more energy than is produced by the sun in its entire lifetime to power a computer capable of guessing it.
    
    **Past Attacks**
    * There have been no known attempts to perform this attack.
    
    **No Impact on Adoption**
    * This attack is probably impossible. It is very unlikely that quantum computing or any other field of scientific research will result in such a drastic rewriting of our understanding of the basic laws of physics that guessing private keys would become possible.
   

> * Requirements
>   * Must contain at least one H1 
>   * No need to divide the rest of this document, the renderer will handle it for you.

## Heading Information

The table of contents will only render H tags, therefor there are some restrictions for how deep H tags should go. To remedy
this use the following syntax. 

> * Use only `#<heading>` threw `####<heading>` for heading tags
> * Use `**<Heading>**` for lesser headings 

## Deploying Changes

> There are 3 steps for deploying changes
> 1) Push updated Markdown up to GitHub
> 2) Create config JSON and add it to published_threat_model repo
> 3) Update server 

### 1. Push updated Markdown 
> * File threat model should be README.md

### 2. Create Config and Add it
    "bitcoinThreatModel": {
        "COMPANY_NAME" : "JW Weatherman",
        "PUBLISH_DATE" : "October 2017",
        "DESCRIPTION" : "A security review of the Bitcoin cryptocurrency",
        "TITLE" : "Bitcoin Threat Model",
        "FAVICON" : "http://res.cloudinary.com/loristeeth/image/upload/v1511128064/Small_btc_logo__y588lv.png",
        "QUOTE" : "No quote",
        "HASHTAGS" : "#bitcoin, #btc, #blockchain, #cryptocurrency, #forex, #crypto, #free",
        "MAIN_IMAGE" : "http://res.cloudinary.com/loristeeth/image/upload/c_scale,w_800/v1510175135/tm_big_logo_wxtnbt.png",
        "REPO_URL" : "https://api.github.com/repos/JWWeatherman/bitcoin_security_threat_model/readme",
        "STYLE" : {
          "heading-page-background-color" : "#fff",
          "heading-page-h1-color" : "#2c3e50",
          "heading-page-h2-color" : "#2c3e50",
          "heading-page-h3-color" : "#f5922f",
          "heading-page-h4-color" : "#2c3e50",
          "heading-page-jumbotron-color" : "#2c3e50",
          "page-background-color" : "#fff",
          "page-color" : "#2c3e50",
          "page-h1-color" : "#f7931a",
          "page-h2-color" : "#5b5b5b",
          "page-h3-color" : "#2c3e50",
          "page-h4-color" : "#2c3e50",
          "page-bold-color" : "#2c3e50",
          "page-page-header-background-color" : "#fff2ce",
          "page-page-header-color" : "#2c3e50",
          "page-page-footer-background-color" : "#fff2ce",
          "page-page-footer-color" : "#f7931a",
          "page-page-footer-resources-color" : "#f7931a"
        }
        
> * Create JSON to look like example above
> * All properties must exist
> * You can leave properties out of STYLE object, any properties not present will be default style (Like Bitcoin Threat Model)
> * STYLE must be included even if empty
> * REPO_URL is the api url NOT the url to the repo. Use this template
>   * `https://api.github.com/repos/JWWeatherman/<REPO NAME>/readme`
> * Add config to [Published Threat Models Repo](https://github.com/JWWeatherman/published_threat_models/blob/master/configs.json)

### 3. Update server
The server stores the config and markdown in order to limit the amount of calls to GitHub api. You must tell the server to get the 
updated information. 

> * Get the url form admin
> * Next do this in terminal 

```
# Don't forget to put quotes around url
curl "<URL FROM ADMIN>" 
```

> * Response will be html templates for main page listings

```
             <div class="row-4 w-row medium-rotate small-rotate tiny-rotate">
              <div class="w-col w-col-2 w-col-medium-8"></div>
               <div class="column-5 w-col w-col-5 w-col-medium-8">
                  <img src="http://res.cloudinary.com/loristeeth/image/upload/c_scale,w_800/v1510175135/tm_big_logo_wxtnbt.png" class="image-2 doc-image">
                </div>
                <div class="w-col w-col-3 w-col-medium-8 description-content">
                  <h4 class="heading tiny-h-font small-h-font medium-h-font">Bitcoin Threat Model</h4>
                  <div class="tiny-font small-font medium-font">October 2017</div>
                  <p class="paragraph-2 tiny-font small-font medium-font">A security review of the Bitcoin cryptocurrency</p>
                  <a href="#/bitcoinThreatModel" class="button tiny-font small-font medium-font">Read Bitcoin Threat Model</a>
                </div>
                <div class="w-col w-col-2"></div>
              </div>
            
              <div class="row-4 w-row medium-rotate small-rotate tiny-rotate">
                <div class="w-col w-col-2 w-col-medium-8"></div>
                <div class="column-5 w-col w-col-5 w-col-medium-8">
                  <img src="http://res.cloudinary.com/doohickey/image/upload/c_scale,w_800/v1514835923/human_vortex_nzhq0b.png" class="image-2 doc-image">
                </div>
                <div class="w-col w-col-3 w-col-medium-8 description-content">
                  <h4 class="heading tiny-h-font small-h-font medium-h-font">Human Threat Model</h4>
                  <div class="tiny-font small-font medium-font">December 2017</div>
                  <p class="paragraph-2 tiny-font small-font medium-font">A security review of Humans</p>
                  <a href="#/humanThreatModel" class="button tiny-font small-font medium-font">Read Human Threat Model</a>
                </div>
                <div class="w-col w-col-2"></div>
              </div>
            
              <div class="row-4 w-row medium-rotate small-rotate tiny-rotate">
                <div class="w-col w-col-2 w-col-medium-8"></div>
                <div class="column-5 w-col w-col-5 w-col-medium-8">
                  <img src="https://user-images.githubusercontent.com/32912678/35408498-5682d3bc-01dd-11e8-8e37-08abbde89976.png" class="image-2 doc-image">
                </div>
                <div class="w-col w-col-3 w-col-medium-8 description-content">
                  <h4 class="heading tiny-h-font small-h-font medium-h-font">Ethereum Threat Model</h4>
                  <div class="tiny-font small-font medium-font">January 2018</div>
                  <p class="paragraph-2 tiny-font small-font medium-font">A security review of the Ethereum cryptocurrency</p>
                  <a href="#/etheruemThreatModel" class="button tiny-font small-font medium-font">Read Ethereum Threat Model</a>
                </div>
                <div class="w-col w-col-2"></div>
              </div>


```