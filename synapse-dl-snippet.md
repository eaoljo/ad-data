# Code snippets to download data from Synapse

Full instructions for programmatic downloads [here](https://help.synapse.org/docs/Downloading-Data-Programmatically.2003796248.html).

You need:
- to register for a username and password on Synapse
- to install the Python package: `pip install synapseclient`

`syn22164713` is a placeholder for the dataset ID on Synapse.

## Python 

```
import synapseclient 
 
syn = synapseclient.Synapse() 
syn.login() 

# Obtain a pointer and download the data 
entity = syn.get(entity='syn22164713' ) 

# Get the path to the local copy of the data file 
filepath = entity.path 
```

## Command line
 
```
synapse get syn22164713  
```
