# Github doc example
## Level 2
**This** is a *paragraph*

```ruby
class Person
  attr_accessor :name, :age

  def initialize(name, age)
    @name = name
    @age = age.to_i
  end
```

- List value 1
- List value 2

![sample](https://github.com/dustybones99/github-doc-example/assets/85003428/d0e88773-7741-4f0e-896e-dee03ee6457f)

```bash
#!/bin/bash

TRACE=""
CP=$$ # PID of the script itself [1]

while true # safe because "all starts with init..."
do
  CMDLINE=$(cat /proc/$CP/cmdline)
  PP=$(grep PPid /proc/$CP/status | awk ' { print $2; }') # [2]
  TRACE="$TRACE [$CP]:$CMDLINE\n"
  if [ "$CP" == "1" ]; then # we reach 'init' [PID 1] => backtrace
    break
  fi
  CP=$PP
done
```
> This is quoted text

## References
- [Github Flavored Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#lists)
- [Understanding and Ignoring Errors in bash](https://www.baeldung.com/linux/bash-errors)

## Semantic Versioning! :mage:
[Semanting Versioning Reference](https://semver.org/)

Given a version number **MAJOR.MINOR.PATCH**, e.g. `1.0.1`

increment the:

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes
Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

  
