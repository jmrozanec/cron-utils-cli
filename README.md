cron-utils-cli
===========
Command line interface to cron-utils, a Java library to parse, validate, migrate crons as well as get human readable descriptions for them. The project follows the [Semantic Versioning Convention](http://semver.org/)

[![Gitter Chat](http://img.shields.io/badge/chat-online-brightgreen.svg)](https://gitter.im/jmrozanec/cron-utils)
[![Build Status](https://travis-ci.org/jmrozanec/cron-utils-cli.png?branch=master)](https://travis-ci.org/jmrozanec/cron-utils-cli)
[![Coverage Status](https://coveralls.io/repos/jmrozanec/cron-utils-cli/badge.png)](https://coveralls.io/r/jmrozanec/cron-utils-cli)

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/35b1b558473d42c4980432a3ecf84f6c)](https://www.codacy.com/app/jmrozanec/cron-utils-cli?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=jmrozanec/cron-utils-cli&amp;utm_campaign=Badge_Grade)
[![Project stats by OpenHub](https://www.openhub.net/p/cron-utils-cli/widgets/project_thin_badge.gif)](https://www.openhub.net/p/cron-utils-cli/)

**Download**

cron-utils-cli is available on [Maven central](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.cronutils%22) repository.

    <dependency>
        <groupId>com.cronutils</groupId>
        <artifactId>cron-utils-cli</artifactId>
        <version>7.0.1</version>
    </dependency>


***cron-utils CLI***

We provide a simple CLI interface to use cron-utils right from console, without writing a new project!
cron-utils-cli uses semantic versioning, but since lifecycle does not match the one of the core library,
references the tag commit hash in core as metadata in satellite libraries release versions as means to keep traceability
to the core library.

- Usage: `java -jar cron-utils-cli.jar com.cronutils.cli.CronUtilsCLI --validate -f [CRON4J|QUARTZ|UNIX] -e '<cron expression>'`

- Example: `java -jar cron-utils-cli.jar com.cronutils.cli.CronUtilsCLI --validate -f UNIX -e '* 1 * * *'`

If you want a standalone jar without requiring the 'cp', build an uber jar with :
```bash
mvn assembly:assembly -DdescriptorId=jar-with-dependencies
```
Then, launch cli-utils (built in the `target` directory) with :
```bash
java -jar cron-utils-cli-<version>-jar-with-dependencies.jar com.cronutils.cli.CronUtilsCLI --validate -f [CRON4J|QUARTZ|UNIX] -e '<cron expression>'`
```

**Contribute & Support!**

Contributions are welcome! You can contribute by
 * starring and/or Flattring this repo!
 * requesting or adding new features. Check our [roadmap](https://github.com/jmrozanec/cron-utils/wiki/Roadmap)!
 * enhancing existing code: ex.: provide more accurate description cases
 * testing
 * enhancing documentation
 * providing translations to support new locales
 * bringing suggestions and reporting bugs
 * spreading the word 
 * telling us how you use it! We look forward to [list you at our wiki](https://github.com/jmrozanec/cron-utils/wiki/Projects-using-cron-utils)!


Check [our page](http://cronutils.com)! For stats about the project, you can visit our [OpenHUB profile](https://www.openhub.net/p/cron-utils-cli).

Support us donating once or by subscription through Flattr!

[![Flattr this!](https://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=jmrozanec&url=https://github.com/jmrozanec/cron-utils-cli)

**Other cron-utils projects**

You are welcome to visit and use the following cron-utils projects:
 * [cron-utils](https://github.com/jmrozanec/cron-utils): cron-utils core library. Provides means to parse, validate, migrate crons as well as get human readable descriptions for them.
 * [htime](https://github.com/jmrozanec/htime): A Java library to make it easy for humans format a date. You no longer need to remember date time formatting chars: just write an example, and you will get the appropiate formatter.
 * [cron-utils-spring](https://github.com/jmrozanec/cron-utils-spring): A Java library to describe cron expressions in human readable language at Spring framework, using cron-utils.
 * [cron-utils-cli](https://github.com/jmrozanec/cron-utils-cli): cron-utils features made available through a CLI.
 * [cron-utils-sisyphus](https://github.com/jmrozanec/cron-utils-sisyphus): A Scala scheduler that supports multiple cron notations.
 * [cron-utils-scheduler](https://github.com/jmrozanec/cron-utils-scheduler): A Java job scheduler based on cron-utils library.
