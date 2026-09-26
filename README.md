# hans102938.github.io

This repository contains my Quarto website for DSCI 521 Milestone 3. The site includes two computational posts using the Ames Housing dataset:

- an R post: `posts/ames-housing/`
- a Python post: `posts/ames-housing-python/`

The rendered website is written to the `docs/` folder for GitHub Pages.

## Requirements

Install these tools before building the site:

- [Quarto](https://quarto.org/docs/get-started/)
- [uv](https://docs.astral.sh/uv/)
- R

Python dependencies are recorded in `pyproject.toml` and `uv.lock`. R dependencies are recorded in `renv.lock` and activated through `.Rprofile` and `renv/activate.R`.

## Build instructions

Clone the repository:

```bash
git clone https://github.com/hans102938/hans102938.github.io.git
cd hans102938.github.io
```

Restore the Python environment:

```bash
uv sync
```

Restore the R environment from an R console:

```r
renv::restore()
```

Render the website from the repository root:

```bash
uv run quarto render
```

After rendering, open:

```text
docs/index.html
```

The live site is published from the `docs/` folder using GitHub Pages.

## Data

Both analysis posts use the Ames Housing dataset. The original dataset was compiled by Dean De Cock of Truman State University for teaching regression and data analysis, and is described in:

De Cock, D. (2011). "Ames, Iowa: Alternative to the Boston Housing Data as an End of Semester Regression Project." Journal of Statistics Education, 19(3).

Useful source links:

- Original paper: https://jse.amstat.org/v19n3/decock.pdf
- Original data/documentation page: https://jse.amstat.org/v19n3/decock/
- AmesHousing R package mirror: https://github.com/topepo/AmesHousing

The CSV files used by the posts are included in this repository, so rendering the website does not require downloading the dataset from the internet.
