---
layout: pages
title: "Fast Trade"
subtitle: My algorithmic trading system
permalink: /fast-trade
date: 2022-03-26
---

## Fast Trade


### Disclaimer

This is a "just for fun" project. Please don't take anything here as financial advice. I'm just some guy on the internet sharing his passion project.

## Motivations

This is a project I started in maybe 2014 (my first github repo was called [MarketSim](https://github.com/jrmeier/MarketSim) and was some PHP files). I wanted to create a trading system you could give a file and it would output trade decisions, both live and historical, for backtesting. The goal, of course, was to use this thing make money in my sleep and generate some truely passive income. I created a few different Around 2019, I started the latest iteration of this project, which I called [fast-trade](https://github.com/jrmeier/fast-trade). I wanted to trade on centralized markets since 1.) that data was extremely available 2.) When I wanted to go live, the APIs make it easy. I wrote it in Python and took advantage of the Pandas library to do all the heavy lifting. I also wrote  

## What is it?

It's an algorithmic trading system. It's a set of rules that you can give a file and it will output trade decisions, both live and historical, since the data can be as current as you want. Essentially, I wanted be able to describe a trading strategy by setting values in a JSON file. It was a fun project to think about how to break down these proccess to binanary decisions. I used data from Binance.US.

## The Library

[fast-trade](https://github.com/jrmeier/fast-trade) is the basic library. By doing `pip install fast-trade` you can use it in your own projects. It's a Python library that takes a JSON file and outputs a Pandas DataFrame with the trade decisions. It's not a full trading system, it's just the engine that makes the decisions. It's up to you to decide how to execute those decisions. You can use it as a CLI or in your python projects.

## The Platform

For a while, I was heavily developing a web platform for that would enable a full GUI. I had users and everything! However, after a few months, it became clear it wasn't quite ready for prime time. User's expect all the features of TradingView and are willing to put up with the far slower backtesting experience that TradingView offers. I'm not sure if I'll ever get back to it, but I'm still proud of the work I did. I wrote the frontend in React.js and setup a simple Flask API to handle the backend. I used Docker to containerize the whole thing and deployed it an old cheap workstation with 64GB of ram and 6 cores I got from someone on craigslist which was sitting in my closet. The backend also included a data managment library that would download and store the updated historical data. The system most imporantly kept a version of the data in memory, which would enable to backend to serve charts and run backtests in real time.

## Result

I only turned it on once and it lost a few dollars. I also really learned the hard way about order and how placing orders and getting the price you want is crutial and extremely hard. I remain convinced there was a lot of "sketchy" things happening the order book resulting in some strange order executions. I suppose this is the risk of using a cryptocurrency exchange for trading.

## The Future

I have another project that uses fast-trade for the same stuff, but manages live data. If the link to [Fast Trade Cache](https://github.com/jrmeier/fast-trade-cache) is live, I have done the work of cleaning it up and making sure it all works.

## Screenshots and Videos

2021 - Viewing traders and editing some settings

!["Fast Trade trader screen as of March 2021"](/images/FastTradeMarch_2021Trader.gif)

Videos:
