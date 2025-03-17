# Scripts and data associated with Microbiology Galaxy Lab and microGalaxy 2025 Paper

This repository includes all the scripts and data needed to produce figures in the paper along with the resulted figures.

# Requirements

- Install [conda](https://conda.io/miniconda.html)

    ```
    $ make install-conda
    ```

- Create the conda environment

    ```
    $ make create-env
    ```

# Usage

## Retrieve citations

- Launch [Jupyter](https://jupyter.org/) to access the notebooks to generate graphs

    ```
    $ make run-jupyter
    ```

- Go to [http://localhost:8888](http://localhost:8888) (a page should open automatically in your browser)

## Update data

- Launch the dedicated script

    ```
    $ bash bin/get_data.sh
    ```
    
## Rebuild Extended Figures

```{r}
$ Rscript -e "rmarkdown::render('bin/citations-graphs.Rmd',output_file = tempfile())"      # Extended Figure 1
$ Rscript -e "rmarkdown::render('bin/survey-figure.Rmd', output_file = tempfile())"         # Extended Figure 2
$ Rscript -e "rmarkdown::render('bin/tools-graphs.Rmd', output_file = tempfile())"          # Extended Figure 3
$ Rscript -e "rmarkdown::render('bin/workflows-graphs.Rmd', output_file = tempfile())"      # Extended Figure 4
$ Rscript -e "rmarkdown::render('bin/tutorials-graphs.Rmd', output_file = tempfile())"      # Extended Figure 5
```




