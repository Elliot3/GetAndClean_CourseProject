# README - Getting and Cleaning Data - Course Project

## Introduction

The goal of this Repository is to represent the final Course Project for the Coursera course Getting and Cleaning Data taught in conjunction with Johns Hopkins University.

The purpose of this assignment is to demonstrate all of the skills learned in the course involving taking multiple data sets, merging them together and then cleaning them up to allow for analysis. The data associated to this project is data collected from accelerometers from the Samsung Galaxy S smartphone. The following are included in this Repository: the script to run the clean-up/analysis (run_analysis.R), a CodeBook (CodeBook.md) which describes the variables, the data and the associated transformations, as well as this README (README.md).

## Requirements

All of the analysis has been developed using R version 3.1.1.

## Installation

1. Download the data here:[URL](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).
2. Execute the run_analysis.R script which performs the following:
- Reads all of the pertinent files
- Creates 3 separate data frames: masterDataSet, keyDataSet and subjectDataSet
- Using these files, the data for all 3 is merged into one master data frame
- Only the columns pertaining the mean or standard deviations are then selected
- The columns for subject_id and activity_labels are added to the resulting data frame
- The columns names are edited to make them more descriptive
- A file is created, tidyDataSet.csv, which calculates the average for each variable for each activity and each subject

## Configuration

For all of the Configuration explanation, please consult the Code Book.