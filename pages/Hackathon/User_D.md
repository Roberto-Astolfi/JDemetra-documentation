#### Benchmarking 

Often one has two (or multiple) data of different frequency for the same
target variable. Sometimes, however, these data are not coherent in the
sense that they don't match up. Benchmarking[^1] is a method to overcome
this situation. It happens quite often, as aggregate of higher-frequency
measurement is not necessarily equal to the less-aggregated measurement.
Moreover, the sources of data may have different reliability. Usually it
is thought that less frequent data are more trustworthy as they are
based on larger samples and compiled more precisely. In general, the
more reliable measurements are considered as benchmarks.

In seasonal adjustment methods benchmarking means the procedure that
ensures the consistency over the year between adjusted and
non-seasonally adjusted data. It should be noted that the *ESS
Guidelines on Seasonal Adjustment* (2015) does not recommend
benchmarking as it introduces a bias in the seasonally adjusted data.
Also the U.S. Census Bureau points out that \"*forcing the seasonal
adjustment totals to be the same as the original series annual totals
can degrade the quality of the seasonal adjustment, especially when the
seasonal pattern is undergoing change. It is not natural if trading day
adjustment is performed because the aggregate trading day effect over a
year is variable and moderately different from zero*\"[^2].
Nevertheless, some users may prefer that the annual totals of the
seasonally adjusted series match the annual totals of the original,
non-seasonally adjusted series[^3].

According to the *ESS Guidelines on Seasonal Adjustment* (2015), the
only benefit of this approach is that there is consistency over the year
between adjusted and the non-seasonally adjusted data; this can be of
particular interest when low-frequency (e.g. annual) benchmarking
figures officially exist (e.g. National Accounts, Balance of Payments,
External Trade, etc.) where users\' needs for time consistency are
stronger.

1.  Following the *ESS Guidelines on Seasonal Adjustment* (2015)
    recommendations, by default, the benchmarking functionality is not
    applied (the *Benchmarking* node is empty). To activate it, click on
    the *Specifications* button and activate the checkbox in the
    *Benchmarking* section.

> ![C:\\Users\\st05sg\\Documents\\Sylwia\\SEZONOWOŚĆ\\JDemetra
> Plus\\JDemetra+ User Guide\\bench
> 1.jpg](media=.//media/image1.jpeg){width="5.245138888888889in"
> height="2.763888888888889in"}
>
> Figure 3.88: Benchmarking option -- a default view.

2.  Three parameters can be set here. *Target* specifies the target
    variable for the benchmarking procedure. It can be *Original* (the
    raw time series are considered as target data) or *Calendar
    Adjusted* (the time series adjusted for the calendar effects are
    considered as target data). *Rho* is a value of the AR(1) parameter
    (set between 0 and 1). By default it is set to 1. Finally, *Lambda*
    is a parameter that relates to the weights in the regression
    equation. It is typically equal to 0 (for an additive
    decomposition), 0.5 (for a proportional decomposition) or 1 (for a
    multiplicative decomposition). The default value is 1.

3.  To launch the benchmarking procedure click on the apply button. The
    results are displayed on four panels. The top-left one compares the
    original product of a seasonal adjustment procedure with the result
    from applying a benchmarking to the seasonal adjustment. The
    bottom-left panel highlights the differences between these two
    results. The outcomes are also presented in a table on the top-right
    panel. The relevant statistics concerning relative differences are
    presented in the bottom-right panel.

> ![C:\\Users\\st05sg\\Documents\\Sylwia\\SEZONOWOŚĆ\\JDemetra
> Plus\\JDemetra+ User Guide\\bench
> 2.jpg](media=.//media/image2.jpeg){width="6.066037839020122in"
> height="2.4741721347331582in"}
>
> Figure 3.89: The results of the benchmarking procedure.

4.  Both pictures and the table can be copied in the usual way (see
    2.1.4 and 3.1.1).

> ![F:\\Benchmarking
> 1.jpg](media=.//media/image3.jpeg){width="5.897818241469817in"
> height="3.3516666666666666in"}
>
> Figure 3.90: Options for benchmarking results.

5.  The result of the benchmarking procedure (*benchmarking.result*) and
    the target data (*benchmarking.target*) can be also exported to the
    Excel file (see 3.1.2).

