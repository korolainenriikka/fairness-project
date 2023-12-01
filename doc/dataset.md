# Dataset

Using the [German Credit Dataset](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data). 

## Features

- Status of existing checking account (categorical)
- Duration (in months)
- Credit history
- Purpose
- Credit amount
- Savings account / bonds
- Present employment since
- Installment rate in percentage of disposable income
- Personal status and sex
- Other debtors / guarantors
- Present residence since
- Age
- Number of existing credits at this bank
- Job
- Number of people being liable to provide maintenance for
- Telephone
- Foreign Worker

### Encoding

Depending on if they represent an ordinal or a nominal value, categorical variables should either be integer encoded or one-hot encoded. For some variables, this distinction is not that clear, so we need to make an educated guess.

#### One-hot encoding

- Purpose
- Other debtors / guarantors
- Telephone (binary)
- Foreign worker (binary)

#### Integer encoding

All features were encoded so that a high value corresponds to a good situation, and a low value to a bad situation.

- Status of existing checking account (0 [no checking], 1 [< 0 DM], 2 [0-200 DM] , 3 [over 200 DM in checking])
- Credit history (4 [all credits at this bank paid back duly],3 [existing credits paid back duly till now], 2 [no credits], 1 [delay in paying off in the past], 0 [critical account/other credits existing (not at this bank)])
- Savings account / bonds (1 [<100 DM], 6 [100-500 DM], 15 [500-1000 DM], 0 [unknown / no account])
- Present employment since (0 [unemployed], 1 [... < 1 year], 2 [1-4 years], 3 [4-7 years], 4 [> 7 years])
- Housing (0 [rent], 1 [own], 2 [for free])
- Job (0 [unemployed], 1 [unskilled], 2 [skilled], 3 [management])

#### Other encoding
- Personal status and sex (create two binary columns: male/female and single/married)

### Sensitive features

- Age
- sex
- foreign worker (proxy for nationality)

### Removed features

Columns whose meaning was not fully understood were dropped. These were the following:

- Property
- Other installment plans