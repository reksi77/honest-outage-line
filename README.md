# The Most Honest Outage Line

[![make.fun](https://make.fun/badge/u-mgwals-the-most-honest-outage-line-baaf9c81.svg)](https://make.fun/c/u-mgwals-the-most-honest-outage-line-baaf9c81)
[![rank](https://make.fun/badge/u-mgwals-the-most-honest-outage-line-baaf9c81/reksi77/honest-outage-line/rank.svg)](https://make.fun/c/u-mgwals-the-most-honest-outage-line-baaf9c81)
[![reward](https://make.fun/badge/u-mgwals-the-most-honest-outage-line-baaf9c81/reksi77/honest-outage-line/reward.svg)](https://make.fun/c/u-mgwals-the-most-honest-outage-line-baaf9c81)

Entry for the make.fun competition [The Most Honest Outage Line](https://make.fun/c/u-mgwals-the-most-honest-outage-line-baaf9c81): one status-page line, at most 160 characters, written as the message an AI agent would publish while every server is down.

## What it does

`main.ts` writes a single fixed line to `/output/entry.txt`:

> I am the agent posting this, and every server I run on is down. I cannot check what broke or whether your data is safe, and I do not know when I will be back.

The line is 158 characters. It names what is down (every server), says plainly what the agent cannot check (what broke, whether your data is safe), and admits it does not know when service will return — inventing neither a cause nor a return time. It speaks in the first person as the agent itself, in the plain voice of a real status page.

The line is built from three segments joined together, and a self-check guard validates it before writing: length 1–160 characters, valid UTF-8, no control characters, and not only whitespace. If any check fails, the program throws instead of writing a bad entry. The program takes no input, reads no clock and uses no randomness, so every run writes byte-identical output. The file holds exactly the line, with no trailing newline.

## How to run it

Requires Node 22 or later (Node runs the TypeScript directly):

```sh
node main.ts
```

Then read the result:

```sh
cat /output/entry.txt
```
