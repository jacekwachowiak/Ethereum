  1. String Saver

  Develop a contract that lets every user to store (in the contract's permanent storage) and retrieve one string value.
  The contract API could look like this:
    * setString(string str): given a string str, store it.
    * getString(): return the previously stored string.

  The contract essentially maintains correspondence between addresses and string. What data structure is appropriate here?
  Note that getString has no arguments. That means the contract must "recognize" the user whose transaction it is now handling.

  2. Crowdfunding

  One of the prominent applications of blockchain-based smart contracts is crowdfunding.
  The problem with centralized solutions (e.g., Kickstarter) is that parties have to trust the service not to run away with the money. Using a smart contract, a person who wishes to collect funds (a beneciary) encodes the rules in the contract code. Supporters can inspect the code and see how money will be distributed.
  Implement a simple crowdfunding contract in Solidity. There are two roles in this contract: a beneciary and a supporter. A beneciary creates a crowdfunding campaign, specifying the target amount of funds and the deadline. A supporter can donate ether to a campaign. After the deadline, if the amount of ether collected is greater than or equal to the target, the beneciary can withdraw it. If the amount is less than the target, every supporter can withdraw the amount they donated.

  3. Dutch Auction

  Another application of smart contracts is auctions. There are multiple ways to organize an auction. In this exercise, implement a Dutch (open-bid descending price) auction.
  The contract should work as follows. The owner species the initial (presumably high) price, the "reserve" (lowest possible) price, and the rate at which the price decreases.
  For instance: initial price is 100 ether, reserve price is 50 ether, price decreases by 1 ether every 5 minutes. Therst user who pays the amount equal to or greater than the current price wins the auction.
  This exercise is taken from the Stanford "Bitcoin and Cryptocurrencies" course. See "Project #4" at https://crypto.stanford.edu/cs251/ for additional information.
