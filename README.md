# BIproject

# MILESTONE 1: EXPLORATORY DATA ANALYSIS

#Loading the dataset library(readr) pima_indians_diabetes \<- read_csv("data/pima-indians-diabetes.csv") View(pima_indians_diabetes)

# ------Issue 1:Decriptive Statistics-----

#Measures of Frequency pima_indians_diabetes_freq \<- pima_indians_diabetes\$Glucose cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$`No. of pregnancies` cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$`Blood Pressure` cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$`Skin Thickness` cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$Insulin cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$B.M.I. cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$`Diabetes predigree function` cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$Age cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

pima_indians_diabetes_freq \<- pima_indians_diabetes\$Class cbind(frequency = table(pima_indians_diabetes_freq), percentage = prop.table(table(pima_indians_diabetes_freq)) \* 100)

#Measures of Central Tendancy #Mode pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$Class))[  which(table(pima_indians_diabetes$Class) == max(table(pima_indians_diabetes\$Class))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$`No. of pregnancies`))[  which(table(pima_indians_diabetes$`No. of pregnancies`) == max(table(pima_indians_diabetes\$`No. of pregnancies`))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$Glucose))[  which(table(pima_indians_diabetes$Glucose) == max(table(pima_indians_diabetes\$Glucose))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$`Blood Pressure`))[  which(table(pima_indians_diabetes$`Blood Pressure`) == max(table(pima_indians_diabetes\$`Blood Pressure`))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$`Skin Thickness`))[  which(table(pima_indians_diabetes$`Skin Thickness`) == max(table(pima_indians_diabetes\$`Skin Thickness`))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$Insulin))[  which(table(pima_indians_diabetes$Insulin) == max(table(pima_indians_diabetes\$Insulin))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$B.M.I.))[  which(table(pima_indians_diabetes$B.M.I.) == max(table(pima_indians_diabetes\$B.M.I.))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$`Diabetes predigree function`))[  which(table(pima_indians_diabetes$`Diabetes predigree function`) == max(table(pima_indians_diabetes\$`Diabetes predigree function`))) ] print(pima_indians_diabetes_mode)

pima_indians_diabetes_mode \<- names(table(pima_indians_diabetes$Age))[  which(table(pima_indians_diabetes$Age) == max(table(pima_indians_diabetes\$Age))) ] print(pima_indians_diabetes_mode)

#Mean mean_age \<- mean(pima_indians_diabetes\$Age) print(mean_age)

mean_pregnancies \<- mean(pima_indians_diabetes\$`No. of pregnancies`) print(mean_pregnancies)

mean_glucose \<- mean(pima_indians_diabetes\$`Glucose`) print(mean_glucose)

mean_blood_pressure \<- mean(pima_indians_diabetes\$`Blood Pressure`) print(mean_blood_pressure)

mean_skin_thickness \<- mean(pima_indians_diabetes\$`Skin Thickness`) print(mean_skin_thickness)

mean_insulin \<- mean(pima_indians_diabetes\$Insulin) print(mean_insulin)

mean_BMI \<- mean(pima_indians_diabetes\$B.M.I.) print(mean_BMI)

mean_DPF \<- mean(pima_indians_diabetes\$`Diabetes predigree function`) print(mean_DPF)

#median median_pregnancies \<- median(pima_indians_diabetes\$`No. of pregnancies`) print(median_pregnancies)

median_glucose \<- median(pima_indians_diabetes\$Glucose) print(median_glucose)

median_blood_pressure \<- median(pima_indians_diabetes\$`Blood Pressure`) print(median_blood_pressure)

median_skin_thickness \<- median(pima_indians_diabetes\$`Skin Thickness`) print(median_skin_thickness)

median_insulin \<- median(pima_indians_diabetes\$Insulin) print(median_insulin)

median_BMI \<- median(pima_indians_diabetes\$B.M.I.) print(median_BMI)

median_DPF \<- median(pima_indians_diabetes\$`Diabetes predigree function`) print(median_DPF)

median_age \<- median(pima_indians_diabetes\$Age) print(median_age)

median_class \<- median(pima_indians_diabetes\$Class) print(median_class)

#Measures of Distribution summary(pima_indians_diabetes)

#standard deviation sapply(pima_indians_diabetes[, 1:8], sd)

#variance sapply(pima_indians_diabetes[, 1:8], var)

#kurtosis if (!is.element("e1071", installed.packages()[, 1])) { install.packages("e1071", dependencies = TRUE) } require("e1071")

sapply(pima_indians_diabetes[, 1:8], kurtosis, type = 2)

#skewness sapply(pima_indians_diabetes[, 1:8], skewness, type = 2)

