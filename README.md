This is a EOS smart contract for private or public 1st amd 2nd price auctions of real or digital inventory where an auction master (auctioneer) initialises the auction and users can submit bids.

ABI Interface [countour_public.cpp]: (Action caller pays for used ram)
- placebid(user, bid) //Users can place bids
- getwinner() //Get's the current status of the running or ended contract
- getbids() //Dumps list of all bids from x addresses

ABI Interface [countour_private.cpp]: (Owner pays for all ram, only once when setting up the contract)
- placebid(user, bid) //Users can place bids
- getwinner() //Get's the current status of the running or ended contract
- endauction() //Ends the auction, can only be called by contract initiator
- reset() //Reset's the auction so that the contract can be re-used for another auction.

/no_cdt - this directory experiments with implementing the private version of the smart contract in pure C.

Try not to use the pre-compiled smart contracts if you can, as they may not be upto-date with the latest code release.

countour_private is more efficient on ram uage than countour_public.


:: Thoughts for the future

It's notable that a public auction cannot be reset, and that maybe a public auction should identify it's purpose with some kind of queryauctionpurpose() function, but this is optional.

As for private auctions, bidding is currently open to anyone aware of it's existance, maybe bidding access could be password protected? Although, only distributing the awareness of the auction is security enough in my reasoning.

:: Learn More about EOS

If you wish to learn more about EOS smart contracts check out this list of links at the EOS CUB:
http://eos.task.cat
