**Project description**

You work as an analyst for the telecom operator Megaline. The company offers its clients two prepaid plans, Surf and Ultimate. The commercial department wants to know which of the plans brings in more revenue in order to adjust the advertising budget.

You are going to carry out a preliminary analysis of the plans based on a relatively small client selection. You&#39;ll have the data on 500 Megaline clients: who the clients are, where they&#39;re from, which plan they use, and the number of calls they made and text messages they sent in 2018. Your job is to analyze clients&#39; behavior and determine which prepaid plan brings in more revenue.

**Description of the plans**

Note: Megaline rounds seconds up to minutes, and megabytes to gigabytes. For **calls** , each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For **web traffic** , individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.

**Surf**

1. Monthly charge: $20
2. 500 monthly minutes, 50 texts, and 15 GB of data
3. After exceeding the package limits:
  - 1 minute: 3 cents
  - 1 text message: 3 cents
  - 1 GB of data: $10

**Ultimate**

1. Monthly charge: $70
2. 3000 monthly minutes, 1000 text messages, and 30 GB of data
3. After exceeding the package limits:
  - 1 minute: 1 cent
  - 1 text message: 1 cent
  - 1 GB of data: $7

**Instructions on completing the project**

**Step 1**. **Open the data file and study the general information**

File path:

_/datasets/megaline\_calls.csv_ [Download dataset](https://code.s3.yandex.net/datasets/megaline_calls.csv)

_/datasets/megaline\_internet.csv_ [Download dataset](https://code.s3.yandex.net/datasets/megaline_internet.csv)

_/datasets/megaline\_messages.csv_ [Download dataset](https://code.s3.yandex.net/datasets/megaline_messages.csv)

_/datasets/megaline\_plans.csv_ [Download dataset](https://code.s3.yandex.net/datasets/megaline_plans.csv)

_/datasets/megaline\_users.csv_ [Download dataset](https://code.s3.yandex.net/datasets/megaline_users.csv)

**Step 2. Prepare the data**

- Convert the data to the necessary types
- Find and eliminate errors in the data

Explain what errors you found and how you removed them. Note: many calls have a duration of 0.0 minutes. These might be missed calls. Whether or not to preprocess these values is up to you; assess how much their absence would affect the results of your analysis.

For each user, find:

- The number of calls made and minutes used per month
- The number of text messages sent per month
- The volume of data per month
- The monthly revenue from each user (subtract the free package limit from the total number of calls, text messages, and data; multiply the result by the calling plan value; add the monthly charge depending on the calling plan)

**Step 3. Analyze the data**

Describe the customers&#39; behavior. Find the minutes, texts, and volume of data the users of each plan require per month. Calculate the mean, dispersion, and standard deviation. Plot histograms. Describe the distributions.

**Step 4. Test the hypothesis**

- The average revenue from users of Ultimate and Surf calling plans differs.
- The average revenue from users in NY-NJ area is different from that of the users from other regions.

You decide what alpha value to use.

Explain:

- How you formulated the null and alternative hypotheses.
- What criterion you used to test the hypotheses and why.

**Step 5. Write an overall conclusion**

**Format:** Complete the task in Jupyter Notebook. Put the programming code in code cells and text explanations in markdown cells, then apply formatting and headings.

**Description of the data**

Remember! Megaline rounds seconds up to minutes, and megabytes to gigabytes. For **calls** , each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For **web traffic** , individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.

The users table (data on users):

- _user\_id_ — unique user identifier
- _first\_name_ — user&#39;s name
- _last\_name_ — user&#39;s last name
- _age_ — user&#39;s age (years)
- _reg\_date_ — subscription date (dd, mm, yy)
- _churn\_date_ — the date the user stopped using the service (if the value is missing, the calling plan was being used when this data was retrieved)
- _city_ — user&#39;s city of residence
- _plan_ — calling plan name

The calls table (data on calls):

- _id_ — unique call identifier
- _call\_date_ — call date
- _duration_ — call duration (in minutes)
- _user\_id_ — the identifier of the user making the call

The messages table (data on texts):

- _id_ — unique text message identifier
- _message\_date_ — text message date
- _user\_id_ — the identifier of the user sending the text

The internet table (data on web sessions):

- _id_ — unique session identifier
- _mb\_used_ — the volume of data spent during the session (in megabytes)
- _session\_date_ — web session date
- _user\_id_ — user identifier

The plans table (data on the plans):

- _plan\_name_ — calling plan name
- _usd\_monthly\_fee_ — monthly charge in US dollars
- _minutes\_included_ — monthly minute allowance
- _messages\_included_ — monthly text allowance
- _mb\_per\_month\_included_ — data volume allowance (in megabytes)
- _usd\_per\_minute_ — price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)
- _usd\_per\_message_ — price per text after exceeding the package limits
- _usd\_per\_gb_ — price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)