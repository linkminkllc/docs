# Pagination

## 

Requests for most top level resources will return a list of items. These list resources all all have pagination parameters that control how the results are returned. These parameters at a minimum include `limit`, `starting_after`, and `ending_before`.

`limit` is used to specify the number of items to return in the result.

`starting_after` and `starting_before` are used to specify a cursor location. Both of these parameters accept an object id, which is a beginning point from which to return `limit` results. Only one should be used at a time.

### Example:

If you've already retrieved  a list of commissions, and the last commission in the list has `id: com_MdZEf3LYnHxDOhwasVjQ`, then you could request the next ten items in the list using this request: 

```text
$ curl https://app.linkmink.com/api/v0.1.0/commissions \
  -u priv_live_TjziuG12nzkgTcTmRJBw: \
  -d limit=10 \
  -d starting_after=com_MdZEf3LYnHxDOhwasVjQ
```



