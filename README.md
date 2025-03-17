# Astral Tooling Proposal

## Introduction

[Astral, the company behind `Ruff` and `uv`](https://astral.sh/blog/announcing-astral-the-company-behind-ruff) has created tooling for Python that I (Ethan Chang) believe would be highly beneficial for the courses at BU Spark! built around Python (DS 539 DS Practicum, DS 549 ML Practicum).

The two courses listed above struggle when it comes to teaching students about proper Git/GitHub usage, and how to maintain both code quality and future "editabiltiy". Given that most projects in these courses last for multiple semesters, making sure that future students can pickup where previous ones left off should be a high priority.

In addition to `Ruff` and `uv`, switching to a `pyproject.toml` file for dependency tracking would be beneficial for the students as well. This would allow for a more consistent and reproducible environment for the students to work in.

## Ruff

As a former Technical Project Manager (TPM) reading Python code that students wrote, to put it bluntly, was a nightmare and a painful experience. Because none of the BU courses teach you how to properly write or format code, students will often write code that is difficult to read and understand. This is why `Ruff` would be a great tool to use in these courses.

There are two primary reasons why `Ruff` would be beneficial for the courses at BU Spark!:

1. It's a linter
    - We really need a linter for Python in Spark. Without one, students will continue to write code that is difficult to read and understand. It also allows students to learn how to write clean code (or make their code cleaner), which is a valuable skill in the industry.
    - With the Ruff CLI, you simply need to do `ruff check`
2. Automatic Code Format Checking (w/ GitHub Actions)
    - Ruff can be used as a GitHub Action to automatically check the code formatting of a PR or commit. This would help students actually learn how to write clean code, since it  forces a student to have all the checks pass, unless they want to be embarrassed with a big red cross on their PR.
    - This would also make each TPM's life easier, as they would not have to manually check the code formatting of each PR.
    - Ruff's example GA can be found in the examples folder.
        - You can also see it at work in the [WLFC Repo](https://github.com/BU-Spark/ml-wlfc-image/commits/cethan-eda/)
3. Automatic Code Format Fixing (via CLI)
    - With `ruff format`, students can automatically fix their code formatting issues. It does not do any linting, but if there is some code that could be formatted in a more readible way, `ruff format` will do it for you without changing any functionality.
    - You can see an example of this in [this commit at the WLFC Repo](https://github.com/BU-Spark/ml-wlfc-image/commit/874613937c73391be937ce495ba4b32ae92c77bf)
      - The change is not significant, but that small modification makes the code more readable.

- [Ruff Documentation](https://ruff.readthedocs.io/en/latest/)
- [Possible Ruff Linting Rules](https://docs.astral.sh/ruff/rules/)
  - An example of the Ruff rules can be seen in the `example.pyproject.toml` file under all headers that contain `[tool.ruff]`

## uv

## pyproject.toml
