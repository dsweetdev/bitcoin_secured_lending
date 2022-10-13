---
title: Bitcoin-Secured Lending

language_tabs:
  - shell: Shell
  - java: Java  
  - csharp: C#
  - javascript--browser: JS  
  - javascript--node: NodeJS
  - php: PHP
  - ruby: Ruby
  - python: Python
  - perl: Perl
  - go: Go
  - swift: Swift


toc_footers:
  - © 2022 Dustin Sweet

includes:
  - APIReference/Lending/authorization.md.erb   
  - APIReference/Lending/programs.md.erb  
  - APIReference/Lending/get_all_programs.md.erb    
  - APIReference/Lending/get_specific_program.md.erb  

  - APIReference/Lending/eligibilities.md.erb
  - APIReference/Lending/get_eligibilities_for_an_account.md.erb

  - APIReference/Lending/quotes.md.erb
  - APIReference/Lending/create_loan_quote.md.erb  
  - APIReference/Lending/get_specific_loan_quote.md.erb    
  - APIReference/Lending/get_loan_quotes_for_an_account.md.erb

  - APIReference/Lending/loans.md.erb
  - APIReference/Lending/create_loan.md.erb  
  - APIReference/Lending/get_specific_loan.md.erb
  - APIReference/Lending/get_loans_for_an_account.md.erb  
  - APIReference/Lending/get_loan_transaction_history.md.erb    
  - APIReference/Lending/close_loan.md.erb

  - APIReference/Lending/loan_transactions.md.erb    
  - APIReference/Lending/apply_interest.md.erb   
  - APIReference/Lending/make_payment.md.erb     
  - APIReference/Lending/add_collateral.md.erb     
  - APIReference/Lending/liquidate_collateral.md.erb   


  - APIReference/Lending/webhooks.md.erb    

  - errors

search: true

code_clipboard: true
---

# _About the Developer_
<img src="images/three_hats.png" alt="three_hats" style="float:right;margin:0px;padding-left:40px;padding-right:56px;"/>
Hi! I'm a technical solutions professional with over 16 years of software engineering experience, specializing in developer platforms, APIs & SDKs, and cloud services. In a sales engineering capacity, I love building relationships with partners and understanding their business needs deeply. In advocacy of the developer, I partner with internal product engineering teams to drive new features and to release incredible new products to market. My ultimate goal is to bring delight to the end users, all while building an ever more efficient, secure, and profitable API product platform.

As a cryptocurrency investor and enthusiast since 2017, I'm passionate about Web3 and the future of democratized digital finance. In my spare time, I enjoy running blockchain nodes and contributing to various projects, such as Trace Labs' recent World Economic Forum-sponsored [Trusted COVID-19 Essential Supplies Repository](https://www.weforum.org/agenda/2021/02/origintrail-blockchain-covid-supplies-repository/).

# _About the Project_
This API platform proof-of-concept (PoC) enables banking integration partners to offer their end-users the ability to obtain a USD loan against their Bitcoin position. Complete API documentation for the Service Platform is included, along with a dedicated integration guide that presents a mobile app reference implementation. All content is my own, authored in calendar Q2 of 2022.

### High-Level Architecture
<img src="images/architecture.png" alt="architecture" style="margin:0px;padding-left:28px;"/>

# _Partner Integration Guide_
<div>
    <iframe class="guide-iframe" src="artifacts/Bitcoin-Secured-Lending-Integration-Guide.pdf"  title="Bitcoin-Secured Lending Integration Guide" style="border:none;width:54%;height:700px;padding-left:28px"></iframe>
    <div class="guide-mobile-iframe" style="display:none;padding-left:28px">The <a href="file:artifacts/Bitcoin-Secured-Lending-Integration-Guide.pdf">Partner Integration Guide</a> is available for download.</div>
</div>

# _API Design_
The [API Design document](file:artifacts/Bitcoin-Secured-Lending-API-Design.pdf), complete with market analysis and product research is available for download.

<br/><br/>

<div><p style="font-size:30px;font-weight:bold;color:#888888;padding-left:28px";>REST API DOCUMENTATION</p></div>

# Overview
We're pleased to offer a brand new Lending API to make it possible for our partners to develop solutions that enable their end-users to obtain a USD loan against their Bitcoin position. This section contains the API endpoints and the request and response schemas for all methods required to integrate to the platform.

## Postman Collection
The quickest way to get started is to use our <a href="artifacts/postman.json" download>Postman</a> request collection. The following steps will help you get up and running. If you prefer, our API can also easily be explored with other tools, like cURL.

### 1) Open the Postman Collection

<div class="postman-run-button"
data-postman-action="collection/import"
data-postman-collection-url="artifacts/postman.json"></div>
<script type="text/javascript">
  (function (p,o,s,t,m,a,n) {
    !p[s] && (p[s] = function () { (p[t] || (p[t] = [])).push(arguments); });
    !o.getElementById(s+t) && o.getElementsByTagName("head")[0].appendChild((
      (n = o.createElement("script")),
      (n.id = s+t), (n.async = 1), (n.src = m), n
    ));
  }(window, document, "_pm", "PostmanRunObject", "https://run.pstmn.io/button.js"));
</script>
<style>
  .postman-run-button {
    position: relative;
    left: 30px;
  }
</style>

### 2) Configure the Postman Environment

 * Setup a new environment by clicking the Gear icon at top right
 * Name the new environment _Bitcoin Lending_ and click _Add_ to create
 * Expand the _GET STARTED_ folder and select the _Environment Setup_ method
 * Select the _Pre-req._ tab and set `bearer-token` to the Access Token Value previously obtained
 * Click the _Send_ button

### 3) Explore the API

 * Execute any of the requests within the collection
 * Refer to this documentation for the requirements of each method

<aside class="warning">
If Postman returns a <i><b>"Could not get any response"</b></i> error, most likely you need to set the environment (as in step #2 above).
</aside>