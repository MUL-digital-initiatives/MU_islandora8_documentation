The config file for update operations looks like this (note the `task` option is 'update'):

```yaml
      task: update
      host: https://digital.library.missouri.edu/
      username: DigitalServices
      password: 6gJ^p?gq^n1=77Uw,eME
      input_dir: C:\Users\huying\Documents\islandora_workbench
      input_csv: Update_rights.csv
      rollback_dir: C:\Users\huying\Documents\islandora_workbench
      timestamp_rollback: true
      rollback_file_include_node_info: true
```
Always run a --check before updating any metadata. This is how I use Anaconda prompt to run Workbench since I don't have native python environment.
<img width="1104" height="373" alt="image" src="https://github.com/user-attachments/assets/639d9854-edd6-4eb2-b999-5ff0ec907690" />
