# Tunnel-Onion-Token (TOT's)
White Paper
A Ethereum side chain for decongestion, anonymity, and off chain compute

---Global Chain Variables---
" these variables are published and updated on the etherium netowrk"

Scaling values
   -   publishers requried
   -   editors required
   -   appraisers required
trust values
   "minimum trust value of a token to be used in each position
   -   publisher minimum
   -   editor minimum
   -   appraiser minimum
   -   cooldown minimum
   -   entry minimum
   -   end minimum
   -   etc... 
Blacklistings
 - lenght of blacklist is a variable
 - list of 4 arrays of e.g. 100 most recent tokens that made errrors, array[publishers, edditors, appraisers, nodes]
 - start working in a tunnel until you are off the list
 - if your on a blacklist your trust value is halved wich you must be advertising in your tunnel proof of work
 - if you are the at the end of blacklist and have not done any tunneling you are placed first of list again
 - blacklist currently has a problem that it can be filled up quickly with asholes... is thinking

int 256 chain_token_lifespan_lenght =< 10
" the list of where a token is in its lifespan, minted at highest number
   - publisher state
   - editor state
   - appraiser state
   - cooldown 
   - entry node
   - end node
   - entry middle node
   - end middle node 
   - middle "technicaly 
   - ... adding middle nodes increases chain length complexity
   - unminted awaiting chain acceptance
  
BranchingFactor 
   - has value from <0-1> is the factor of how much a node will branch, 
   - 0  value as an extreme has the tunnels never branch
   - 1 value as an extreme has the tunnel branch to every node available

---Token Variable ---
 - token_address
 - token_address_type, e.g. erc20, bitcoin
 - current_lifespan
 - address array as inputs, addresses and 
 - address array for outputs
 - payload data
 - chain compute log

simple overview of lifespan state
   -   Publisher state
        -A number of publishers are required to reach concensus for a block to be deployed
        -If a publisher is good it will help the block get published and its payday for everyone including itself.
        -If the publisher is bad it gets blacklisted and its trust value goes to 0 becuase it is naughty
       
   -   Editor State and appraisers do the same thing just at different levels of trust
        - 
   -   cooldown
        A token does no work on a mining machine when cooling down "free money congrats"
        the cooldown is required so that an end node cant emmidiatley appraise the block it was previousely working on
        cooldown nodes must be requested at random to become appraisers chainlink_random_number%(number of apraisers             required)
        they may also be requested to give a ruling on a tunnel dispute to add a node to the blacklist
          this will increase their trust making them more likely to be a publisher but cooldown length increases
     - end node
       end nodes cant be blacklisted as they arent at fault for a chinese whisper of the tunnel
       
          
       
        
Block Architecture published to etherium
   -   0 current global variables
   -   0a next block global variables concensus
   -   1a published TOT's block data condensed (payday!!! execute on chain)
   -   1b publishers blacklist (listing the previouse blocks publishers and edditors who have caused an error)
   -   2a editors TOT's block data condensed (will attempt to become 1a on next chain execution otherwise blacklisted)
   -   2b editors TOT's blacklist (listing the previouse blocks appraisers who have caused an error
   -   3a appraiser TOT's block data condensed
   -   3b appraiser TOTS's blacklist (does not affect trust value but is used by apraisers)
   -   
   -   
        
