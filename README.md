## 1 - Create pipeline Jenkins job for .NET project

### Install .NET SDK Plugin

1) Go to **Manage Jenkins** -> **Manage Plugins**
2) Select Available plugins and search **.NET SDK Support**, check install and click **Install without restart**

### Add .NET SDK Installation

1) Go to **Manage Jenkins** -> **Global Tool Configuration**
2) Find **.NET SDK** section and click Add **.NET SDK**
3) Add name for .NET SDK installation, check **Install automatically**, choose .NET version, Release, SDK and platform and **Save** changes

### Create Jenkins pipeline job

1) Go to **Jenkins Dashboard** and click **New Item**, enter Item Name and choose **Pipeline**
2) Create Jenkinsfile on Repository and add pipeline code inside
3) In Pipeline section select **Pipeline script from SCM** and choose **Git**
4) Provide Repository URL and Credentials created in previous steps, and select which Branch to build and fill Script path with path to Jenkinsfile on Repository
5) **Save** changes and click **Build now**
