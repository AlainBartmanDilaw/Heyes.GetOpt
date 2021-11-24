# Purpose
The GetOpt class allows you to easily define and handle command line options and arguments. Various styles of options are catered for each optionally having its own argument.<br>
For example:<br>
  long options: (--foo),<br>
  long options with arguments (--foo=bar),<br>
  short options (-f, /f),<br>
  short options with arguments (-f bar, -fbar) and<br>
  consolidated short options (-fb).

# Example
This example defines 4 options (a, b, foo and bar).<br>
"foo" is required to be given with an argument (eg. --foo=xyz) and bar can be supplied with or without an argument.<br>

    try {<br>
        GetOpt foo = new GetOpt(args);<br>
        GetOpt.SetOpts(new string[] {"a", "b", "foo=", "bar=?"})<br>
        GetOpt.Parse();<br>
    } catch (ArgumentException e) {<br>
        myProgram.PrintUsage();<br>
    }<br>
