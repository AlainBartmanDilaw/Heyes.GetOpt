# Introduction
Previously developped by Richard Heyes (from PHP to CS as far as I know), this library seemed abandoned.

# Purpose
The GetOpt class allows you to easily define and handle command line options and arguments. Various styles of options are catered for each optionally having its own argument.

For example:

  long options: (--foo),

  long options with arguments (--foo=bar),

  short options (-f, /f),

  short options with arguments (-f bar, -fbar) and

  consolidated short options (-fb).

# Example
This example defines 4 options (a, b, foo and bar).

"foo" is required to be given with an argument (eg. --foo=xyz) and bar can be supplied with or without an argument.

    try {
        GetOpt foo = new GetOpt(args);
        GetOpt.SetOpts(new string[] {"a", "b", "foo=", "bar=?"})
        GetOpt.Parse();
    } catch (ArgumentException e) {
        myProgram.PrintUsage();
    }
