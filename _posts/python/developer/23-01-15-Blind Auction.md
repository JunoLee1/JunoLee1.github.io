---
layout: single
title: "[Python] Blind auction"
categories: ["developer"]
tag: [algorithm, python, developer]
toc: true
toc_label: "Table of Contents"
toc_icon: "align-justify" # corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
---

># Blind Auction

I was trying to make blind auction system. First of all, it was essential to  draw an flow chart. 

># flow chart
   1. Ask name and how much he or she can bids on the item
   2. Ask if there is other bid on the item
   3. find maximum bidder 
*Definately* I was stuck in function part.. and how to get winner variable. By making winner before iterate, we could memorize bidder while iterating. 

```python 
from replit import clear
from art import logo
print(logo)

bids = {}
bidding_finished = False

def find_highest_bidder(bidding_record):
  highest_bid = 0
  winner = ""
  # bidding_record = {"Angela": 123, "James": 321}
  for bidder in bidding_record:
    bid_amount = bidding_record[bidder]
    highest_bid = max(highest_bid, bid_amount)
    winner = bidder
    print(f"The winner is {winner} with a bid of ${highest_bid}")

while not bidding_finished:
  name = input("What is your name?: ")
  price = int(input("What is your bid?: $"))
  bids[name] = price
  should_continue = input("Are there any other bidders? Type 'yes or 'no'.\n")
  if should_continue == "no":
    bidding_finished = True
    find_highest_bidder(bids)
  elif should_continue == "yes":
    clear()
  
  


