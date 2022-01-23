# Visualisation-DIPR

\-----   DESCRIPTION     -----\
This package provides anyone interested the UN's Sustainable Development Goals
a way to explore and identify available data that relates to each goals indicators.
The goal of this tool is to recommend specific indicators a user should investigate when
attempting to model the SDG Indicators. This tool is effectively an SDG
Development Indicator Predictor Recommender, and we have given it the name 'DIPR'.

The tool derives recommendations and trends using two data sources.
1. The World Banks World Development Indicators, or 'WDI'.
2. The United Nations Sustainable Development Goals.

The recommendations are developed by using a novel dimensionality reduction
technique which combines a Correlation Filter and PCA to recommend
what metrics from the expanded set of WDI's (over 1400 available) are impactful.

The trends are developed using a weighted average methodology to project
future SDGI values from the current observed values to determine if
the given goal is on track to meet the criteria set by the UN 2030 Agenda.

A detailed explanation of both methods can be found in the paper in
this package's /DOC folder. Additionally, the /CODE/data_etl folder
contains the notebooks used to produce both the recommendations and the
trends in the /recommendation_etl and /trend_etl subfolders.

Lastly, the data required to run our demo has been preprocessed and comes
loaded with this package. A script (get_dipr_data.ipynb) and instructions
on how to download all source raw data used in the analysis can be found
in a notebook in the /raw_data_etl folder.

\-----   INSTALLATION    -----\

The following steps will make DIPR available on your local machine.

0. Ensure python 3.7.X is available on your local machine. It can
be installed from python.org. You may desire to create a virtual
environment for this project so that python packages installed in
the next step do not conflict with other projects.


1. Open a new terminal/command line session.


2. Install necessary python packages. This can be done by referencing
DIPR's requirements file found at " team140final/CODE/requirements.txt ".

The command is
" pip install -r team140final/CODE/requirements.txt "

The example below shows installing the packacges inside a virtual
environment named "test_env"

" (test_venv) johnb@Johns-MBP test_venv % pip install -r team140final/CODE/requirements.txt "

A message like the one below should be visible upon successful installation

" Successfully installed dash-bootstrap-components-0.12.0 dash-core-components ... "


3. Next, launch the dashboard by navigating to app.py in the terminal/
command line and running the file with python.

Example below

" (test_venv) johnb@Johns-MBP test_venv % cd team140final/CODE/viz/dash "
" (test_venv) johnb@Johns-MBP dash % python app.py "


If successful the message below will be displayed and you can then open the dashboard
in your browser at the url given.

"    * Serving Flask app "app" (lazy loading)                                           "
"    * Environment: production                                                          "
"    WARNING: This is a development server. Do not use it in a production deployment.   "
"    Use a production WSGI server instead.                                              "
"    * Debug mode: off                                                                  "
"    * Running on http://127.0.0.1:8050/ (Press CTRL+C to quit)                         "


\-----     EXECUTION     -----\

1. The DIPR workflow is started by first selecting an SD Goal in the upper ribbon. To do
this the user simply clicks the pane containing the Goal of interest.
2. The dashboard will populate the indicators for that goal in a dropdown.
3. Select the indicator of interest from the drop down.
4. Select the country of interest by clicking it withing the map.
5. The past and predicted trend for that selected indicator will be shown in the upper right.
6. A ranked recommendation of predictors for that indicator will be shown in the lower portion.

\-----   YouTube DEMO    -----\

A demo of our tool can be found at https://www.youtube.com/watch?v=7Z6vyD-zQJs
