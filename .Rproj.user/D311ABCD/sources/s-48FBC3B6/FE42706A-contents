#' Building a function in order to replicate 'groupby' functions in pandas
#' Group DataFrame using a mapper or by a Series of columns
#' A groupby operation involves some combination of splitting
#' the object, applying a function, and combining the results
#' @param data The input data inserted for analysis
#' @return function returns analysis results on dataset including:
#' cumcount() -- Number each item in each group from 0 to the length of that group - 1
#' cummax() -- Cumulative max for each group
#' cummin() -- Cumulative min for each group
#' cumprod() -- Cumulative product for each group
#' cumsum() -- Cumulative sum for each group
#' @author Eyvaz Najafli
#' @details
#' GroupBy objects are returned by groupby calls
#' @seealso \href{https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html}{Pandas}
#' @export
#'

analysis <- function(data.raw){
  pd <- reticulate::import('pandas', as='pd')
  dataframe <- reticulate::r_to_py(data.raw)
  testthat::expect_is(dataframe,class = "pd.core.frame.DataFrame")
  grouped.sp.cnt <- reticulate::r_to_py(dataframe$groupby('Species')$cumcount())
  grouped.sp.max <- reticulate::r_to_py(dataframe$groupby('Species')$cummax())
  grouped.sp.min <- reticulate::r_to_py(dataframe$groupby('Species')$cummin())
  grouped.sp.prod <- reticulate::r_to_py(dataframe$groupby('Species')$cumprod())
  grouped.sp.sum <- reticulate::r_to_py(dataframe$groupby('Species')$cumsum())
  return(c(grouped.sp.cnt, grouped.sp.max, grouped.sp.min,
           grouped.sp.prod, grouped.sp.sum))
}

