# fivethirtyeight 0.6.2.9000

*


# fivethirtyeight 0.6.2

* Fixed bugs in `tame.Rmd` vignettes
* Fixed url's



# fivethirtyeight 0.6.1

* Changed all vignette code to no longer dynamically read data off the web, per
CRAN policy on internet access. All relevant outputs and figures are now hard
coded.



# fivethirtyeight 0.6.0

* Wide to long/tidy data format in data examples now done with
`tidyr::pivot_longer()` instead of `tidyr::gather()`
* Added new data sets:
    + By Natalia Iannucci @niannucci: `media_mentions_cable`, `media_mentions_online`
    + By Marium Tapal @mariumtapal: `state_index`, `state_words`
    + By Lizette Carpenter @lcarpenter20: `cabinet_turnover`
    + By Irene Ryan @ireneryan: `castle_solutions`, `castle_solutions_2`, `castle_solutions_3`
    + By Alina Barylsky @abarylsky: `dem_candidates`
    + By Rana Gahwagy @ranawg:`quasi_winshares`
    + By Danica Miguel @danicamiguel: `raptor_by_player`,`raptor_by_team`
    + By Sunni Raleigh @sunniraleigh: `wwc_2019_forecasts`, `wwc_2019_matches`
    + By Anna Ballou @aballou16: `foul_balls` 
    + By Jane Bang @Janebang: `nba_draymond`
    + By Jordan Moody @jormacmoo: `fight_songs`
    + By Kara Van Allen @kvanallen: `nba_elo`, `nba_elo_latest`
    + By Jessica Keast @jkeast: `nba_all_elo`
    + By Fatima Keita @fatimak98: `impeachment_polls`
