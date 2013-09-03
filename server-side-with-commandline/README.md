# Server-side with Commandline

OJ has a [commandline tool](http://ojjs.org/docs.html#commandline) that can build OJ server-side. This will get you started:

## Installing Commandline Tool

(1) Install node

(2) Install the `oj` commandline tool with:

    npm install -g oj

(3) Install node packages through npm by specifying the packages you want in `package.json` and then running:

    npm install

(4) Finally compile `.oj` and `.ojc` files in this directory with:

    oj .

To be clear `.oj` is JavaScript and `.ojc` is CoffeeScript -- use whichever you prefer. Keep in mind the OJ tool can traverse through node `require` calls and unify/minify all files together. It can also minify/unify Node modules such as `underscore`, `backbone`, etc. These will be picked up from your `package.json` file as you would expect.

## Other Commandline Options

Minify with:

    oj . --minify

Watch with:

    oj . --watch

Output to a directory with:

    oj . --output <directory_name>

Recursively compile with:

    oj . --recurse

Show verbose info

    oj . --verbose 4

All of these options can be mixed and matched.

