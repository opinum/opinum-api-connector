This package simplifies the Opinum API calls.

No magic. You need to follow the [Opinum Swagger Documentation](https://api.opinum.com) for correct formatting of your requests

You first need to create an instance of the ApiConnector class with following parameters:

> _environment_
> > a dictionary of environment variables
> >
> > if `None`, ApiConnector uses your environment variables (_os.environ_)
> >
> > Mandatory environment variables are:
> >
> > * _OPINUM_USERNAME_: the Datahub user. <br>
> > TAKE CARE: if this user has access to multiple tenants and if you do not specify a tenant id,
> > ApiConnector will use the last tenant used.
> > * _OPINUM_PASSWORD_: the password for the user
> > * _OPINUM_CLIENT_ID_: the client id for accessing the API
> > * _OPINUM_SECRET_ the corresponding secret
> > 
> > Optional environment variables are:
> >
> > * _OPINUM_API_URL_: another API URL than the Europe SaaS one (https://api.opinum.com)
> > * _OPINUM_AUTH_URL_: another authentication URL than the Europe SaaS one (https://identity.opinum.com)
> > * _DEFAULT_PUSH_URL_: another push URL than the Europe SaaS one (https://push.opinum.com)
> > * _OPINUM_SCOPE_: the scope of you session (default: "_opisense-api_")<br>
> > if you want to push data, the scope should be "_opisense-api push-data_"

> _account_id_
> > one of the tenant ids available for the Datahub user (default: `None`)

> _retries_when_connection_failure_
> > number of extra attempts when no 200 or 204 return code (default: 0, maximum: 5)


