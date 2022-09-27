# Cron Config Template

A configuration designed in simple YAML/Ruby to synchronize `/etc/cron.d` folder.

Specific env key-pair is required for each managed file to avoid accidental deletion of un-managed crons.

**Only for platforms that supports `/etc/cron.d` natively**. Program will not work without the specified folder/filesystem specification.

## Installation

- Get your `ruby` installation.
- `gem install bundler`, if there's no Bundler.
- `bundle install` to match packages mentioned in `Gemfile.lock` (if any).

## Executable

- `bundle exec ruby sync-jobs [param]`
  
  with `param` is either `add`, `delete`, `sync`.

I do not recommend running **`delete`** before copying the files to `jobs/` folder, as all commands use `jobs/` as file to copy from and `/etc/cron.d` as managed directory to write.

**Always backup your `/etc/cron.d` before doing this.**

## Copying

To copy this template, **`git clone` then changing the remote** is preferred than **forking the repo** first. As this repo is just a template, not for actual cronjobs that potentially private. 

Forking this repo if you are either developing this as well or fine with public managed cronjobs.

