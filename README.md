# NorESM Experiments

An overview of NorESM2 experiments including upgrades, code modifications and parameter settings.

The overview includes:

    NorESM2-MM CMIP6 DECK simulations
    NorESM2-LM CMIP6 DECK simulations
    NorESM2-MM CMIP6 historical simulations
    NorESM2-LM CMIP6 historical simulations
    NorESM2-MM CMIP6 scenario simulations
    NorESM2-LM CMIP6 scenario simulations
    NorESM2-MM spinup tree
    NorESM2-LM spinup tree

## Usage

### Automatic deployment

the GitHub actions workflow (`noresm-exp/.github/workflows/deploy.yml`) automatically renders the content,pushes the rendered output to the `gh-pages` branch of the repo and hosts it on GitHub Pages when a push or pull request is made to the main branch


### Building the book

If you'd like to develop and/or build the NorESM Experiments content, you should:

1. Clone this repository
2. Run `pip install -r requirements.txt` (it is recommended you do this within a virtual environment)
3. (Optional) Edit the source files located in the `noresm_exp_book/content` directory
4. Run `jupyter-book clean noresm_exp_book/` to remove any existing builds
5. Run `jupyter-book build noresm_exp_book/`

A fully-rendered HTML version of the book will be built in `noresm_exp_book/_build/html/`.

## Credits and licence

This project is created using the open source [Jupyter Book project](https://jupyterbook.org/) and the [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).  

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

