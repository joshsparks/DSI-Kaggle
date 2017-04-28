# GROUP PROJECT MEETING NOTES 4/17

## First In-Person Meeting

Over the weekend, Sparks set up a Github Repo that contained a readme markdown file and all the csv files derived from Kaggle
	He added branches for each member of the group

Additionally, he set up a Trello board that states the deliverables of the project as well as various benchmarks to meet in the progression of the project, accompanied by dates for completion

(TL;DR Sparks won the first weekend)

### Discussing Next Steps:

merge weather and train datasets on date
write script (.py, .ipynb file) to open datasets (one of the deliverables asked for)

plan to meet this upcoming Sunday (4/23), either in person or discussion of project progress/mid-timeline check-in vis-a-vis the Interwebs

create a notebook specifically for EDA (combined with script for opening dataset? Yes?)

Miranda: brainstorming ideas for how to combine lat and long into singular numeric value (vectors?)
	also, maybe using a scatterplot, just plotting x=lat, y=long, hue="WNVpresent" to check out geographic representation of incidence of WNV in mosquito traps
	--> binning coordinates for geographic classification?

look at trends within species

(NB: M = missing)

QUESTION: can we collapse weather data into average over the two stations? Do we want to?

create Annotated Bibliography



# MEETING NOTES 4/18

Monday night, Sparks cleaned all the data. You go, Glen Coco.

## Going Over Sparks' Data Cleaning:

EDA (re: Ritika's function)

Date-time converted to datetime format
	create y/m/d columns (because spray data includes time)
	would create issues for joining dataframes
	time forced to military format

Cleaning Weather Data:
	human error in Sunset Times (17:60 instead of 18:00)

Basically everything is almost 100% sanitized --- A couple of missing values (maybe 30-40 total observations), to be filled by Miranda on Tuesday (4/18) night

### Discussing Next Steps:

-create EDA markdown file (Sparks)

-create Research directory, to be filled with lab notebook (this document), Annotated Bibliography, 
pdfs of relevant scientific journal articles (Miranda for initialization)

-add resources (relevant articles, with notes on relevance) to Trello (all)

-finish data cleaning from Sparks' existing jupyter notebook (Miranda)

-initial investigation into inferences / relationships (Ray)

-GIT ISSUES (Sparks/Miranda)



# MEETING NOTES 4/23

Final Cleaning and EDA, last steps in pre-modeling
finishing up Scientific Method documentation and research
writing Problem Statement (Sparks)
Ray wants to use LDA (Ray)


## WEEK OF MONDAY, 4/24:

Feature Selection and Visual EDA (Miranda)
Creating master dataframe that combines weather, spray, and train or (exclusive or) test data for modeling (Sparks)
Discussion of what existing research, background information tells us about what features might be most predictive (Group)

Individual running of models on train data only, followed by models fit on train data and submitted to Kaggle

Kaggle scores derived from ROC-AUC scores
NB: private score derived from 70% test dataset, public score derived from 30% test dataset

First model submitted, Random Forest on all features in master dataframe, receives 96% accuracy but only 63% ROC-AUC score for train-test-split within train data. Once submitted to Kaggle, performs @ 62%

Best performing model receives 74.8% ROC-AUC score on Kaggle
	Gradient Boosting Classifier with tuned parameters and 9 features 
	features included were chosen from Random Forest feature importance, those that performed best

Models that used 6, 7, 8, 10, and 11 features performed worse

XGBoost did not outperform Gradient Boosted Trees

Pipeline of Random Forest and Gradient Boosting underperformed both Random Forest and Gradient Boost performed independently


What are the takeaways? What can we recommend to the Chicago Department of Public Health?

*Those traps that have seen WNV before are more likely to see it again, so respray in those areas
*WNV spikes after Mosquito populations spike mid-to-late summer, concentrate spraying at these times
*C. pipiens is unsurprisingly the species most often responsible for carrying WNV, perhaps target more specifically



