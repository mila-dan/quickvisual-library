# quickvisual-library
A plotting library in Python built on top of Matplotlib and Seaborn


The library is uploaded to https://pypi.org/project/Quickvisual/

To install the library: pip install Quickvisual

To create charts: 
1. install the library
2. import the Charts class: from Quickvisual import Charts
3. create an object: chart_one = Charts(df)
4. make a plot: chart_one.plot(col)

The main functions:

1. plot_hist(col) - a histogram of numeric column with automatic bin size 
2. plot_scatter(xcol, ycol) - a scatter plot of two numeric variables
3. plot_bar(xcol, ycol, func) - a bar plot of numeric variable by categorical xcol.
	f.e., plot_bar(xcol='product_type', ycol='price', func='mean') - a barplot of average price by product_type
4. plot_count(xcol, hue = None) - a count plot of categorical variable xcol
5. plot_line(xcol, ycol, hue = None) - a line plot of mean ycol by xcol
	f.e. plot_line(xcol='period', ycol='price', hue='product_type') - average price by period for different product types
6. plot_box(xcol, ycol) - a box plot distribution of numeric variable ycol by categorical xcol
7. plot_violin(xcol, ycol) - a violin plot distribution of numeric variable ycol by categorical xcol
8. plot_bar_with_line(xcol, bar_col, line_col, bar_func, line_func) - a bar plot and a line plot of xcol, 
	where bar_col represents a bar, bar_func - aggregation function of a bar, line_col represents a line with line_func - aggregation function for a line.