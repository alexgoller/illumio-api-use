# Illumio Core api-use

Illumio Core api-use will fill three environment variables with the API credentials JSON file contained in the first argument given to api-use.

The 3 variables are

* ILO_API_KEY
* ILO_API_KEY_ID
* ILO_API_TOKEN

# Usage

Create a directory with your keys and be sure that only you have access to it and it's on a encrypted volume.
Then just use the below to quickly set the variables and change between different API keys.

    source api-use <file with API key generated by Illumio Core PCE>

Especially useful for playing with the API and using curl like this:

    curl -X GET -u $ILO_API_KEY:$ILO_API_TOKEN "https://my-pce:8443/api/v2/orgs/1/workloads"
