Thanks for your contribution!

## Edit the task view:

### Requirements:

* R (to create the `.html` from the `.ctv` file) [Installation](http://cran.r-project.org/)
* `pandoc`: [Installation](http://johnmacfarlane.net/pandoc/installing.html)

If you don't want to or can't install these things, then just edit the `webtech.ctv` file, and submit a pull request.

### Steps

1. Fork this repo
2. Edit the [webtech.ctv](https://github.com/ropensci/webservices/blob/master/webtech.ctv) file. If the package you are adding is on CRAN, add a new `<li>` element with your package name within a `<pkg>` tag. If it's not on CRAN, put it within an `<a>` tag, and include a link to the repo with `href`.
3. On the command line type `make` and press enter, which creates the `WebTechnologies.html`, `README.md`, and `index.html` files.
4. Check to make sure the `.ctv` file is correct, by doing in R

    ```coffee
    setwd("/path/to/webservices/")
    install.packages("ctv")
    library("ctv")
    check_ctv_packages("WebTechnologies.ctv")
    ```

    And you should get

    ```coffee
    $`Packages in <info> but not in <packagelist>`
    character(0)

    $`Packages in <packagelist> but not in <info>`
    character(0)

    $`Packages in <packagelist> but not in repos`
    character(0)
    ```

    If you don't, follow the error messages to fix. If you can't figure out how to fix, just send the PR anyway, and the maintainer will fix.

    If you changed anything in the `webtech.ctv` file, repeat step 3 to remake files. If everthing was fine, proceed.
5. Push back up to your account, then send a pull request to `ropensci/webservices`

## Submit an issue

If you just want to submit an issue, then go to the [issues page](https://github.com/ropensci/webservices/issues?state=open) and do that.
