# ICGC DCC - Portal

Parent project of the portal modules

## Build

From the command line:
```
$ mvn
```

## Running

### Command-line

From the root of the project:

```shell
mvn -pl '!dcc-portal-ui' compile && mvn -pl dcc-portal-api exec:java -Dexec.args="server /absolute/path/to/settings.yml"
```

Technically the first part only has to be done when source files change.

### IDE
From Eclipse or IntelliJ:

| Property   | Value                            |
| ---------- | -------------------------------- |
| Main Class | `org.icgc.dcc.portal.PortalMain` |
| VM Options | `-Xmx6G`                         |
| Arguments  | `server /path/to/settings.yml`   |

*Note: If Eclipse or IntelliJ are taking a long time to build before running, try excluding
the dcc-portal-ui as a module.*
    
## Modules

Sub-system modules:

- [Portal API](dcc-portal-api/README.md)
- [Portal UI](dcc-portal-ui/README.md)
- [Portal PQL](dcc-portal-pql/README.md)

## Changes

Change log for the user-facing system modules may be found [here](CHANGES.md).

## Copyright and License

* [License](LICENSE.md)
