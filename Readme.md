#### Steps to reproduce
* `git clone git@github.com:GoalSmashers/npm-windows-wrapper-bug.git`
* `cd npm-windows-wrapper-bug`
* `npm install`
* `demo.bat`

#### Expected behavior
* Files 1.min.css and 2.min.css are created.

#### Actual behavior
* Only the first file is created as `demo.bat` exits right after executing the first command (see [demo.bat](./demo.bat) source).

#### Example of right behavior
* `works.bat`

It creates both files but clean-css is called directly, not through the cleancss.cmd wrapper in `.\node_modules\.bin\`

#### Affected versions
* node.js 0.8.x, 0.10.x, tested on NPM 1.2.14 on Windows 7
