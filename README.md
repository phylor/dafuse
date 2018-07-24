# Dafuse

Dafuse is a tool to dump and synchronize databases.

Installation:

```
gem install dafuse
```

Dump a database of the environment `staging`:

```
dafuse dump staging
```

## Example Configuration

Configuration is read from the file `dafuse.yml` in your current directory.

Example:
```
staging:
  ssh:
    host: my_server
    user: root
  database:
    name: my_database
    user: database_user
```

## Development & Publication

Run it:

```
ruby -Ilib ./bin/dafuse
```

Install the Gem locally:

```
gem build dafuse.gemspec && gem install dafuse-*.gem
```

Publish gem:

```
gem push dafuse-*.gem
```
