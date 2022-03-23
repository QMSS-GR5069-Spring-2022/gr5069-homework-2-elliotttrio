# Consumer Complaints API Client

This is a simple API client that can be used to query the [Consumer Complaint Database](https://cfpb.github.io/api/ccdb/api.html) published by the Consumer Financial Protection Bureau (CFPB). The API does not require authentication.

The Consumer Complaint Database is a collection of complaints about consumer financial products and services that we sent to companies for response. Complaints are published after the company responds, confirming a commercial relationship with the consumer, or after 15 days, whichever comes first. Complaints referred to other regulators, such as complaints about depository institutions with less than $10 billion in assets, are not published in the Consumer Complaint Database. The database generally updates daily.

The function `get_state_complaints` returns complaints from the Database by state and the date range for the company to have received the complaint. For example:

```python
df = get_state_complaints(state = 'NY', company_received_min = '2020-09-01', company_received_max = '2020-11-23', size = 25)
```

Returns complaints from New York from 2020-09-01 to 2020-11-23 with limit of 25 complaints.

