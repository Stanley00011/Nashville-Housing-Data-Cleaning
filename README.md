This project focuses on cleaning and standardizing the Nashville housing dataset stored in the `PortfolioProject.dbo.NashvilleHousing` table. 
The provided SQL queries demonstrate the steps involved in standardizing the date format, populating missing property addresses,
breaking down addresses into individual components, updating fields for clarity, and removing duplicates and unused columns.

Table of Contents
[Standardize Date Format](#standardize-date-format)
[Populate Property Address Data](#populate-property-address-data)
[Breaking out Address into Individual Columns](#breaking-out-address-into-individual-columns)
[Change Y and N to Yes and No](#change-y-and-n-to-yes-and-no)
[Remove Duplicates](#remove-duplicates)
[Delete Unused Columns](#delete-unused-columns)

Standardize Date Format

Standardize Date Format
SELECT saleDateConverted, CONVERT(Date, SaleDate)
FROM PortfolioProject.dbo.NashvilleHousing;

UPDATE NashvilleHousing
SET SaleDate = CONVERT(Date, SaleDate);

If it doesn't Update properly
ALTER TABLE NashvilleHousing ALTER COLUMN SaleDate DATE;

UPDATE NashvilleHousing
SET SaleDateConverted = CONVERT(Date, SaleDate);


Populate Property Address Data

Populate Property Address data
SQL queries for populating missing property addresses go here


Breaking out Address into Individual Columns

Breaking out Address into Individual Columns (Address, City, State)
SQL queries for breaking down address into individual components go here


Change Y and N to Yes and No

Change Y and N to Yes and No in "Sold as Vacant" field
SQL queries for updating "Sold as Vacant" field go here


Remove Duplicates
to Remove Duplicates
SQL queries for removing duplicates go here


Delete Unused Columns
sql
Delete Unused Columns
 SQL queries for deleting unused columns go here

