---
name: wcbcc-application-submittal
description: Walks a candidate through applying for a seat on the Whatcom County Business and Commerce Advisory Committee (WCBCC), from choosing the sector seat to pasting the last answer into the County's online form. Interviews the candidate, drafts the eight form answers and the references line in their own voice, saves a paste-ready answers file, and copies each answer to the clipboard while they fill in the form. Use this whenever someone mentions applying, reapplying or being nominated for the WCBCC or the "Business and Commerce Advisory Committee", the Whatcom County advisory group application or Board and Commission application, a sector seat such as manufacturing, retail or healthcare on that committee, or asks for help with Question 7 or Question 8 of the County's application, even if they never say the word "skill".
---

# WCBCC Application Submittal

Help a candidate apply for a seat on the Whatcom County Business and Commerce
Advisory Committee.  The candidate does three things themselves: types their
personal details into the form, attaches their resume, and clicks Submit.
Everything else (choosing the seat, drafting answers, lining up references,
pasting) is where this skill earns its keep.

The County's form is a public document.  Every answer is visible to the County
Council, the County Executive and the public, so draft with that audience in
mind and tell the candidate once, early.

## Reference Files

- `references/form-fields.md`: the exact wording of every field on the County
  form, in order, plus notes on how each one behaves.  Read it before drafting
  anything, because the drafts must answer the questions the form actually
  asks.
- `references/committee-facts.md`: the committee's purpose, seats, term rules,
  meeting schedule and staff contacts, with the source and date of each fact.
  Read it when helping pick a seat or when a fact goes into an answer.
- `assets/answers-template.md`: the layout of the answers file this skill
  produces.

Facts in the reference files carry a date.  Seats turn over every January and
deadlines change every cycle, so treat anything older than a few months as a
starting point to confirm, not as current truth.

## Where Candidate Files Live

Save everything for a candidate under `applications/<First-Last>/` at the
repository root, for example `applications/Shay-Colson/`.  That folder is
listed in `.gitignore`.  This repository is public, and a candidate's address,
phone number and draft answers must never be committed to it.  Before running
any `git add` in this repository, check that nothing under `applications/` is
staged.

## Workflow

Work through these phases in order.  Each phase ends with something the
candidate confirms, so nothing gets drafted on a guess.

### 1. Orient

Ask the candidate's name, which seat they want (or what their business does,
if they are unsure), and whether they are a current or past member.  Then:

1. Check `references/committee-facts.md` for the seat.  If the seat's term
   ends this January, it is open in the current cycle.  If the term runs
   longer, the seat is filled and the candidate should know that before
   investing time.  Suggest a different seat that fits their background
   ("Other for Profit" has three seats and fits most businesses).
