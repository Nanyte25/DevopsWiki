# Walkthrough using RHM-OPS Jira Manager script.

This is intended as a quick reference for how we can use the (fh-jira-manager.py) to Create JIRA's on behalf of the Red Hat Mobile Operations Team.

## Location

Firstly you need to make sure you have the following repo cloned onto your machine.

# Github Repos
## Red Hat Mobile (rhm-utils)

No matter where you work in Red Hat Mobile, you might find the following rhm-utils repo useful. This contains a lot of useful scripts and tools for common tasks like checking monitoring dashboards, creating domains, setting domain properties and so on. To access this repo, do the following (and then configure your Bash profile accordingly:

``` 
if [ ! -d ~/repos ]; then mkdir ~/repos; fi
cd ~/repos
git clone git@github.com:rhm-devops/rhm-utils.git
```

This script is located in /rhm-utils/bin and has a corresponding sim link need to be setup.

```
cd ~/.rhm

ln -s $HOME/repos/rhm-utils/conf/fh-jira-templates.json fh-jira-templates.json

```

## Using the fh-jira-manager.py. To see a full list of available command line arguments use the following command.

```
$ ./fh-jira-manager.py -t

fh-jira-manager.py [-h] --action
                          {component-add,component-remove,issue-assign,issue-comment,issue-create,issue-delete,issue-read,issue-update,issue-update-epic,issue-update-sprint,label-add,label-remove,target,template-create}
                          [--server SERVER] [--username USERNAME]
                          [--password PASSWORD] [--project PROJECT]
                          [--parent PARENT] [--summary SUMMARY]
                          [--assignee ASSIGNEE] [--message MESSAGE]
                          [--key KEY] [--description DESCRIPTION]
                          [--issuetype {Bug,Enhancement,Epic,Feature,Sub-task,Task}]
                          [--priority {Blocker,Critical,Major,Minor,Trivial}]
                          [--components COMPONENTS] [--labels LABELS]
                          [--template TEMPLATE] [-v] [-q]
fh-jira-manager.py: error: argument --action is required

```

## Creating a new JIRA using this script.

```
./fh-jira-manager.py --action issue-create --assignee <jira-username> --summary "description of JIRA" --components nameofexistingcomponent 

 e.g NOC Support

```

## Deleting an existing JIRA using this script.

```
./fh-jira-manager.py --action issue-delete --assignee <jira-username> --summary "description of JIRA" --components nameofexistingcomponent 

 e.g NOC Support

```


## Creating a new JIRA with corresponding labels 

```


```

## Generating multiple epics(JIRA'S) and sub-tasks from a JSON template. The scripts has the ability to generate Jira's from reading in a JSON file which will in turn create new EPIC with sub-tasks associated.

```
./fh-jira-manager.py --action template --assignee Jmernin --template test --summary three-ireland -v


The -v show us the verbos output from the command.

```
