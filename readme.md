# Urbit docs

These are the urbit docs as they appear on [urbit.org](urbit.org/docs).

We've found it helps to have a clone of the docs on hand in case urbit.org
experiences high traffic. Follow these steps to get these into your ship:

## Installation

First, you'll need a running urbit. Follow our urbit.org [install
instructions](https://urbit.org/docs/using/install), then
[setup](https://urbit.org/docs/using/setup) an urbit.

Follow the *Network install* below if your urbit is running on the live network
(comets are usually best for development). Follow the *Local install* instead if
you're on a [fake
ship](https://urbit.org/fora/posts/~2017.1.5..21.31.04..20f3~/) or are otherwise
experiencing problems with the network install.

### Network install

In your urbit's `:dojo`, run the command:

    ~your-urbit:dojo> |sync %home ~ropmev-pocseb %docs

Depending on network traffic, this initial merge and sync could take anywhere
between thirty seconds to several minutes. Upon a successful sync you'll see the
output:

    sync succeeded from %docs on ~ropmev-pocseb to %home

If your sync isn't succeeding after a few minutes for whatever reason, run
`|cancel %home` in your `:dojo` and follow the local install below instead.

### Local install

In your urbit's `:dojo`:

    ~your-urbit:dojo> |mount /=home=

If `~your-urbit` was installed at `/urbit/path` on your Unix machine, you can
now find your home desk at the path `/urbit/path/your-urbit/home`.

In Unix, clone this repo somewhere and copy in the `docs` files to your urbit's
mounted `%home` desk. You can run the following shell commands (*replacing your
urbit's home desk path as necessary*):

    $ git clone https://github.com/urbit/docs
    $ cp -r ./docs* /urbit/path/your-urbit/home/web

Your `%clay` filesystem should acknowledge the newly added files.

Lastly, serve your home desk's `web` directory to the web by running the
following `:dojo` command:

    ~your-urbit:dojo> |serve /=home=/web

## Get started!

And now your docs are live! View them at:

    http://localhost:8443/~~/docs

> If you're running multiple ships locally, your port number will be `8444`,
> `8445`, and so on. Check your `:dojo` output for the correct local port of
> your examples urbit, or view these at `https://your-urbit.urbit.org` over DNS
> instead for live-network ships.

## Learn a lot, and have fun!

People are always around on
[`:talk`](https://urbit.org/docs/using/setup#-messaging-talk) and
[`:fora`](https://urbit.org/~~/fora) to answer your questions. Help each other
out, and don't hesitate if you have an idea for a docs improvement. We'd love if
the docs themselves became an Urbit community project.

## Contributing / Feedback

Give us feedback [on `:fora`](https://urbit.org/~~/fora/) on how we can make the
docs better. Let us know about your ideas, requests, and/or problems and we'll
try and get back to you quickly. Pull requests are more than welcome.
