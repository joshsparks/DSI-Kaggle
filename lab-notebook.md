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



