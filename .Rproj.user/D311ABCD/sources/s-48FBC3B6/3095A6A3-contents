#' Building a function in order to replicate 'lineplot' functions in Seaborn
#' Draw a line plot with possibility of several semantic groupings
#' The relationship between x and y can be shown for different subsets
#' of the data using the hue, size, and style parameters
#' These parameters control what visual semantics are used
#' to identify the different subsets
#' @param x, y Variables that specify positions on the x and y axes
#' @param hue Grouping variable that will produce lines with different colors
#' @param size Grouping variable that will produce lines with different widths
#' @param style Grouping variable that will produce lines with different dashes and/or markers
#' @param data Input data structure
#' Either a long-form collection of vectors
#' that can be assigned to named variables or
#' a wide-form dataset that will be internally reshaped
#' @return The matplotlib axes containing the plot
#' @author Eyvaz Najafli
#' @details
#' By default, the plot aggregates over multiple y values
#' at each value of x and shows an estimate of the central
#' tendency and a confidence interval for that estimate
#' @seealso \href{https://seaborn.pydata.org/generated/seaborn.lineplot.html}{Seaborn}
#' @export
#'

visualize <- function(x, y, hue, data){
  sns <- reticulate::import('seaborn', as='sns')
  sns$set()
  sns$set_theme(style="whitegrid")
  plot <- sns$lineplot(x=x, y=y, hue=hue, data=data)
  return(plot)
}