#Measures of Relationship #Covariance pima_indians_diabetes_cov \<- cov(pima_indians_diabetes[, 1:8]) View(pima_indians_diabetes_cov)

#Correlation pima_indians_diabetes_cor \<- cor(pima_indians_diabetes[, 1:8]) View(pima_indians_diabetes_cor)

#-----Issue 2:Inferential Statisitics----- #Statistical tests(ANOVA)

library(dplyr) library(broom) #One way Anova result_anova \<- aov(`No. of pregnancies` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`Glucose` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`Blood Pressure` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`Skin Thickness` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`Insulin` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`B.M.I.` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`Diabetes predigree function` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

result_anova \<- aov(`Age` \~ Class, data = pima_indians_diabetes) summary_anova \<- summary(result_anova) print(summary_anova)

#Two way anova result_two_way_anova \<- aov(Class \~ `No. of pregnancies` \* Age, data = pima_indians_diabetes) summary_two_way_anova \<- summary(result_two_way_anova) print(summary_two_way_anova)

result_two_way_anova \<- aov(Class \~ Insulin \* Glucose, data = pima_indians_diabetes) summary_two_way_anova \<- summary(result_two_way_anova) print(summary_two_way_anova)

result_two_way_anova \<- aov(Class \~ `Diabetes predigree function` \* Age, data = pima_indians_diabetes) summary_two_way_anova \<- summary(result_two_way_anova) print(summary_two_way_anova)

#-----Issue 3:Basic Visualization----- #Univariate plots

#histogram par(mfrow = c(1, 8)) for (i in 1:8) { hist(pima_indians_diabetes[, i], main = names(pima_indians_diabetes)[i]) }

#bar plot barplot(table(pima_indians_diabetes[, 9]), main = names(pima_indians_diabetes)[9])

#box plot par(mfrow = c(1, 8)) for (i in 1:8) { boxplot(pima_indians_diabetes[, i], main = names(pima_indians_diabetes)[i]) }

#Multivariate plots

#Correlation plot if (!is.element("ggcorrplot", installed.packages()[, 1])) { install.packages("ggcorrplot", dependencies = TRUE) } require("ggcorrplot") ggcorrplot(cor(pima_indians_diabetes[, 1:8]))

#Scatter plot pairs(Class \~ ., data = pima_indians_diabetes, col = pima_indians_diabetes\$Class)

#Box and Whisker plots if (!is.element("caret", installed.packages()[, 1])) { install.packages("caret", dependencies = TRUE) } require("caret")

featurePlot(x = pima_indians_diabetes[, 1:8], y = pima_indians_diabetes[, 9], plot = "box")

# MILESTONE 2: PREPROCESSING AND DATA TRANSFROMATION

if (!is.element("NHANES", installed.packages()[, 1])) { install.packages("NHANES", dependencies = TRUE, repos = "<https://cloud.r-project.org>") } require("NHANES")

## dplyr ----

if (!is.element("dplyr", installed.packages()[, 1])) { install.packages("dplyr", dependencies = TRUE, repos = "<https://cloud.r-project.org>") } require("dplyr")

## naniar ----

if (!is.element("naniar", installed.packages()[, 1])) { install.packages("naniar", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

require("ggplot2")

## MICE ----

if (!is.element("mice", installed.packages()[, 1])) { install.packages("mice", dependencies = TRUE, repos = "<https://cloud.r-project.org>") } require("mice")

## Amelia ----

if (!is.element("Amelia", installed.packages()[, 1])) { install.packages("Amelia", dependencies = TRUE, repos = "<https://cloud.r-project.org>") } require("Amelia")

pima_subset \<- pima_indians_diabetes %\>% select(Age, `No. of pregnancies`, Glucose, `Blood Pressure`, `Skin Thickness`, Insulin, `B.M.I.`, `Diabetes predigree function`)

### Subset of rows ----

# We then select 500 random observations to be included in the dataset

rand_ind \<- sample(nrow(pima_subset), 500, replace= FALSE) pima_indians_diabetes \<- pima_subset[rand_ind, ] str(pima_subset)

#Confirmation of missing values any_missing \<- any(is.na(pima_indians_diabetes)) print(any_missing)

# -----MILESTONE 3: TRAINING THE MODEL-----

#Installing and Loading the Required Packages \## caret ---- if (require("caret")) { require("caret") } else { install.packages("caret", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

## klaR ----

if (require("klaR")) { require("klaR") } else { install.packages("klaR", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

## e1071 ----

if (require("e1071")) { require("e1071") } else { install.packages("e1071", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

## readr ----

if (require("readr")) { require("readr") } else { install.packages("readr", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

## LiblineaR ----

if (require("LiblineaR")) { require("LiblineaR") } else { install.packages("LiblineaR", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

## naivebayes ----

if (require("naivebayes")) { require("naivebayes") } else { install.packages("naivebayes", dependencies = TRUE,

```         
               repos = "https://cloud.r-project.org")
```

}

##mlbench if (!is.element("mlbench", installed.packages()[, 1])) { install.packages("mlbench", dependencies = TRUE) } require("mlbench")

train_index \<- createDataPartition(pima_indians_diabetes\$class, p = 0.80, list = FALSE) pima_indians_diabetes_train \<- pima_indians_diabetes[train_index, ] pima_indians_diabetes_test \<- pima_indians_diabetes[-train_index, ]

#Bootstrapping train_index \<- createDataPartition(pima_indians_diabetes\$class, p = 0.65, list = FALSE) pima_indians_diabetes_train \<- pima_indians_diabetes[train_index, ] pima_Indians_diabetes_test \<- pima_indians_diabetes[-train_index, ]

```         
 #Training a logistic regression model
```

train_control \<- trainControl(method = "boot", number = 500)

pima_indians_diabetes_model_lm \<- caret::train( class \~ `No. of pregnancies` + Glucose + `Blood Pressure` + `Skin Thickness` + Insulin + `B.M.I.` + `Diabetes predigree function` + Age, data = pima_indians_diabetes_train, trControl = train_control, na.action = na.omit, method = "glm", family = binomial(), metric = "Accuracy" )

```         
#Testing the model
```

predictions_lm \<- predict(pima_indians_diabetes_model_lm, pima_indians_diabetes_test[, 1:9])

#Viewing the accuracy and the predicted values print(pima_indians_diabetes_model_lm) print(predictions_lm)

# MILESTONE 4: HYPER-PARAMETER TUNING AND ENSEMBLES

# Load the necessary package and dataset

library(caret) data(PimaIndiansDiabetes) dataset \<- PimaIndiansDiabetes

# Separate independent and dependent variables

pima_independent_variables \<- dataset[, 1:8] pima_dependent_variable \<- dataset[, 9]

# Define the control parameters for model training

seed \<- 42 metric \<- "Accuracy" train_control \<- trainControl(method = "repeatedcv", number = 10, repeats = 3, search = "random")

# Perform random search for the Random Forest model

set.seed(seed)

# Define the search space for mtry

mtry_values \<- c(1:ncol(pima_independent_variables))

# Random search over mtry values

pima_model_random_search_rf \<- train(pima_dependent_variable \~ ., data = pima_independent_variables, method = "rf", metric = metric, tuneGrid = data.frame(.mtry = sample(mtry_values, 12)), trControl = train_control)

print(pima_model_random_search_rf) plot(pima_model_random_search_rf)

# MILESTONE 5: CONSOLIDATION

if (require("plumber")) { require("plumber") } else { install.packages("plumber", dependencies = TRUE, repos = "<https://cloud.r-project.org>") }

## caret ----

if (require("caret")) { require("caret") } else { install.packages("caret", dependencies = TRUE, repos = "<https://cloud.r-project.org>") } name_of_function \<- function(arg) { \# Do something with the argument called `arg` } loaded_diabetes_model_lda \<- readRDS("./models/saved_diabetes_model_lda.rds")

#\* @apiTitle Diabetes Prediction Model API

#\* @apiDescription Used to predict whether a patient has diabetes or not.

#\* @param arg_pregnant The number of pregnancies the patient has had #\* @param arg_glucose Plasma glucose concentration (glucose tolerance test) #\* @param arg_pressure Diastolic blood pressure (mm Hg) #\* @param arg_triceps Triceps skin fold thickness (mm) #\* @param arg_insulin 2-Hour serum insulin (mu U/ml) #\* @param arg_mass Body mass index (weight in kg/(height in m)\^2) #\* @param arg_pedigree Diabetes pedigree function #\* @param arg_age Age (years)

#\* @get /diabetes

predict_diabetes \<- function(arg_pregnant, arg_glucose, arg_pressure, arg_triceps, arg_insulin, arg_mass, arg_pedigree, arg_age) { \# Create a data frame using the arguments to_be_predicted \<- data.frame(pregnant = as.numeric(arg_pregnant), glucose = as.numeric(arg_glucose), pressure = as.numeric(arg_pressure), triceps = as.numeric(arg_triceps), insulin = as.numeric(arg_insulin), mass = as.numeric(arg_mass), pedigree = as.numeric(arg_pedigree), age = as.numeric(arg_age)) \# Make a prediction based on the data frame predict(loaded_diabetes_model_lda, to_be_predicted) } api \<- plumber::plumb("BIproject.R")

# Specify a constant localhost port to use

api\$run(host = "127.0.0.1", port = 5022)
