# Dataset

Using the [German Credit Dataset](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data). 

## Features

- Status of existing checking account (categorical)
- 


### Encoding

Depending on if they represent an ordinal or a nominal value, categorical variables should either be integer encoded or one-hot encoded. For some variables, this distinction is not that clear, so we need to make an educated guess.

#### One-hot encoding

- 

#### Integer encoding

- Status of existing checking account (0 [no checking], 1 [< 0 DM], 2 [0-200 DM] , 3 [over 200 DM in checking])
- 

### Sensitive features

- Age
- sex
- foreign worker (proxy for nationality)