![](media=.//media/image4.png){width="3.5140398075240595in"
height="2.9219411636045494in"}

Figure 3.91: Exporting the results of the benchmarking procedure.

### Detailed seasonal adjustment of multiple time series

This part guides the user through useful functions that can be used in
the regular production of seasonally adjusted data, like summarising the
results, saving and refreshing options. This part is divided into
several case studies. Each of them focuses on a given issue and presents
available options.

As prerequisite, the 3.1.2 scenario should be studied. The specification
for each series included in the multi-document can be modified using the
case studies presented in 3.2.1. Although the case studies presented in
this section are intended for the datasets, they can be also performed
for a single time series, provided that the analysis is done in a
multi-document (the user is expected to follow the path *Statistical
methods* → *Seasonal adjustment* → *Multi Processing* → *New*).

Links to the appropriate parts of the *JDemetra+ Reference Manual*
(2017) for detailed explanations on actions to be provided when
necessary.

Once a seasonal adjustment process for multiple time series is initiated
a relevant item appears in the main menu. It includes the following
options:

-   *Default specification --* displays a list of pre-defined
    > specifications.

-   *Start --* runs the defined seasonal adjustment process. The item is
    > active when some of the series included into SA-Processing window
    > are unprocessed**.**

-   *Refresh* -- refresh a process with new data. Option is active when
    > the previously saved workspace is opened and a relevant
    > multi-document opened. For description of the *Refresh* options
    > refer to 3.2.2.3.

-   *Accept* -- for a time series marked in the *SA-Processing* window
    > this option sets the *Quality* value to *Accepted*. This option is
    > helpful when the user wish to indicate the series for which the
    > results have been reviewed and accepted by the user.

-   *Edit* -- allows to modify the content of the specification by
    > *Copy*, *Copy Series,* *Paste, Delete* and *Cut* the time series
    > that is marked in the multi-processing window.

-   *Clear selection* -- unmarks series selected in the *SA-Processing*
    > window.

-   *Specification...* -- enables to pick the seasonal adjustment
    > specification from the list. The chosen specification will be
    > applied to the time series added to the processing afterwards.

-   *Priority* -- an indicator that can be used to mark series that
    > require more or less attention. Priorities take values from 0
    > to 10. JDemetra+ computes them automatically, based on the average
    > of the (logged) series. The user can choose the method of
    > computation (log-based or level based).

-   *Initial order* -- displays times series on the list in initial
    > order. The option restores the initial order if the list has been
    > sorted by given column (e.g. by quality or method).

-   *Output...* -- offers a set of output formats (TXT, XLS, ODBC, CSV,
    > CSV matrix), the choice of the folder that will contain the
    > results and the content of the exported file.

-   *Report...* -- displays a summary report concerning the processing,
    > including, e.g. number of series, specifications used, models
    > used, diagnostic results.

> ![E:\\Muli proc
> 1.jpg](media=.//media/image5.jpeg){width="5.9520002187226595in"
> height="2.5789162292213472in"}
>
> Figure 3.92: *SAProcessing* menu.

#### Output options

1.  Once a seasonal adjustment process for the dataset is performed the
    results can be exported to the external file. Go to the main menu
    and follow the path: *SAProcessing* → *Output...*

2.  In the *Batch output* window the user can specify which output items
    will be saved and the folder in which JDemetra+ saves the results.
    It is possible to save the results in the *TXT*, *XLS*, *CSV*, and
    *CSV matrix* formats. In the first step the user should choose the
    output format from the list.

> ![](media=.//media/image6.png){width="3.7101279527559057in"
> height="2.829306649168854in"}
>
> Figure 3.93: Default output formats.

3.  The user may choose more than one format as the output can be
    generated in different formats at the same time.

> ![](media=.//media/image7.png){width="3.76415135608049in"
> height="2.5545680227471568in"}
>
> Figure 3.94: Adding an output format to the list.

4.  To display and modify the settings click on the given output format
    on the list. The available options depend on the output format.

5.  For *Csv* format the following options are available: *folder*
    (location of the file), *file prefix* (name of the file),
    *presentation* (controls how the output is divided into separate
    files) and *series* (series included in the file). These options are
    presented in the next points of this case study.

> ![](media=.//media/image8.png){width="3.7683683289588803in"
> height="2.628284120734908in"}
>
> Figure 3.95: Options for a *Csv* format.

