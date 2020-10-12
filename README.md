# Election_Analysis

## Overview of Election Audit

Audit the election results and provide the results in a readable format.

## Election Audit Results

### County Turnout
This election had 3 candidates running with a total vote count of 369,711 through all 3 of the counties. The data set that was received looks like this:

<img src="https://github.com/Changscorner/Election_Analysis/blob/main/Resources/data.png">

Taking a look at this data we can see that there are  3 candidates total with 3 counties. With this information I know I have to create a few lists of dictionaries to fill in with the candidate name, county voted in, and the total amount of votes received by the candidate.

In the dataset there are many duplicates in each row of the candidates names and the counties. To make sure that there are no duplicates inputted into the list we use this code:

```
  if candidate_name not in candidate_options:

    # Add the candidate name to the candidate list.
    candidate_options.append(candidate_name)

    # And begin tracking that candidate's voter count.
    candidate_votes[candidate_name] = 0

  # Add a vote to that candidate's count
  candidate_votes[candidate_name] += 1
```
This code checks to see if the candidate name is already in the list and if it isn't it will append the name to the end of the list and set the vote count for that candidate to 0. It then adds 1 vote to that candidates count.

The breakdown of the counties is as follows:

  - Jefferson: 38,855 votes cast consisting of 10.5% of total votes casted
  - Denver: 306,055 votes cast consisting of 82.8% of total votes casted
  - Arapahoe: 24,801 votes cast consisting of 6.7% of total votes casted

As seen from the results, Denver takes the overwhelming majority of the votes casted in this election. 

### Candidate Vote breakdown

There are 3 candidates in this election.

1.) Charles Casper Stockham

2.) Diana DeGette

3.) Raymon Anthony Doane

Charles Casper Stockham received 23% of the vote with 85,213 votes casted for him.

Diana DeGette received 73.8% of the vote with 272,892 votes casted for her.

Raymon Anthony Doane received 3.1% of the vote with 11,606 votes casted for him.

### Election results

Diana DeGette is the clear winner of this election with a vast lead over the other 2 candidates.

The script outputs all of the details above into a txt file that is easily readible.

<img src="https://github.com/Changscorner/Election_Analysis/blob/main/Resources/election%20results.png">


## Election Audit Summary

This script can be very easily adjusted to accommodate other elections with some very simple changes.

