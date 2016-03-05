# Angular 1 vs. 2

The goal of this repo is to compare Angular 1 in Javascript with Angular 2 in Typescript by making a directive/component that represents a list of hierarchical select boxes where earlier selections influence later options.  For instance, you might select you city by first selecting your continent, then your country, then optionally your state, and then your city.  These options will be fetched over HTTP.  When you select your continent, only countries in that continent will be shown and so on.

A common test suite will test both applications using the same tests.  A common HTTP backend will serve the options.

## Requirements
* The number of select boxes is not initially known and not constant.  For instance, selecting the United States as a country might produce select boxes for state and city, but selecting Bulgaria might only produce one select box for city.
* If a select box has only one option, it is automatically selected.
* If you change the value of a select box, all subsequent selections are cleared.  For instance, if you select United States-->Illinois-->Chicago and then change United States to Canada, then Illinois and Chicago are removed.
* A seperate HTTP request will be made upon every selection.
