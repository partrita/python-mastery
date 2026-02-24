# Advanced Python Mastery - Project Overview

This repository contains the materials for the **Advanced Python Mastery** course by David Beazley. It is an exercise-driven course focused on advanced Python programming techniques, language internals, and building a deep mental model of how Python works.

## Project Type: Educational / Course Material

The repository is structured as a self-paced course consisting of presentation slides, exercises, data files, and fully worked-out solutions.

## Directory Structure

- **`Exercises/`**: Contains Markdown files (`exX_Y.md`) for each exercise in the course. Each exercise also has a corresponding `solnX_Y.md` file which provides a written explanation of the solution.
- **`Solutions/`**: Contains the actual Python source code for the exercise solutions, organized into subdirectories by exercise number (e.g., `Solutions/1_1/`).
- **`Data/`**: Contains datasets (CSV, DAT, etc.) used throughout the exercises (e.g., `portfolio.csv`, `prices.csv`).
- **`mybook/`**: A Quarto-based project that likely compiles the course material into a structured book format.
- **`PythonMastery.pdf`**: The core presentation slides for the course. **Start here!**
- **`pixi.toml` / `pixi.lock`**: Configuration for the [Pixi](https://pixi.sh/) package manager, primarily used for managing the Quarto environment.

## How to Use This Repository

1.  **Reference the Slides**: Open `PythonMastery.pdf` to follow the course flow. The slides indicate when to perform specific exercises.
2.  **Perform Exercises**: Go to the `Exercises/` directory and work through the exercises in order (e.g., starting with `ex1_1.md`).
3.  **Data Files**: When an exercise refers to a data file, you can find it in the `Data/` directory.
4.  **Check Solutions**:
    *   For a quick look at the solution logic, see the `solnX_Y.md` files in the `Exercises/` folder.
    *   For the complete, runnable Python code, see the corresponding directory in `Solutions/`.
5.  **Environment Management**: If you need to build the Quarto book or manage dependencies, use `pixi`.
    *   Run `pixi shell` to enter the environment.
    *   Run `pixi run render` to build the documentation.

## GitHub Pages Deployment

The course book is automatically deployed to GitHub Pages via a GitHub Action (`.github/workflows/deploy.yml`).
- **Trigger**: Every push to the `main` branch.
- **Process**:
    1. Sets up the Pixi environment.
    2. Renders the Quarto book located in `mybook/` using `pixi run render`.
    3. Deploys the content of `mybook/_book` to GitHub Pages.

To enable this, go to repository **Settings > Pages** and set the **Source** to **GitHub Actions**.

## Development Conventions

- **Python Version**: The course targets Python 3.6 features but is compatible with modern Python versions.
- **Style**: Exercises emphasize idiomatic Python and deep understanding of language features like decorators, context managers, metaprogramming, and generators.
- **Testing**: While some exercises might involve testing, the primary focus is on exploration and implementation of core concepts.

## Key Files

- `README.md`: General course information and FAQ.
- `PythonMastery.pdf`: The main instructional slides.
- `pixi.toml`: Project dependency management.
- `Exercises/index.md`: The main entry point for all exercises.