6.  The user can define the folder in which the selected results and
    components will be saved (click the *folder* item and choose the
    final destination).

> ![](media=.//media/image9.png){width="4.281737751531058in"
> height="3.2075481189851267in"}
>
> Figure 3.96: Specifying a destination folder.

7.  With the option *File Prefix* the user can modify the default name
    of the output saved in the CSV file.

> ![](media=.//media/image10.png){width="3.145994094488189in"
> height="2.915094050743657in"}
>
> Figure 3.97: Setting a *File Prefix* option.

8.  *Layout* controls how the output is divided into separate files.
    Expand the list to display available options:

-   *HTable* -- the output series will be presented in the form of
    horizontal tables (time series in rows).

-   *VTable* -- the output series will be presented in the form of
    vertical tables (time series in columns).

-   *List* -- the output series will be presented in the form of
    vertical tables (time series in rows). Apart from that, for each
    time series each file contains in separate columns: the data
    frequency, the first year and of estimation span, the first period
    (month or quarter) of observation span and the number of
    observations. The files do not include dates.

> ![](media=.//media/image11.png){width="3.8810958005249345in"
> height="2.9811318897637795in"}
>
> Figure 3.98: Layout options for a *Csv* format.

9.  The *Content* section presents a list of series that will be
    included into set of output files. The list of available codes is
    given in the *JDemetra+ Reference Manual*, section 7.7. To modify
    the initial settings click on the grey button in the *Content*
    section. The *CVS-series* window presents two panels: the panel on
    the left includes a list of all valuable output items. The panel on
    the right presents the selected output items. Mark the series and
    use the arrows to change the settings. Confirm your choice with the
    *OK* button.

> ![](media=.//media/image12.png){width="3.782548118985127in"
> height="3.3674562554680665in"}
>
> Figure 3.99: Specifying a content of the output file.

10. Options available for the *XLS* format are the same as for the *TXT*
    format with an exception of the *Layout* section. The list of
    available codes in the *Content* section is given in the *JDemetra+
    Reference Manual*, section 7.7.

-   *BySeries* -- all results for a given time series are placed in one
    sheet;

-   *ByComponent* -- results are grouped by components. Each component'
    type is saved in a separate sheet.

-   *OneSheet* -- all results are saved in one sheet.

> ![F:\\A User Guide\\Output
> 1.jpg](media=.//media/image13.jpeg){width="2.9168055555555554in"
> height="2.5679997812773405in"}
>
> Figure 3.100: Layout options for an *Excel* format.

11. If the user sets the option layout to *ByComponent*, the output will
    be generated as follows:

> ![](media=.//media/image14.png){width="4.084905949256343in"
> height="1.697250656167979in"}
>
> Figure 3.101: An Excel file view for the *ByComponent* option.

12. The option *OneSheet* will produce the following *XLS* file:

> ![](media=.//media/image15.png){width="4.427083333333333in"
> height="2.375in"}
>
> Figure 3.102: An Excel file view for the *OneSheet* option.

13. By default, the series in the Excel output files are organised
    vertically. When the user unmark the check box the horizontal
    orientation is used.

> ![](media=.//media/image16.png){width="3.673857174103237in"
> height="2.8240004374453194in"}
>
> Figure 3.103: The *VerticalOrientatio*n option.

14. In case of the *TXT* format the only available options are *folder*
    (location of the file) and *series* (results included in the output
    file). The list of available codes in the *Content* section is given
    in the *JDemetra+ Reference Manual*, section 7.7.

> ![](media=.//media/image17.png){width="3.705797244094488in"
> height="2.8396227034120733in"}
>
> Figure 3.104: Options for the *Txt* output.

15. The *CSV matrix* produces the CSV file containing information about
    the model and quality diagnostics of the seasonal adjustment. The
    user may generate the list of default items or create their own
    quality report. By default, all the available items are included in
    the output. The list of the items is given in the *JDemetra+
    Reference Manual*, section 7.7.

> ![](media=.//media/image18.png){width="3.1830850831146105in"
> height="3.6608705161854767in"}
>
> Figure 3.105: List of items available for the *Csv matrix* output
> type.

16. Once the output settings are introduced, click the *OK* button.

