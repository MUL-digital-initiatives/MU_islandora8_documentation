The office Workbench documentation: https://mjordan.github.io/islandora_workbench_docs/updating_terms/
A specific use case for MU Digital Initiatives is to avoid this Drupal bug: confusing error & behavior when creating a new referenced entity containing parentheses https://www.drupal.org/project/drupal/issues/2924783
Workaround we came up is that whenever we create a new geographical taxonomy term that has parentheses, we use [] instead. Then, we will use Islandora Workbench to update the term. 
Steps: 
  1) export a .csv file from: https://digital.library.missouri.edu/admin/structure/taxonomy_manager/voc/geo_location
  2) identify the terms that need to be updated. Delete all other terms in the csv but the ones that need to be updated
  3) change the colume header tid to term_id, name to term_name. Save the csv. 
  4) prepare a yml file for updating taxonomy terms. 

The config file for update operations looks like this (note the `task` option is 'update'):

```yaml
      task: update_terms
      host: https://digital.library.missouri.edu/
      username: DigitalServices
      password: 
      vocab_id: geo_location
      input_dir: "C:/Users/huying/Documents/islandora_workbench"
      input_csv: Update_terms.csv
      rollback_dir: C:/Users/huying/Documents/islandora_workbench
      update_mode: replace
```
