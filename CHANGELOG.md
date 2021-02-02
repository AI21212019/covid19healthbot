# Changelog

## 2021-02-02

### Changed

- Updated testing and care advice for pediatric individuals (Age 2 to 17 years) with primary and secondary symptoms of COVID-19
- Updated demographic questions: 
 - Added new question on ZIP code
 - Added two questions on race and ethnicity
 - Revised gender identity question to be more inclusive 
 - Added Down syndrome to the list of COVID-19 high-risk conditions for adults and children


## 2020-12-23

### Changed

- Removed questions 32 and 33 on symptom severity

## 2020-12-17

### Changed

- Reintroduced headache (secondary symptom) in the list of COVID-19 adult symptoms
-	Added a new care message for influenza considerations for symptomatic adults and children
-	Updated the question about exposure with a broader definition of close contact
-	Updated options to reduce quarantine for contacts of persons with SARS-CoV-2 for asymptomatic individuals

## 2020-12-10

### Changed

-	Added a new question about testing status and results
-	Added new care messages that correspond with testing status and results
-	Added a new question about symptom severity
-	Added a new care message for individuals who have been in close contact with someone with confirmed COVID-19
-	Updated the 15 minute rule for close contact with COVID-19
-	Revised Care Messages #5, #8, and #9 to include recommendations on safe practices like washing hands with soap and water
-	Revised Care Message #6 to include additional information for healthcare workers
-	Modified testing messages to recommend testing for asymptomatic individuals who have been exposed to COVID-19


## 2020-09-10
 
### Changed

-	Added pediatric flow for ages 2 to 17 years
-	Includes specific questions for pediatric age groups and settings
- Updated COVID-19 testing and care messages and logic
-	Plain language updates


## 2020-07-15
### Changed

· Updated underlying conditions that increase risk of severe COVID-19 illness.

## 2020-06-08
### Changed
- Updated COVID-19 testing message to include HHS website to locate nearby testing centers.


## 2020-06-05
### Changed
- Removed pediatric flow <18 years old
- Updated exposure question to remove "area where COVID is widespread"
- Updated symptoms question
- Updated COVID-19 testing messages and logic 
- Plain language updates, streamlined decision tree and updated care messages
- Consolidated questions for life threating emergency


## 2020-05-13
### Changed
- Age question answer options are now shown as a dropdown list instead of individual buttons
- If user fails to answer US State question 3x, show message 0 and stop scenario

## 2020-05-08
### Changed
- Updated both non-English scenarios, wrapper and core, to version 58 (latest version)
- Updated localization string spreadsheet to include strings for non-English languages for version 58

## 2020-05-06
### Changed
- Removed custom scenario localization and switched to using Microsoft Health Bot built-in localization tool

### Added
- Localization strings spreadsheet to import into health bot instance for all scenarios

## 2020-05-01
### Changed
- Update to symptoms logic

## 2020-05-01
### Added
Algorithm:
  - Asymptomatic flow 
    - Includes a specific question on healthcare worker use of personal protective equipment
    - New care messages for this flow
  - Question on the quality of the users’ breathing 
  - Messages with information about COVID-19 testing 
  - Age stratification (≥64 and 65+) on care messages
  
Scenarios:
  - Data dictionary and consistent indexing for answer choices
  - Added an "Outcome" block for each path that sends a custom log event with the answers for each question and the corresponding index from the data dictionary

### Changed
Algorithm: 
  -	Consolidated care messages related to seeking immediate medical attention: call 911; go to the emergency department 
  - Updated symptom-related questions 
  -	Updated care messages

Scenarios:
  - Split English and Non-English into two separate scenarios for both the wrapper and core scenario

### Fixed
- State health department website links for Virginia, Rhode Island and Arkansas

## 2020-04-10
### Changed
- Updated localization strings for Chinese, Korean, Spanish and Vietnamese in Core protocol scenario and wrapper scenario

## 2020-04-07
### Added
- "ES-ES" switch statement for localization for Spanish language in Core protocol scenario and wrapper scenario

### Changed
- Change "you (they)" to "you" in location questions in wrapper scenario
- Change "Bluish lips or face" to "Blue-colored lips or face" in wrapper scenario and Core protocol scenario messages

## 2020-04-06
### Added
- Add missing 'Outcome 10' step in non-exposure pathway in Core protocol scenario

### Fixed
- Fix issue in comorbidity checking in exposure pathway in Core protocol scenario that didn't account for whether 'Pregnancy' was listed as an option
- Fix issue in comorbidity checking in non-exposure pathway in Core protocol scenario that used string instead of index of condition

## 2020-04-02
### Added
- Global conversation variable that allows accessing the Core protocol scenario outcome and questions answers in the wrapper scenario

### Changed
- Updates to localization strings in both Core protocol scenario and wrapper scenario

### Fixed
- Fix issue in Core protocol where selecting age: '2-4 years' and "Not experiencing life-threatening symptoms" resulted in an incorrect message outcome

## 2020-03-30
### Added
- Split scenario into two:
  - CDC wrapper scenario, which includes CDC specific questions
  - Core COVID-19 triage protocol scenario
- Split scenario includes initial localization strings for Chinese, Korean, Spanish and Vietnamese
  
### Changed
- All JavaScript expressions that were using a string for checking in scenario blocks, now use index in order to work with localization

### Removed
- Combined wrapper and core scenario

## 2020-03-28
### Changed
- Added logic: if a user fails to answer a question 3 times, show message and ask them to choose an option and restart the self-checker. This applies to all questions with a "Submit" button
- Update comorbidity language (uses algorithm version 51)
- Update decision tree logic (uses algorithm version 51)

## 2020-03-27
### Fixed
- Show 'Pregnancy' in list of comorbidity symptoms for 'Other' gender

## 2020-03-26
### Added
- Initial commit of scenario
