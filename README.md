# Run random forest pipeline on Flux

1. You need to change the email etc on the pbs file. 
2. The ```#PBS -t 1-100``` part means that we will run the model 100 times. The arrayID will also set the seed for each run.
3. You need to load R/3.5.0 and r-biomed-libs/3.5.0 libraries
4. We also need to have caret installed as a package which is in the r-biomed-libs/3.5.0 module.
```qsub random_forest.pbs```

- ```random_forest.pbs``` runs the ```code/learning/main_RF.R``` file. 
- ```main_RF.R``` file uses functions that are also in ```code/learning``` directory.
- You'll need to change the data that ```main_RF.R``` uses.

# Cat files that are generated for each data-split (each run by arrayID)

You will use the ```cat_files.sh``` for this. 