> ![](media=.//media/image19.png){width="4.288542213473316in"
> height="3.278261154855643in"}
>
> Figure 3.106: Options for the *Csv matrix* output.

17. For each output format JDemetra+ informs about the status of the
    operation. An exemplary message in presented below.

> ![](media=.//media/image20.png){width="4.252961504811899in"
> height="2.6086953193350833in"}
>
> Figure 3.107: Generating output process result.

#### Revision policies

The saved results from the seasonal adjustment multi-process can be
refreshed when new or modified observations are available. JDemetra+
offers several options for refreshing the output, which are in line with
the *ESS Guidelines on Seasonal Adjustment* (2015) requirements.

1.  To refresh the results open previously saved workspace using the
    path *File* → *Open Workspace*. Choose the multi-document from the
    *Workspace* window (see 2.1.1) and double click on it to display the
    multi-document menu (*SAProcessing*).

> ![F:\\A User Guide\\Detailed SA
> 1.jpg](media=.//media/image21.jpeg){width="5.9920002187226595in"
> height="2.584070428696413in"}
>
> Figure 3.108: Opening a multi-document.

2.  Several refreshment options are available.

> ![](media=.//media/image22.png){width="5.97588145231846in"
> height="2.8389720034995625in"}
>
> Figure 3.109: The *Refresh* menu.

The meaning of the consecutive options is presented in the following
table.

  **Option**                                                                              **Meaning**
  --------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  *Partial concurrent adjustment → Fixed model*                                           The ARIMA model, outliers and other regression parameters are not re-identified and the values of all parameters are fixed. The transformation type remains unchanged.
  *Partial concurrent adjustment → Estimate regression coefficients*                      The ARIMA model, outliers and other regression parameters are not re-identified. The coefficients of the ARIMA model are fixed, other coefficients are re-estimated. The transformation type remains unchanged.
  *Partial concurrent adjustment → Estimate regression coefficients + Arima parameters*   The ARIMA model, outliers and other regression parameters are not re-identified. All parameters of the RegARIMA model are re-estimated. The transformation type remains unchanged.
  *Partial concurrent adjustment → Estimate regression coefficients + Last outliers *     The ARIMA model, outliers (except from the outliers in the last year of the sample) and other regression parameters are not re-identified. All parameters of the RegARIMA model are re-estimated. The outliers in the last year of the sample are re-identified. The transformation type remains unchanged.
  *Partial concurrent adjustment → Estimate regression coefficients + all outliers *      The ARIMA model and regression parameters, except from outliers) are not re-identified. All parameters of the RegARIMA model are re-estimated. All outliers are re-identified. The transformation type remains unchanged.
  *Partial concurrent adjustment → Estimate regression coefficients + Arima model *       Re-identification of the ARIMA model, outliers and regression variables, except from the calendar variables. The transformation type remains unchanged.
  *Concurrent*                                                                            Re-identification of all the RegARIMA model.

##### **Partial concurrent adjustment **

According to the *ESS Guidelines on Seasonal Adjustment* (2015), partial
concurrent adjustment is the strategy in which the model, filters,
outliers and calendar regressors are re-identified once a year and the
respective parameters and factors re-estimated every time a new or
revised data become available. JDemetra+ offers several types of partial
concurrent adjustment.

###### **Partial concurrent adjustment → Fixed model**

The *Partial concurrent adjustment → Fixed model* strategy means that
the ARIMA model, outliers and other regression parameters are not
re-identified and the values of the parameters are fixed. In particular,
no new outliers or calendar variables are added to the model as well as
no changes neither in the calendar variables nor in the outliers' types
are allowed. The transformation type remains unchanged.

The picture below presents the initial model (on the left) and the
results of the refreshment procedure with the *Partial concurrent
adjustment → Fixed model* option (on the right). The parameters of the
ARIMA part are not estimated and their values are the same as before.
The trading days and outliers are fixed too and no new regression
effects are identified.

![](media=.//media/image23.png){width="6.042472659667542in"
height="5.391303587051619in"}

Figure 3.110: A *Partial concurrent adjustment* → *fixed model* revision
policy results.

###### **Partial concurrent adjustment → Estimate regression coefficients**

