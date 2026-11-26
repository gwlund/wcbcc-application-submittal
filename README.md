# WCBCC Application Submittal

A Claude Code skill that streamlines applying for a seat on the
Whatcom County Business and Commerce Advisory Committee (WCBCC).  

Claude interviews the candidate, drafts the County form's eight questions and the
references line in the candidate's own words, saves a paste-ready answers
file, and copies each answer to the clipboard while the candidate fills in
the form.

The candidate stays in control of everything that goes to the County:
personal details are typed by hand, and the candidate reviews every answer
and clicks Submit.

## Requirements

- Claude Code, installed and signed in.  Setup instructions:
  https://docs.claude.com/en/docs/claude-code
- Git, to download this repository.

## Getting Started

```bash
git clone https://github.com/gwlund/wcbcc-application-submittal.git
cd wcbcc-application-submittal
claude
```

The skill lives inside this repository (`.claude/skills/`), so it loads
whenever Claude Code starts in this folder.  Nothing needs installing in a
personal skills folder.

Then describe the goal in plain words, for example:

> I'd like to apply for the retail seat on the Business and Commerce
> Advisory Committee.

Claude walks through six steps: choosing the seat and confirming the
deadline, a short interview, drafting the answers, the resume or summary,
references, and pasting the answers into the County's form.

## Privacy

Drafts are saved under `applications/`, which is excluded from git.  Nothing
a candidate types is committed or pushed from this repository.  Please keep
it that way if contributing changes back: the County form is a public
document once submitted, but drafts, addresses and phone numbers are not.

## Keeping It Current

Seats and deadlines change every January.  The committee roster, term dates
and deadline live in
`.claude/skills/wcbcc-application-submittal/references/committee-facts.md`,
each with its source and date.  Please open an issue or pull request when a
new roster or deadline comes out.

## Feedback

Built by Gil Lund, WCBCC manufacturing seat.  Questions and suggestions are
welcome as GitHub issues.
