# (PART) Data Tables {.unnumbered}

# gt Example 1 {#dt-eg1}

Here is an example on how to add a title and subtitle using gt 


```r
library(tidyverse)
library(gt)

head(mtcars) %>%
  gt()  %>%
  tab_header(
    title = md("Just a **title**"),
    subtitle = md("Just a `subtitle`")
  )
```

```{=html}
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#wmusnlzrzr .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#wmusnlzrzr .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#wmusnlzrzr .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#wmusnlzrzr .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 4px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#wmusnlzrzr .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#wmusnlzrzr .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#wmusnlzrzr .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#wmusnlzrzr .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#wmusnlzrzr .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#wmusnlzrzr .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#wmusnlzrzr .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#wmusnlzrzr .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#wmusnlzrzr .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#wmusnlzrzr .gt_from_md > :first-child {
  margin-top: 0;
}

#wmusnlzrzr .gt_from_md > :last-child {
  margin-bottom: 0;
}

#wmusnlzrzr .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#wmusnlzrzr .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#wmusnlzrzr .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#wmusnlzrzr .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#wmusnlzrzr .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#wmusnlzrzr .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#wmusnlzrzr .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#wmusnlzrzr .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#wmusnlzrzr .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#wmusnlzrzr .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#wmusnlzrzr .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#wmusnlzrzr .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#wmusnlzrzr .gt_left {
  text-align: left;
}

#wmusnlzrzr .gt_center {
  text-align: center;
}

#wmusnlzrzr .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#wmusnlzrzr .gt_font_normal {
  font-weight: normal;
}

#wmusnlzrzr .gt_font_bold {
  font-weight: bold;
}

#wmusnlzrzr .gt_font_italic {
  font-style: italic;
}

#wmusnlzrzr .gt_super {
  font-size: 65%;
}

#wmusnlzrzr .gt_footnote_marks {
  font-style: italic;
  font-size: 65%;
}
</style>
<div id="wmusnlzrzr" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;"><table class="gt_table">
  <thead class="gt_header">
    <tr>
      <th colspan="11" class="gt_heading gt_title gt_font_normal" style>Just a <strong>title</strong></th>
    </tr>
    <tr>
      <th colspan="11" class="gt_heading gt_subtitle gt_font_normal gt_bottom_border" style>Just a <code>subtitle</code></th>
    </tr>
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">mpg</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">cyl</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">disp</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">hp</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">drat</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">wt</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">qsec</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">vs</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">am</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">gear</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1">carb</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr>
      <td class="gt_row gt_right">21.0</td>
      <td class="gt_row gt_right">6</td>
      <td class="gt_row gt_right">160</td>
      <td class="gt_row gt_right">110</td>
      <td class="gt_row gt_right">3.90</td>
      <td class="gt_row gt_right">2.620</td>
      <td class="gt_row gt_right">16.46</td>
      <td class="gt_row gt_right">0</td>
      <td class="gt_row gt_right">1</td>
      <td class="gt_row gt_right">4</td>
      <td class="gt_row gt_right">4</td>
    </tr>
    <tr>
      <td class="gt_row gt_right">21.0</td>
      <td class="gt_row gt_right">6</td>
      <td class="gt_row gt_right">160</td>
      <td class="gt_row gt_right">110</td>
      <td class="gt_row gt_right">3.90</td>
      <td class="gt_row gt_right">2.875</td>
      <td class="gt_row gt_right">17.02</td>
      <td class="gt_row gt_right">0</td>
      <td class="gt_row gt_right">1</td>
      <td class="gt_row gt_right">4</td>
      <td class="gt_row gt_right">4</td>
    </tr>
    <tr>
      <td class="gt_row gt_right">22.8</td>
      <td class="gt_row gt_right">4</td>
      <td class="gt_row gt_right">108</td>
      <td class="gt_row gt_right">93</td>
      <td class="gt_row gt_right">3.85</td>
      <td class="gt_row gt_right">2.320</td>
      <td class="gt_row gt_right">18.61</td>
      <td class="gt_row gt_right">1</td>
      <td class="gt_row gt_right">1</td>
      <td class="gt_row gt_right">4</td>
      <td class="gt_row gt_right">1</td>
    </tr>
    <tr>
      <td class="gt_row gt_right">21.4</td>
      <td class="gt_row gt_right">6</td>
      <td class="gt_row gt_right">258</td>
      <td class="gt_row gt_right">110</td>
      <td class="gt_row gt_right">3.08</td>
      <td class="gt_row gt_right">3.215</td>
      <td class="gt_row gt_right">19.44</td>
      <td class="gt_row gt_right">1</td>
      <td class="gt_row gt_right">0</td>
      <td class="gt_row gt_right">3</td>
      <td class="gt_row gt_right">1</td>
    </tr>
    <tr>
      <td class="gt_row gt_right">18.7</td>
      <td class="gt_row gt_right">8</td>
      <td class="gt_row gt_right">360</td>
      <td class="gt_row gt_right">175</td>
      <td class="gt_row gt_right">3.15</td>
      <td class="gt_row gt_right">3.440</td>
      <td class="gt_row gt_right">17.02</td>
      <td class="gt_row gt_right">0</td>
      <td class="gt_row gt_right">0</td>
      <td class="gt_row gt_right">3</td>
      <td class="gt_row gt_right">2</td>
    </tr>
    <tr>
      <td class="gt_row gt_right">18.1</td>
      <td class="gt_row gt_right">6</td>
      <td class="gt_row gt_right">225</td>
      <td class="gt_row gt_right">105</td>
      <td class="gt_row gt_right">2.76</td>
      <td class="gt_row gt_right">3.460</td>
      <td class="gt_row gt_right">20.22</td>
      <td class="gt_row gt_right">1</td>
      <td class="gt_row gt_right">0</td>
      <td class="gt_row gt_right">3</td>
      <td class="gt_row gt_right">1</td>
    </tr>
  </tbody>
  
  
</table></div>
```
