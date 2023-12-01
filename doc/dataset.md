# Dataset

Using the [German Credit Dataset](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data). 

## Features

- Status of existing checking account (categorical)
- 


### Encoding

Depending on if they represent an ordinal or a nominal value, categorical variables should either be integer encoded or one-hot encoded. For some variables, this disticntion is not that clear, so we need to make an educated guess.

- Status of existing checking account (integer encoding, from 0 [no checking] to 5 [over 200 DM in checking])
- 

### Sensitive features

- Age
- sex
- foreign worker (proxy for nationality)