  # config-mgt
  # This is the README file for the config-mgt project.

  ## Description
  This project contains Ansible playbooks for configuring servers in different environments.

  ## Playbooks
  The following playbooks are included in this project:

  - `site.yaml`: This playbook includes the dynamic variables and imports the static assignments for all hosts.
  - `uat-webservers.yaml`: This playbook configures the UAT web servers.
  - `database.yaml`: This playbook configures the database servers.
  - `loadbalancer.yaml`: This playbook configures the load balancers.

  ## Dynamic Variables
  The `env-vars.yaml` playbook contains dynamic variables that are used in the other playbooks. These variables are specific to each environment and should be updated accordingly.

  ## Static Assignments
  The `static-assignments` directory contains YAML files that define the static assignments for each host group. These files should be updated as needed to reflect changes in the infrastructure.

  ## Usage
  To use these playbooks, first update the dynamic variables in `env-vars.yaml` to match your environment. Then, run the `site.yaml` playbook to configure all hosts.

  To configure a specific host group, run the corresponding playbook. For example, to configure the UAT web servers, run the `uat-webservers.yaml` playbook.

  ## Tags
  Each task in the playbooks is tagged with a specific tag. To run only tasks with a specific tag, use the `--tags` option when running the playbook. For example, to run only the tasks tagged with `always`, use the following command:
