# deveggs baskets

Community baskets for [deveggs](https://github.com/kunggaochicken/deveggs): developers who
chose to publish how they work with agents. Browse them for ideas, and borrow anything that
looks useful. This repo holds only shared baskets, so the deveggs tool repo stays small.

## Layout

```
baskets/<github-username>/
  README.md        optional: how you work
  eggs/            on trial
  chickens/        permanent
  skills/          skills/{eggs,chickens}/<id>/SKILL.md
  scripts/         optional
```

## Borrowing an egg

Copy the file into your own basket's `eggs/` folder, **never** into `chickens/`.
Someone else's chicken is only an egg for you: it hasn't been tried in your loop.
Clear the `trials` row (`✓0 ✗0`) and the `## Trials` log. Then add a line to its
`context` saying where you borrowed it from, and try it like any other egg.

Borrowed skills work the same way: copy `skills/chickens/<id>/` into your
`~/.deveggs/skills/eggs/<id>/` and add `[egg: on trial] ` to the start of its description.

## Sharing yours

Use `deveggs share --dry-run` first. It builds a copy of your basket with private
details stripped (origin quotes, repo names, session ids, paths, emails, secrets) and
shows what it would share and what it redacted. Then run `deveggs share` to open the PR.

To share by hand:

1. **Review before you share.** An egg's Origin section and `context` row hold your
   verbatim words, repo names and session details. Remove anything private:
   client names, internal repos, credentials, anything from work you can't publish.
   Leave out `cracked/`.
2. Copy your basket into `baskets/<your-github-username>/`, keeping the same layout.
3. Open a PR to `kunggaochicken/deveggs-baskets` from a branch based on `main`. It should
   touch only `baskets/<your-github-username>/`.

Never commit your personal basket's git history or anything outside your own folder.
