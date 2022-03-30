# Tips for using Git and GitHub aimed at new uses of the OpenSAFELY system

Rendered at https://remlapmot.github.io/git-and-github-for-os/

To build/render the html output open the project in RStudio and either

* open the *Build* pane click the *Build Website* button
* or, run in R

    ``` r
    rmarkdown::render_site(encoding = 'UTF-8')
    ```
* or more simply as there is just one output type

    ``` r
    rmarkdown::render_site(output_format = 'bookdown::gitbook_book', encoding = 'UTF-8')
    ```
