# Authentication

## API Key \(public and private\)

LinkMink uses API keys to authenticate requests.Your API key is found on the 'Account' page under 'Settings'. 

Since the API exposes many privileges, your API key must be kept secure. It should never be shared or stored in a location where someone else could access it, such as public repositories, or in client-side code.

You'll use your API key to authenticate every request you make to the LinkMink API. Authentication is accomplished using [HTTP Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication), with your API key used as the username. 

Any requests that don't include authorization will return an error. Any request that is not made over HTTPS will fail.

### Example: 

```bash
$ curl -u priv_live_TjziuG12nzkgTcTmRJBw: https://app.linkmink.com/api/v0.1.0/commissions
```