The *Partial current adjustment → Estimate regression coefficients*
option means that the ARIMA model, outliers and other regression
parameters are not re-identified. The coefficients of the ARIMA model
are fixed, other coefficients are re-estimated. In particular, no new
outliers or calendar variables are added to the model as well as no
changes neither in the calendar variables nor in the outliers' types are
allowed. The transformation type remains unchanged.

The picture below presents the initial model (on the left) and the
results of the refreshment procedure with the *Partial concurrent
adjustment* *→ Estimate regression coefficients* option (on the right).
The number of estimated parameters is 16 in the initial model and 14 in
the revised model (the parameters of the ARIMA model are not estimated.

![](media=.//media/image24.png){width="5.733094925634296in"
height="6.8258366141732285in"}

Figure 3.111: The *Partial concurrent adjustment* *→ Estimate regression
coefficients* revision policy results.

###### **Partial concurrent adjustment → Estimate regression coefficient + Arima parameters**

The *Partial concurrent adjustment → Estimate regression coefficient +
Arima parameters* strategy means that the ARIMA model, outliers and
other regression parameters are not re-identified. All parameters of the
RegARIMA model are re-estimated but the explanatory variables remain the
same. The transformation type remains unchanged.

The picture below presents the initial model (on the left) and the
results of the refreshment procedure with the *Partial* *concurrent
adjustment → Estimate regression coefficient + Arima parameters* option
(on the right). The parameters of the ARIMA part have been re-estimated
and their values have been updated. Also regression coefficients have
been re-estimated and the number of estimated coefficients in the
revised model is the same as in the initial model (i.e. 16 estimated
coefficients). The structure of the model remains unchanged while all
coefficients have been updated.

![](media=.//media/image25.png){width="6.295833333333333in"
height="5.538888888888889in"}

Figure 3.112: The *Partial concurrent adjustment* → *Estimate regression
coefficient + Arima parameters* revision policy results.

###### **Partial concurrent adjustment → Estimate regression coefficient + Last outliers**

The *Partial concurrent adjustment → Estimate regression coefficient +
Last outliers* strategy means that the ARIMA model, outliers (except
from the outliers in the last year of the sample) and other regression
parameters are not re-identified. All parameters of the RegARIMA model
are re-estimated. Software tests for the outliers in the last year of a
data span and include in the model those which are statistically
significant. The transformation type remains unchanged.

The picture below presents the initial model (on the left) and the
results of the refreshment procedure with the *Partial* *concurrent
adjustment → Estimate regression coefficient + Last outliers* option (on
the right). The parameters of the ARIMA part have been re-estimated and
their values have been updated. Also regression coefficients have been
re-estimated. The number of estimated coefficients in the revised model
is larger than the initial model because an additional outlier has been
identified in the last year of a data span.

![](media=.//media/image26.png){width="6.3in" height="8.4in"}

Figure 3.113: The *Partial concurrent adjustment* → *Estimate regression
coefficient + Last outliers* revision policy results.

###### **Partial concurrent adjustment → Estimate regression coefficient + outliers**

The *Partial concurrent adjustment → Estimate regression coefficient +
outliers* option means that the ARIMA model and regression parameters,
except from the parameters for the outliers, are not re-identified. The
parameters of these variables are re-estimated. All outliers are
re-identified, i.e. the previous outcome of the outlier detection
procedure is not taken into account and all outliers are identified and
estimated once again. The transformation type remains unchanged.

The picture below presents the initial model (on the left) and the
results of the refreshment procedure with the *Partial concurrent
adjustment → Estimate regression coefficient + outliers* option (on the
right). The parameters of the ARIMA part have been re-estimated and
their values have been updated. Also regression coefficients for the
calendar variables have been re-estimated. In the revised model there is
no *Prespecified outliers* section. Instead, the outliers were
re-identified.

![](media=.//media/image27.png){width="6.295833333333333in"
height="7.861111111111111in"}

Figure 3.114: The *Partial concurrent adjustment* → *Estimate regression
coefficient + outliers* revision policy results.

[^1]: Description of the idea of benchmarking is based on Dagum, B.E.,
    Cholette, P.A. 1994), and Quenneville, B. et all (2003). Detailed
    information can be found in: Dagum, B.E., Cholette, P.A. (2006).

[^2]: *X-12-ARIMA Reference Manual* (2011).

[^3]: Hood, C.C. (2005).
