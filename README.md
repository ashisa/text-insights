# What is this repository?

This repository contains the script used in the MSDN magazine article titled "From simple text to targeted sentiment analysis with Microsoft Cognitive Services". A description of the scripts are as following -

+ **detectlanguage.sh** - This script used the languages endpoint to detect the language of the input text using the Text Analytics API
+ **keyphrases.sh** - This script detects the key phrases in the given text input using the Text Analytics API
+ **linguistic.sh** - This script send the text to the Linguistic Analysis API and returns the constituency tree, POS Tag and tokens response
+ **sentiment.sh** - This scripts detects the sentiment score of the text record using the Text Analytics API

# How to use these scripts?

These scripts use the Curl command found in most Linux distributions.

You can still use these scripts in Windows 10 by installing the Ubuntu Bash on Windows. For more information on running a Linux subsystem on Windows, please visit this link - https://msdn.microsoft.com/en-us/commandline/wsl/about

You will also need the trial or production subscription keys for the Text Analytics and Linguisitic Analysis Cognitive services. You can obtain the trial keys from the this link - https://azure.microsoft.com/en-in/try/cognitive-services/

Once you are ready with your Linux terminal and the subscription keys for these services, replace "my-trial-key" with your Text Analytics subscription key in the following scripts -

+ detectlanguage.sh
+ keyphrases.shs
+ sentiment.sh

Now, replace the text "my-trial-key" with your Linguistics Analysis API in the following script -

+ liguistics.sh

Once you are done with these changes, you are ready to execute these scripts. Please follow the steps in the article to get the results direcly from the respective services.

# Tips:

If you see diagnostics/debug information being returned from the scripts, please execute them using the following syntax -

```
./detectlanguage.sh 2>/dev/null
```

If you want to see the results in a pretty format, install the awesome command-line JSON processor [**jq**] (https://stedolan.github.io/jq/) and pipe the output to it -

```
./sentiment.sh 2>/dev/null | jq
```



