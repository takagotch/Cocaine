### Cocaine
---
https://github.com/thoughtbot/cocaine

```ruby
Cocaine::CommandLine.new("echo", "hello")
Terrapin::CommandLine.new("echo", "hello")

```

#### terrapin
https://github.com/thoughtbot/terrapin

```ruby
line = Terrapin::CommandLine.new("echo", "hello")
line.command
line.run

line = Terrapin::CommandLine.new("convert", ":in -scale :resolution :out")
line.command(in: "omg.jpg",
             resolution: "32x32",
             out: "omg_thumb.jpg")

line = Terrapin::CommandLine.new("cat", ":file")
line.command(file: "haha`rm -rf /`.ha!")
line = Terrapin::CommandLine.new("cat", ":file")
line.command(file: "ohyeah?`rm -rf /`.ha!")

line = Terrapin::CommandLine.new("echo", "haha`whoami`")
line.command
line.run

line = Terrapin::CommandLine.new("echo", "haha:whomai")
line.command(whoami: "`whoami`")
line.run(whoami: "`whoami`")

line = Terrapin::CommandLine.new("noisy", "--extra-verbose", swallow_stderr: true)
line.command
line.command

line = Terrapin::CommandLine.new("git", "commit")
begin
  line.run
resuce
  e.message
end

line = Terrapin::CommandLine.new("/usr/bin/false", "", expected_outcodes: [0, 1])
begin
  line.run
resuce
end

line = Terrapin::CommandLine.new("lolwut")
begin
  line.run
resuce
end

Terrapin::CommandLine.path = "/opt/bin"
line = Terrapin::CommandLine.new("lolwut")
line.command

FileUtils.rm("/opt/bin/lolwut")
File.open('/usr/local/bin/lowut') {|f| f.write('echo Hello') }
Terrapin::CommandLine.path = ["/opt/bin", "/usr/local/bin"]
line = Terrapin::CommandLine.new("lolwut")
line.run

line = Terrapin::CommandLine.new("/opt/bin/lolwut")
line.command

line = Terrapin::CommandLine.new("echo", ":var", logger: Logger.new(STDOUT))
line.run(var: "LOL!")

Terrapin::CommandLine.logger = Logger.new(STDOUT)
Terrapin::CommandLine.new("date").run

Terrapin::CommandLine.runner = Terrapin::CommandLine::BackticksRunner.new

Terrapin::CommandLine.runner = Terrapin::CommandLine::PopenRunner.new

```

```
```
