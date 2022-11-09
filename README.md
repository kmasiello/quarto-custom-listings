# A sampling of EJS templates for custom listings in Quarto

My css may not be the most efficient, but it gets the job done. 

## Templates available

1. Featured - makes each entry a button box with highlight and drop shadow effect on hover. Boxes will tile two across.
2. Featured-wide - same as Featured, except it takes the full width of the column.
3. Articles-condensed - shows a summary of articles and allows you to organize them according to specific metadata titles and add custom descriptions
4. Articles-list - makes a pretty list of articles with a hover effect

## Using the templates
Each format has three pieces:

- The custom ejs template, found in the `ejs` directory
- The css associated with this template, found in the `styles` directory
- The usage of the template, found in the YAML of `index.qmd`, e.g., 
    
    ```
    listing: 
    - id: featured-wide
      template: ejs/featured-wide.ejs
      contents:
        - articles/article2
    ```
## Notes
Developed with Quarto version 1.1.251. There are improvements coming in future releases of Quarto to make it easier to feed custom meta data into the templates. For now though, some templates require a custom metadata list (accomplished with a `.yml` file) and some can use the default listing fields. If interested, follow https://github.com/quarto-dev/quarto-cli/issues/3071
