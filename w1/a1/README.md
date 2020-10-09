# A1: Data Curation

In order to work through this assignment and execute the Jupyter Notebook, clone this repo and run `jupyter notebook` from the location of the notebook (e.g. Human_Centered_Data_HW1.ipynb).

# Goal of the project:
To construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from December 2007 through September 30 2020

# License:
Wikimedia's general Terms of Use: https://foundation.wikimedia.org/wiki/Terms_of_Use/en
License of the source data can be found here: https://creativecommons.org/licenses/by-sa/3.0/legalcode

# Link to relevant APIs:
https://wikimedia.org/api/rest_v1/metrics/legacy/pagecounts/aggregate/{project}/{accesands-site}/{granularity}/{start}/{end}
https://wikimedia.org/api/rest_v1/metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end}

# Gathering data: 
The data was access using Legacy Pagecounts API (https://wikimedia.org/api/rest_v1/metrics/legacy/pagecounts/aggregate/{project}/{access-site}/{granularity}/{start}/{end}) from 200712-201608 and Pageviews API(https://wikimedia.org/api/rest_v1/metrics/pageviews/aggregate/{project}/{access}/{agent}/{granularity}/{start}/{end} from 200712-202008

For each API  data for all months where data is available were extracted. Data was as raw results into 5 separate JSON source data files available on the repository.

* NOTE: Pageview API excludes spiders/crawlers, however data from the Pagecounts API does not
* Note: A new page view definition tool effect on May 2015. This change eliminated all crawler traffic. In the graph described in the data analysis section, red, green and brown mark new definition.

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

# Vallues of all fields:
year (year of the access)
month (month of the access)
pagecount_desktop_views (number of the desktop views available from pagecount API)
pagecount_mobile_views (number of the mobile views available from pagecount API)
pageview_desktop_views (number of the desktop views available from pageview API)
pageview_mobile_views (number of the mobile views available from pageview API)
pagecount_all_views (total number of the desktop and mobile view avaialable from pagecount API)
pageview_all_views (total number of the desktop and mobile view avaialable from pageview API)

# Data analysis
year and month were indexed  
visualized the dataset as a time series graph
The number of views on the y axis (x 10,000,000,000) shows the number of views.
* Note: A new page view definition tool effect on May 2015. This change eliminated all crawler traffic. Red, green and brown mark new definition.

