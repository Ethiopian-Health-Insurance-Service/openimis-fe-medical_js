# openIMIS Frontend Medical reference module
This repository holds the files of the openIMIS Frontend Medical reference module.
It is dedicated to be deployed as a module of [openimis-fe_js](https://github.com/openimis/openimis-fe_js).

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/openimis/openimis-fe-medical_js.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/openimis/openimis-fe-medical_js/alerts/)

## Main Menu Contributions
None

## Other Contributions
None (Administration module providing menu entries to proxied pages for medical items and services)

## Available Contribution Points
None

## Published Components
* `medical.DiagnosisPicker`, auto-suggestion picker that either (`cacheDiagnoses` configuration) cache the diagnoses or debounce search based on user input (GraphQL: `diagnosesStr`)
* `medical.ItemPicker`, auto-suggestion picker that either (`cacheItems` configuration) cache the items or debounce search based on user input (GraphQL: `medicalItemsStr`)
* `medical.ServicePicker`, auto-suggestion picker that either (`cacheServices` configuration) cache the services or debounce search based on user input (GraphQL: `medicalServicesStr`)
* `medical.VisitTypePicker`, constant-based picker, translation keys: `medical.visitType.null`, `medical.visitType.E`,...
* `medical.CareTypePicker`, constant-based picker, translation keys: `medical.careType.null`, `medical.careType.I`,...


## Dispatched Redux Actions
* `MEDICAL_DIAGNOSIS_PICKER_{REQ|RESP|ERR}`: loading diagnoses picker (either cache or ad hoc query)
* `MEDICAL_ITEM_PICKER_{REQ|RESP|ERR}`: loading items picker (either cache or ad hoc query)
* `MEDICAL_SERVICE_PICKER_{REQ|RESP|ERR}`: loading services picker (either cache or ad hoc query)

## Other Modules Listened Redux Actions
None

## Configurations Options
* `debounceTime`: for pickers without cache, debounce time (ms) before triggering the search. Default: `800`
* `cacheDiagnoses`: wherever diagnoses picker caches the diagnoses or not
* `diagnosesMinCharLookup`: if diagnoses picker is not configured to cache diagnoses, minimum number of characters before trigring the search. Default: 2
* `cacheItems`: wherever items picker caches the diagnoses or not (default false, WARNING: when caching, the list is filtered with validity date = today)
* `itemsMinCharLookup`: if items picker is not configured to cache items, minimum number of characters before trigring the search. Default: 2
* `cacheServices`: wherever services picker caches the diagnoses or not (default false, WARNING: when caching, the list is filtered with validity date = today)
* `servicesMinCharLookup`: if services picker is not configured to cache services, minimum number of characters before trigring the search. Default: 2
* `DiagnosisPicker.selectThreshold`: Diagnosis suggestions count threshold under which the AutoSuggestion switch to a SelectInut (drop down list), default: 10
* `ItemPicker.selectThreshold`: Items suggestions count threshold under which the AutoSuggestion switch to a SelectInut (drop down list), default: 10
* `ServicePicker.selectThreshold`: Services suggestions count threshold under which the AutoSuggestion switch to a SelectInut (drop down list), default: 10