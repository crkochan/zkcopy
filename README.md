# zkcopy

Forked from kshchepanovskyi/zkcopy

Tool for fast copying ZooKeeper data between different clusters.
Originally it was developed for copying big volumes of configuration over WAN.

## Build

Requires [apache maven 3](https://maven.apache.org/).

```bash
mvn clean install
```

## Usage

```bash
java -jar target/zkcopy.jar --source server:port/path --target server:port/path
```

For [docker](https://hub.docker.com/r/crkochan/zkcopy/), use following commands:

```bash
docker pull kshchepanovskyi/zkcopy
docker run --rm -it crkochan/zkcopy --source server:port/path --target server:port/path
```

## Options

```
usage: zkcopy
 -c,--copyOnly <true|false>       (optional) set this flag if you do not
                                  want to remove nodes that are removed on
                                  source
 -h,--help                        print this message
 -s,--source <server:port/path>   location of a source tree to copy
 -t,--target <server:port/path>   target location
 -w,--workers <N>                 (optional) number of concurrent workers
                                  to copy data
```
