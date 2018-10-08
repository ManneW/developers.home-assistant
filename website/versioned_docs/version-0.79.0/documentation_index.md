---
title: Documentation
id: version-0.79.0-documentation_index
original_id: documentation_index
---

The user documentation is located at [https://www.home-assistant.io](https://www.home-assistant.io). This section here is the place where we provide documentation and additional details about creating or modifying content.

The [home-assistant.io](https://home-assistant.io) website is built using [Jekyll](http://github.com/mojombo/jekyll) and [these dependencies](https://pages.github.com/versions/). The pages are written in [Markdown](http://daringfireball.net/projects/markdown/). To add a page, you don't need to know about HTML.

You can use the "**Edit this page on GitHub**" link to edit pages without creating a fork. Keep in mind that you can't upload images while working this way.

For larger changes, we suggest that you clone the website repository. This way, you can review your changes locally. The process for working on the website is no different from working on Home Assistant itself. You work on your change and propose it via a Pull Request (PR).

To test your changes locally, you need to install **Ruby** and its dependencies (gems):

- [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/) if you don't have it already. Ruby version 2.3.0 or higher is required.
- Install `bundler`, a dependency manager for Ruby: `$ gem install bundler`
- In your home-assistant.io root directory, run `$ bundle` to install the gems you need.

Shortcut for Fedora: `$ sudo dnf -y install gcc-c++ ruby ruby-devel rubygem-bundler rubygem-json && bundle`

Then you can work on the documentation:

- Fork home-assistant.io [git repository](https://github.com/home-assistant/home-assistant.io).
- Create/edit/update a page in the directory `source/_components/` for your platform/component. The Home Assistant documention itself is located in the directory `source/_docs/`. 
- Test your changes to home-assistant.io locally: run `rake preview` and navigate to [http://127.0.0.1:4000](http://127.0.0.1:4000)
- Create a Pull Request (PR) against the **next** branch of home-assistant.io if your documentation is a new feature, platform, or component.
- Create a Pull Request (PR) against the **current** branch of home-assistant.io if you fix stuff, create Cookbook entries, or expand existing documentation.

It could be necessary that you run `rake generate` prior to `rake preview` for the very first preview.

Site generated by `rake` is only available locally. If you are developing on a headless machine use port forwarding:

```bash
$ ssh -L 4000:localhost:4000 user_on_headless_machine@ip_of_headless_machine
```
