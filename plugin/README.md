# Fyug

Compose and play generative music with an agent. Ask for a piece in your own
words ("a slow ambient drone in D dorian", "a Bach invention on marimba") and
the agent writes it, plays it and refines it with you.

## What this plugin adds

- **Skills**: `fugue` (the way in: it works out how a piece will play where
  you are), `fugue-invention-author` (writes a new piece),
  `fugue-development-author` (packages a reusable instrument or effect) and
  `fugue-review-listener` (listens to the piece and suggests a change).
- **The hosted Fyug server** (`https://mcp.fyug.fm/mcp`): checks a piece and
  plays it in an in-chat player, where you and the agent change it as it
  plays. It needs no account and nothing installed.

The plugin holds text files only and installs nothing on your machine. One
of them is a short Python script, `skills/fugue/scripts/write_preview.py`,
which the agent can run where there is no hosted server to write a piece into
a preview page you open in your browser. It reads the files you name and
writes that one page; it sends nothing anywhere.

## Install

In Claude Code:

```
/plugin install fyug --marketplace Ilusiv-media/fyug
```

In Codex:

```
codex plugin marketplace add Ilusiv-media/fyug
codex plugin add fyug@fyug
```

## The in-chat player and the full product

The in-chat player runs the piece in your browser, with a reduced set of
instruments and effects. On the web it sits beside the chat and lets you
download the piece or share a link to it; on a phone the music stops when the
player is off screen. Fyug itself is a native app that plays live on your
machine, in the background, with every instrument, your own samples and a
view of the piece. A downloaded piece opens there with `fyug play`:

https://github.com/Ilusiv-media/fyug#install

Once Fyug is installed, run `fyug setup` to connect it to your agent. The
skills use it in place of the in-chat player or the preview page when it is
there.

## License

MIT. See `LICENSE`.
