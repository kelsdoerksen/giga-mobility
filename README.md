<div align="center">

# UNICEF-Giga: Mapbox Mobility Analysis to Support Global School Mapping

<p>
<b><a href="#-description">Description</a></b>
|
<b><a href="#-dataset">Dataset</a></b>
|
<b><a href="#-code-organization">Code Organization</a></b>
</p>

</div>

## 📄 Description
This work presents the processing and analysis of [Mapbox Movement](https://docs.mapbox.com/data/movement/guides/) data for the purposes of extracting features and insight for automated school mapping. This work is developed under Giga, a global initiative by UNICEF-ITU to connect every school to the internet by 2030.

Obtaining complete and accurate information on schools locations is a critical first step to accelerating digital connectivity and driving progress towards SDG4: Quality Education. However, precise GPS coordinate of schools are often inaccurate, incomplete, or even completely non-existent in many developing countries.  In support of the Giga initiative, we leverage machine learning and a combination of remote sensing and auxillary data to accelerate school mapping. We hypothesize that mobile device timeseries data could be valuable in helping to deilineate between building types for our AI models, thereby reducing the number of False Positives and wasteful use of ground-based validation resources.

This work aims to support government agencies and connectivity providers in improving school location data to better estimate the costs of digitally connecting schools and plan the strategic allocation of their financial resources.

<p>

## 🚶‍♀️ Dataset
Official documentation from MapBox can be found at [Mapbox Documentation](https://docs.mapbox.com/). We use hourly weekday, weekend Mapbox activity index data, which is a Mapbox proprietary movement indicator that reflects the level of activity in the specified time span and geographic region.


## 📚 Code Organization
`KMeans_Clustering.ipynb` notebook for clustering samples via KMeans method.

`AdminZones_Clustering.ipynb` notebook for clustering samples via administrative boundaries according to geoBoundaries.

`Buffer_Intersection.ipynb` notebook for adding Mapbox mobility data to school/non-school samples according to user-defined buffer extent (in meters).

`Point_Intersection.ipynb` notebook for adding Mapbox mobility data to school/non-school samples according to direct intersection with Mpabox quadkey or by taking the nearest Mapbox mobility point to the aoi.

`TimeSeries_Feature_Generation.ipynb` notebook for generating movility data features to be used by ML classifier.

