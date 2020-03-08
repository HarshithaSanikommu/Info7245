## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

```
git clone https://github.com/HarshithaSanikommu/Info7245.git

```

### Prerequisites

What things you need to install the software:

```
Python3.5+
Apache Beam
Google Cloud Storage
NLTK
```

### Installing

Run These Commands on the terminal
```
pip3 install apache-beam nltk google-cloud-storage apache-beam[gcp]
```

### Setup For Running in Google Cloud DataFlow
#### Step 1
##### Create a project on Google Cloud Platform #####
To create a new project:
 - Go to the Manage resources page in the Cloud Console.
 - On the Select organization drop-down list at the top of the page, select the organization in which you want to create a project. If    you are a free trial user, skip this step, as this list does not appear.
 - Click Create Project.
 - In the New Project window that appears, enter a project name and select a billing account as applicable.
 - If you want to add the project to a folder, enter the folder name in the Location box.
 - When you're finished entering new project details, click Create.
 
##### Create a bucket: #####
 - Open the Cloud Storage browser in the Google Cloud Console. 
 - Click Create bucket to open the bucket creation form.
 - Enter your bucket information and click Continue to complete each step:
 - Specify a Name, subject to the bucket name requirements.
 - Select a Default storage class for the bucket. The default storage class will be assigned by default to all objects uploaded to the bucket. Next, select a Location where the bucket data will be permanently stored.
 - Select an Access control model to determine how you control access to the bucket's objects.
 - Optionally, you can add bucket labels, set a retention policy, and choose an encryption method. Click Done.
Create 2 folders inside the bucket `temp` and `staging` for creating a temperory and staging location for apache beam to interact with.

#### Step 2
Test If you have adequate access writes to your Bucket by running the example shown <a href='https://googleapis.dev/python/storage/latest/index.html#example-usage'>Here</a>
#### Step 3
Spin up a Google VM Instance <a href='https://console.cloud.google.com/compute/instances'> Here </a> with minimum configuration since DataFlow is a managed service, it handles the resources part.
#### Step 4
> Configure file <a href="https://github.com/HarshithaSanikommu/Caseone/submit.py">`submit.py`</a> from lines 26 to 29 according to your google credentials. Also enter the bucket location in lines 324 to 331 in <a href="https://github.com/HarshithaSanikommu/Caseone/submit.py">`submit.py`</a>
#### Step 5
Once Everything is installed successfully the below command inside the repository folder
```
python3 submit.py
```

## References: ##

● Review the tutorial on Linkedin Learning 
● https://cloud.google.com/dataflow/docs/how-to
● https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3230156 
● https://www.uts.edu.au/sites/default/files/ADG_Cons2015_Loughran%20McDonald%20JE%202011.pdf 
● https://drive.google.com/file/d/15UPaF2xJLSVz8DYuphierz67trCxFLcl/view  

## Libraries and the versions used in this case study: ##
 * anaconda-client==1.7.2
 * anaconda-navigator==1.9.7
 * anaconda-project==0.8.3
 * apache-beam==2.18.0
 * auth==0.5.3
 * beautifulsoup4==4.8.0
 * conda==4.8.2
 * conda-build==3.18.9
 * conda-package-handling==1.6.0
 * conda-verify==3.4.2
 * contextlib2==0.6.0
 * edgar==5.1.9
 * en-core-web-lg==2.2.0
 * en-core-web-sm==2.1.0
 * fastavro==0.21.24
 * gcloud==0.18.3
 * gcsfs==0.6.0
 * google-api-core==1.16.0
 * google-apitools==0.5.28
 * google-auth==1.10.2
 * google-auth-oauthlib==0.4.1
 * google-cloud-bigquery==1.17.1
 * google-cloud-bigtable==1.0.0
 * google-cloud-core==1.2.0
 * google-cloud-dataflow==2.4.0
 * google-cloud-datastore==1.7.4
 * google-cloud-pubsub==1.0.2
 * google-cloud-speech==1.3.1
 * google-clud-storage==1.25.0
 * google-resumable-media==0.5.0
 * googleapis-common-protos==1.51.0
 * grpc-google-iam-v1==0.12.3
 * grpcio==1.26.0
 * html5lib==1.0.1
 * httplib2==0.12.0
 * ipykernel==5.1.2
 * ipython==7.8.0
 * json5==0.8.5
 * jupyter==1.0.0
 * jupyter-client==5.3.3
 * jupyter-console==6.0.0
 * jupyter-core==4.5.0
 * jupyterlab==1.1.4
 * jupyterlab-server==1.0.6
 * nltk==3.4.5
 * notebook==6.0.1
 * numpy==1.17.2
 * oauth2client==3.0.0
 * oauthlib==3.1.0
 * pandas==0.24.2
 * path.py==12.0.1
 * pathlib2==2.3.5
 * py==1.8.0
 * pyarrow==0.15.1
 * requests-oauthlib==1.3.0
 * spacy==2.2.3
 * unicodecsv==0.14.1
 * urllib3==1.24.2
 * virtualenv==16.7.9
 * xlrd==1.2.0
 * XlsxWriter==1.2.1
