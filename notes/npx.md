# `npx`

`npm` package runner. Included since `npm@5.2.0`. Helps round out experience of using NPM registry packages - `npm` makes it easy to install and manage dependencies, `npx` makes it easy to use CLI tools and executables.

Calling `npx <command>` when `<command>` isn't in $PATH automatically installs package and invokes it. When done, installed package won't be in globals, no long-term pollution.