* Marium Tapal @mariumtapal created
[`fivethirtyeightdata`](https://github.com/fivethirtyeightdata) package using
`drat` package to store large files. This is due to CRAN package size
restrictions:
    + When installing `fivethirtyeight` user is now prompted to install
    `fivethirtyeightdata`
    + Moved all user-contributed vignettes to `fivethirtyeightdata` to keep
    package size down
    + Moved the following large datasets to `fivethirtyeightdata`  
    ```
    [1] "castle_solutions"           "castle_solutions_2"
    [3] "castle_solutions_3"         "comic_characters"
    [5] "goose"                      "house_district_forecast"
    [7] "mayweather_mcgregor_tweets" "mlb_elo"
    [9] "nba_all_elo"                "nba_carmelo"
    [11] "nba_elo"                    "nfl_elo"
    [13] "quasi_winshares"            "raptor_by_player"
    [15] "raptor_by_team"             "ratings"
    [17] "senators"                   "spi_matches"
    [19] "twitter_presidents"
    ```



# fivethirtyeight 0.5.0

* Added vignette corresponding to Technology Innovations in Statistics Education [paper](https://escholarship.org/uc/item/0rx1231m#main)
* Removed tidyverse from `DESCRIPTION` Depends, Imports, or Suggests fields
* Added `state_info` data frame of state name, abbreviation, US census division/region
* Added `state_abbrev` variable to `hate_crimes` dataset so that 
users can plot state abbreviations via `geom_text(aes(label = state_abbrev))`
instead of using less informative `geom_point()`
* Given CRAN package size restrictions, the following datasets only consist of a preview of the first 10 rows of the entire dataset: `comic_characters`, `goose`, `house_district_forecast`, `mlb_elo`, `nba_carmelo`, `nfl_elo`, `ratings`, `senators`, and `spi_matches`. Code to load the entire dataset are provided in the respective help file examples.
* Added new data sets:
    + By Starry Zhou: `august_senate_polls`, `cabinet_turnover`, 
    `elasticity_by_district`, `elasticity_by_state`, `endorsements_2020`, 
    `forecast_results_2018`, `governor_national_forecast`, `governor_state_forecast`,
    `house_district_forecast`, `house_national_forecast`, `masculinity_survey`, 
    `mueller_approval_polls`, `ncaa_w_bball_tourney`, `partisan_lean_district`, 
    `partisan_lean_state`, `russia_investigation`, `senate_national_forecast`, 
    `senate_seat_forecast`, `trump_lawsuits`, 
    
    

# fivethirtyeight 0.4.0

* Package website now at <https://fivethirtyeight-r.netlify.app/>
* Added new data sets:
    + By Meredith Manley: `ahca_polls`, `bachelorette`, `candy_rankings`, 
    `chess_transfers`, `generic_polllist`, `generic_topline`, 
    `mayweather_mcgregor_tweets`, `mlb_elo`, `ratings`, `spi_global_rankings`, 
    `spi_matches`.
    + By Maggie Shea: `google_trends`, `nba_carmelo`, `nfl_elo`,
    `nfl_fandom_google`, `nfl_fandom_surveymonkey`, `mediacloud_hurricanes`,
    `mediacloud_states`, `mediacloud_online_news`, `mediacloud_trump`,
    `riddler_pick_lowest`, `sandy_311`, `senators`, `tv_hurricanes`,
    `tv_hurricanes_by_network`, `tv_states`, `trump_approval_poll`,
    `trump_approval_trend`, `trumpworld_issues`,`trumpworld_polls`,
    `twitter_presidents`, `undefeated`
* Note for now `mayweather_mcgregor_tweets`, `mlb_elo`, `nba_carmelo`,
`nfl_elo`, `senators`, only include the first 10 rows of the data because of R
package file size restrictions (< 5MB tarballs); code to download/process the
entire dataset are included in help files. We hope to include full versions of
these datasets in v0.5.0 of package using the `drat` package.
* Converted all ordinal categorical variables to `factor(..., ordered = TRUE)`.
Ex: `bechdel$clean_test`
* Vignette notes:
    + Added a vignette that has a link to all user-contributed vignettes, which 
    are only available on development version of package and on GitHub due to 
    CRAN package size restrictions.
    + For all datasets that have a user contributed vignette, add a link to it 
    in the corresponding help/roxygen code file.
* Added `CITATION`



# fivethirtyeight 0.3.0

* Added new and missing data sets: `riddler_castles2`, `antiquities_act`, `goose`,
`tenth_circuit`
* Added more crowd-sourced vignettes: `bob_ross.Rmd`, `tarantino_swears.Rmd`
* Only main and `bechdel` vignettes included in package b/c of CRAN package size
restrictions. Other crowd-sourced analysis vignettes still available
    + In development version
    + On package website under "Articles" <https://fivethirtyeight-r.netlify.app/>
* Other minor changes:
    + Fixed levels in `bechdel$clean_test` and `bechdel$test` to match
    hierarchical nature of test



# fivethirtyeight 0.2.0

* Added new and missing data sets up through February 28, 2017: 
`college_grad_students`, `college_recent_grads`, `cousin_marriage`, 
`hate_crimes`, `pres_2016_trail`, `riddler_castles`
* Added first crowd-sourced vignettes: `comics_gender`, `NBA`, `trump_twitter`
* Added global help file for package: `?fivethirtyeight` with complete instructions
* Started adding `@examples` code in help files to convert to tidy data format
so that data plays nice with tidyverse tools.
* Other minor changes:
    + [Changed to SVG travis logo](https://github.com/rudeboybert/fivethirtyeight/pull/1)
    + [Removed explicit loading of data in vignette](https://github.com/rudeboybert/fivethirtyeight/pull/2)
    + `fivethirtyeight` main vignette reads data set list from Google Sheets
    master document [https://goo.gl/OT8iHa](https://goo.gl/OT8iHa)



# fivethirtyeight 0.1.0

* Included all data sets as of late December 2016. `love-actually` being the latest
* Included one code example as a Vignette: bechdel
