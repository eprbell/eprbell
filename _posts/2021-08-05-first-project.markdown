---
layout: post
title:  "First Project"
date:   2021-08-05 08:30:00 -0700
categories: eprbell status
tags: bitcoin crypto tax python
---
When I got into Bitcoin a few years ago, I found out that crypto-related tax preparation was not trivial:
- keeping track of multiple transactions, coins, exchanges, wallets, balances, cost bases, long/short-term capital gains, in-out lot relationship and fractioning was tedious and error-prone;
- I could have used a crypto tax preparation service, but preserving privacy and not sending transaction information to third parties unnecessarily was another concern: I preferred to do all crypto tax computation on my own machine.

One of the goals of my sabbatical was to experiment with different cryptocurrency-related investment strategies, but this could generate tax ramifications and I didn't want such intricacy to hold me back: I needed to find a solution to the above problems so that I could transact freely without worrying about making a mistake in my taxes.

After some research, I decided to write my own crypto tax calculator and then open-source it so that others could use or contribute to it. I had just stumbled upon the first project of my new career as a self-employed investor and software developer!

The result of this effort was [RP2](https://github.com/eprbell/rp2), available on Github. RP2 handles the complexity described above and prioritizes user-privacy by storing crypto transaction information locally on the user's computer and never sending it anywhere else. It generates a mock form 8949 and a detailed tax report, tracking flows across wallets/exchanges, taxable events, balances, capital gains, lot fractioning, FIFO ordering and a lot more. This makes my tax accountant happy and reduces tax preparation grind and the risk of calculation error.

RP2 is designed with a programmable plugin architecture for output generators: currently it has only US-specific plugins, but it's possible to contribute additional output generators for different countries or US-based cases. It has extensive unit test coverage to reduce the chance of regression and it's written in Python 3, so it runs on all most commonly used OSes (it has been tested on Windows 10, macOS and Linux).

As for the name, RP2 is a reference to Warren Buffett's claim that Bitcoin is "[rat poison squared](https://www.cnbc.com/2018/05/05/warren-buffett-says-bitcoin-is-probably-rat-poison-squared.html)". Other smart people occasionally made [famously](https://www.snopes.com/fact-check/paul-krugman-internets-effect-economy/) [wrong](https://libquotes.com/thomas-edison/quote/lbx5e7q) [remarks](https://en.wikipedia.org/wiki/Robert_Metcalfe#Incorrect_predictions) about technology: I have a feeling Buffett's quote might end up among those.