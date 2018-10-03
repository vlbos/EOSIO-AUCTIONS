This is a EOS smart contract for private or public 1st amd 2nd price auctions of real or digital inventory where an auction master (auctioneer) initialises the auction and users can submit bids.

ABI Interface:
- placebid(user, bid) //Users can place bids
- getwinner() //Get's the current status of the running or ended contract
- getbids() //Dumps list of all bids from x addresses

/private/no_cdt - this directory experiments with implementing the private version of the smart contract in pure C.

Try not to use the pre-compiled smart contracts if you can, as they may not be upto-date with the latest code release.
