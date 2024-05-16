# Command line usage tutorial

## Getting started

For the CLI, use the `run.py` script.

```bash
python run.py --model_name gpt4 \
  --data_path https://github.com/pvlib/pvlib-python/issues/1603 \
  --config_file config/default_from_url.yaml \
  --per_instance_cost_limit 2.00 
```

Here, `--per_instance_cost_limit` limits the total inference cost to $2 (default is $3).

!!! tip "All options"
    Run `python run.py --help` to see all available options.

## Running on local repositories

```bash
python run.py --model_name gpt4 \
  --data_path /path/to/my_issue.md \
  --repo_path /path/to/my/local/repo \
  --config_file config/default_from_url.yaml \
  --per_instance_cost_limit 2.00 \
  --apply_patch_locally
```

## Taking actions

* You can have the agent automatically open a PR if the issue has been solved by supplying the `--open_pr`
  flag. Please use this feature responsibly (on your own repositories or after careful consideration).

## More examples