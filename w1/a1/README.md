# A1: Data Curation

In order to work through this assignment and execute the Jupyter Notebook, clone this repo and run `jupyter notebook` from the location of the notebook (e.g. Human_Centered_Data_HW1.ipynb).

# Gathering data: 
The data was access using Legacy Pagecounts API (https://wikimedia.org/api/rest_v1/metrics/legacy/pagecounts/aggregate/{project}/{access-site}/{granularity}/{start}/{end}) and Pageviews API(https://wikimedia.org/api/rest_v1/metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end}).

For each API  data for all months where data is available were extracted. Data was as raw results into 5 separate JSON source data files available on the repository.

# Data processing
All the json files were saved into excel files and then merged into one file. 
Following processing were implemented on the columns:
0- all the NAs were replaced with zero
1- combining pageview_mobile_app_views and pageview_mobile_web_views to create "pageview_mobile_views" column 
2- combining pagecount_desktop_views and pagecount_mobile_views to create "pagecount_all_views" 
3- combining pageview_mobile_views and pageview_desktop_views to create "pageview_all_views"
4- pageview_mobile_web_views and pageview_mobile_app_views columns were dropped
5- final  single CSV document(en-wikipedia_traffic_200712-202009.csv) with the following variables was created:
year, month, pagecount_desktop_views, pagecount_mobile_views,pageview_mobile_app_views


# Data analysis
year and month were indexed and line chart of all the variables across year-month were plotted