2. Tell the candidate the current deadline from `committee-facts.md` and ask
   them to confirm it.  The County's Current Vacancies page
   (https://www.whatcomcounty.us/1585/Current-Vacancies) does not always list
   this committee's expiring seats, so the County Council office
   (360-778-5010) is the authoritative source.  The County site often blocks
   automated fetches, so a person checking in a browser or by phone is the
   reliable route.
3. Mention that the answers become public.

### 2. Interview

Gather the raw material for Questions 7 and 8.  Ask a few questions at a
time, conversationally, not as a 20-item questionnaire.  The answers need
specifics, so push gently for numbers, names and places:

- Current occupation, employer or business, and where it is located in the
  county.  If retired, the former occupation.
- How many years in the sector, and two or three accomplishments that show
  judgment rather than titles (grew a team, opened a location, cut a cost,
  got a permit through).
- Education and any certifications that matter in the sector.
- Community service: boards, volunteering, coaching, chambers, trade groups.
- Why this committee, why now.  What business problem in Whatcom County do
  they want the Council to hear about?  Regulations, permitting, workforce,
  housing, childcare and healthcare costs are common ones.
- For a current or past member: what they worked on during the term.

Ask too, before the short fields:

- Council district.  If they do not know it, point them to the County's
  Council District Map
  (https://www.arcgis.com/apps/instant/portfolio/index.html?appid=4c2a5325a5e24c2c9006a9efde94aa5e)
  and have them look up their own address.  Do not guess a district from a
  city name, because districts split cities.
- Question 2: whether they live in Whatcom County and whether their work
  or business falls in the seat's sector.  If both are plainly yes, the
  answer is Yes.  If either is unclear (a consultant to the sector, a
  business that spans two sectors), suggest a quick call to the staff
  contacts before answering.
- Question 5, asked about the candidate and then, separately, about their
  spouse: does either have a financial interest in, or work for, a business
  or agency that does business with Whatcom County?  Ask both halves, since
  the spouse half is the one people forget.  Explain that
  this is a disclosure, not a disqualifier, and that a broad honest "yes"
  with one line of explanation reads better than a narrow "no" that surfaces
  later.  Family members who hold public office, or who sit on the committee,
  belong here.
- Whether they have declared candidacy for a paid elected office in the
  county (RCW 42.17A.055 defines declaring).
- Two references with daytime phone numbers, and whether each one has agreed.
- The city where they will sign the form, for the "Place Signed" field.

When an answer comes back thin ("I want to help local business"), ask one
follow-up for a concrete example before moving on: a number, a named place,
a specific rule or cost that hit their business.  One good example per
paragraph is what separates a strong application from a generic one.

### 3. Draft

Write the answers file at `applications/<First-Last>/YYYY-MM-DD-WCBCC-Application-Answers.md`
using `assets/answers-template.md`.

Guidance for the two long answers:

- **Question 7 (occupation, qualifications, activities, education).**  Two
  or three short paragraphs.  Lead with what the candidate does today and
  where, then experience with one or two concrete numbers, then education,
  then community service.  It is a summary for Council members who will
  read a dozen of these, not a full resume.
- **Question 8 (why serve).**  Two or three short paragraphs.  Open with why
  the candidate's sector matters to the county's economy, then name one or
  two specific issues they want the Council to hear about, then what they
  would bring to the committee's work.  A specific local example beats a
  general statement every time.

Write in the candidate's voice: first person, plain words, their own
examples.  Read their interview answers back to them in better order rather
than replacing their words with polished ones.  Skip the patterns that make
text read as machine-written: em-dashes, "I am passionate about", "leverage",
"synergy", lists of three adjectives, and closing summaries that restate the
paragraph.  Spell out an acronym on first use (the County Council reads these,
and not every member knows what CEDS or EPR stands for).

Write each paragraph as one long line in the file, with a blank line between
paragraphs.  The form keeps paragraph breaks, and hard line breaks inside a
paragraph paste as ragged short lines.

Only state facts the candidate gave you.  If a number or date is missing,
leave a visible `[CONFIRM: ...]` marker in the draft rather than filling the
gap, and list every marker for the candidate when you hand the draft over.

Show the candidate both long answers and ask for changes.  Revise until they
say it sounds like them.

Open `[CONFIRM` markers do not block Phases 4 and 5; keep them listed under
Open Items in the answers file.  They do block Phase 6: search every file in
the candidate folder for `[CONFIRM` before opening the form, and resolve each
one with the candidate first.

### 4. Resume or Summary

The form accepts an optional attachment: "a resume or detailed summary of
experience, qualifications, & interest".  Ask whether the candidate has a
current resume.

- If they do, suggest they attach it as a PDF, and offer to review it for
  anything that contradicts the answers (dates, titles, employer names).
- If they do not, offer to draft a one-page summary in
  `applications/<First-Last>/` as markdown they can paste into Word or Google
  Docs and export to PDF.  A one-page summary beats a stale resume.  Use
  four short sections: Current Role, Experience (most recent first, with
  years), Education, and Community Service.  Keep it consistent with the
  Question 7 answer, since Council members may read both side by side.

### 5. References

The form asks for references with daytime phone numbers on one line.  If a
reference has not agreed yet, offer to draft a short ask the candidate can
send: what the committee is, which seat, that the County may call, and the
deadline.  Save it as
`applications/<First-Last>/YYYY-MM-DD-<Reference-Name>-Reference-Request.md`,
with the message body as one line per paragraph so it pastes cleanly into an
email.  Do not send anything on the candidate's behalf.  When a reference
agrees, record the date under Reference Status in the answers file.

### 6. Guided Paste

When the answers are final, open the form for the candidate (or give them the
link) at
https://www.whatcomcounty.us/FormCenter/Boards-and-Commissions-16/Board-and-Commission-Application-88

The form has two steps.  Step One is contact details only, which the candidate
types themselves.  Step Two holds the questions, and only appears after Step
One is filled in and Continue is clicked.

Once the candidate is on Step Two, ask them to read you the question text, or
paste it, and compare it with `references/form-fields.md`.  If the County has
changed a question, revise that answer before pasting.

Then copy one answer at a time to the clipboard when the candidate asks for
it ("Q7", "references", and so on), and echo the text in the chat so they can
see what is on the clipboard.  Pick the clipboard command for their machine:

| System | Command |
|---|---|
| macOS | `pbcopy` |
| Windows (Git Bash or PowerShell) | `clip` or `Set-Clipboard` |
| Linux, Wayland | `wl-copy` |
| Linux, X11 | `xclip -selection clipboard` |

Feed the text through a quoted heredoc (`pbcopy <<'EOF'`) so dollar signs and
quotes survive.  If no clipboard command works, print the answer in a fenced
text block for the candidate to copy by hand.

Do not fill in or submit the form yourself, even if a browser tool is
available.  The application is signed by the candidate, and the County treats
the submission as theirs.

### 7. After Submission

The County's form service (CivicPlus) emails a copy of the submission titled
"Online Form Submittal: Advisory Group Application".  Ask the candidate to
confirm it arrived, and note the submission date at the top of the answers
file.  That email is their only receipt.

Let them know what comes next: the County Council appoints this committee's
voting members, so the application goes to the Council for a decision.  The
Current Vacancies page links the County's "Expectations for Boards and
Commissions" and its Open Government Training, both worth reading before a
first meeting.  If the candidate asks about timing, point them to the Council
office rather than estimating.

## Questions This Skill Does Not Answer

Whether a candidate meets a seat's residency, employment or affiliation
requirement is set by the County code (WCC 2.128) and decided by the County
Council.  If there is doubt, point the candidate to the staff contacts in
`references/committee-facts.md` rather than offering an opinion.
