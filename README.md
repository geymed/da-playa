Dynamo Deploy Locker

## Tables

`DaPlayaLocks`

id         |       user        |   env        | createdAt | updatedAt | active | uberlock | meta
                                                           
<UUID>     |  <COMMITER_EMAIL> | PRODUCTION   | 123123123 | 123123123 | true   | false    | CI URL
<UUID>     |  <COMMITER_EMAIL> | STAGING      | 123123123 | 123123123 | false  | true     | Slack
<UUID>     |  <COMMITER_EMAIL> | WHATEVZ      | 123123123 | 123123123 | false  | true     | CLI

## Env Vars

`DAPLAYA_AWS_SECRET_KEY`
`DAPLAYA_AWS_ACCESS_KEY_ID`
`DAPLAYA_SLACK_APP_ID`

## CLI
```sh
lock --env <ENV> --user <USER> [--meta <META>] [--uberlock]
# keeps in writing attempts for locking in case it's waiting
# Still locked at env <ENV> by <USER>

release --env <ENV> --user <USER>

locks --env <ENV>
```

## Slack

/daplaya lock <ENV> [META]
/daplaya uberlock <ENV> [META]
/daplaya release <ENV>
/daplaya leases <ENV>
