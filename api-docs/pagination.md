# Pagination

## 

Requests for top level resources will return a list of items. These list resources have pagination parameters that control which results are returned. These parameters include `limit`, `starting_after`, and `ending_before`.

`limit` specifies the number of results to return. Its default value is 25, its minimum is 1 and its maximum is 100.

`starting_after` and `ending_before` are used to specify a cursor location. Both of these parameters accept an object id, which is a beginning point from which to return `limit` results. Only one should be used at a time.

### Errors:

`limit` must be an integer between 1 and 100. Values outside of this range will result in a 400 level error response.

`starting_after` and `ending_before` must be supplied one at a time. If they are both supplied the response will be a 400 level error.

### Example:

If you've already retrieved  a list of commissions, and the last commission in the list has `id: com_MdZEf3LYnHxDOhwasVjQ`, then you could request the next ten items in the list using this request: 

```text
$ curl https://app.linkmink.com/api/v0.1.0/commissions \
  -u priv_live_TjziuG12nzkgTcTmRJBw: \
  -d limit=10 \
  -d starting_after=com_MdZEf3LYnHxDOhwasVjQ
```



