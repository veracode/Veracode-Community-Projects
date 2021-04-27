# Veracode Community Open Source Projects

A collection of useful open source projects that integrate with the Veracode APIs to automate scanning, results retrieval and other tasks.

These projects are community contributed and not supported by Veracode. For a list of supported projects, please see the listing of projects on [Veracode.com](https://www.veracode.com/integrations).

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Contents**

- [Automating common Veracode Platform tasks](#automating-common-veracode-platform-tasks)
- [Developer tools](#developer-tools)
  - [CI/CD](#cicd)
  - [Build tools](#build-tools)
  - [IDEs](#ides)
  - [API testing tools](#api-testing-tools)
  - [Other](#other)
- [Pipeline Scan projects](#pipeline-scan-projects)
- [Dynamic Analysis projects](#dynamic-analysis-projects)
- [Results collection and display](#results-collection-and-display)
- [Application vulnerability correlation](#application-vulnerability-correlation)
- [HMAC Signing libraries](#hmac-signing-libraries)
- [API wrappers](#api-wrappers)
- [Other integrations](#other-integrations)
- [Secure coding examples](#secure-coding-examples)
- [Insecure applications](#insecure-applications)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Automating common Veracode Platform tasks

- [Veracode_Delete_Sandbox](https://github.com/christyson/veracode_delete_sandbox) ([Christyson](https://github.com/christyson/)) - A simple example script to delete a Sandbox if it exists in a Veracode application profile and you have the appropriate permissions.

- [Check Build Status](https://github.com/christyson/check_build_status) ([Christyson](https://github.com/christyson/)) - Script to check if an application profile in Veracode has a build running currently.

- [Veracode API Credentials Expiry](https://github.com/christyson/veracode-python-api_credentials_expiry-example) ([Christyson](https://github.com/christyson/veracode-python-api_credentials_expiry-example)) - A simple example to get the exiration dates of api credentials for your users.

- [VcodeAutoMitigate](https://github.com/brian1917/vcodeAutoMitigate) ([Brian1917](https://github.com/brian1917/)) - Command line app that mitigates flaws in Veracode based on CWE, scan type, and specific text in the description.

- [VcodeMitigationExpire](https://github.com/brian1917/vcodeMitigationExpire) ([Brian1917](https://github.com/brian1917/)) - Utility designed to be run on a regular cadence (e.g., weekly cron job) to expire mitigations. The types of mitigations, expiration references, and other settings are controlled in a JSON config file.

- [Veracode Break the Build by Severity](https://github.com/christyson/Veracode-Break-The-Build-By-Severity) ([Christyson](https://github.com/christyson/)) - This project contains three python scripts useful for working with Veracode projects in a build pipeline to break the build if any findings of a given severity or higher are found.

- [Veracode Mitigation Copier](https://github.com/tjarrettveracode/veracode-mitigation-copier) ([Tjarrettveracode](https://github.com/tjarrettveracode/)) - Copies mitigations from one Veracode profile to another if it's the same flaw based on the following flaw attributes: issueid, cweid, type, sourcefile, and line. The script will copy all proposed and accepted mitigations for the flaw. The script will skip a flaw in the copy_to build if it already has an accepted mitigation.

- [Veracode BCA Builder](https://github.com/brian1917/veracode-bca-builder) ([Brian1917](https://github.com/brian1917/)) - Shell script to generate the BCA package to scan an iOS app.

- [Veracode Offboard](https://github.com/tjarrettveracode/veracode-offboard) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - Deactivates a provided list of users on the Veracode Platform.

- [Veracode PDF Reports](https://github.com/jphillips-vc/veracode-pdf-reports) ([Jphillips-vc](https://github.com/jphillips-vc)) - Pulls latest PDF reports from Veracode for recent Static and Dynamic scans.

- [Veracode Policy Examples](https://github.com/tjarrettveracode/veracode-policy-examples) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - A collection of example application security "policies as code" that can be added to your Veracode organization account.

- [Veracode Sandbox Mitigated Unique Findings](https://github.com/ctcampbell/veracode-sandbox-mitigated-unique-findings) ([Ctcampbell](https://github.com/ctcampbell)) - This script will pull all open findings across all sandboxes for all applications and calculate which mitigated (proposed, accepted, or rejected) findings only exist in a single sandbox, and therefore may be deleted when the sandbox is deleted.

- [Veracode Scan Counts](https://github.com/tjarrettveracode/veracode-scan-counts) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - Identify Veracode application profiles with one or more static scans in an incomplete state.

- [Veracode User Bulk Role Assign](https://github.com/tjarrettveracode/veracode-user-bulk-role-assign) ([Tjarrettveracode](https://github.com/tjarrettveracode/)) - Uses the Veracode Identity API to add roles (Security Labs User, Greenlight IDE User, or eLearning) to existing users.

- [Veracode Workspace Auto Create](https://github.com/tjarrettveracode/veracode-workspace-auto-create) ([Tjarrettveracode](https://github.com/tjarrettveracode/)) - Uses the Veracode Agent Based Scan API and other Veracode REST APIs to automatically create a workspace for application profiles in a Veracode organization.

## Developer tools

### CI/CD

- [Bamboo](https://gitlab.com/buzzcode/Bamboo-Veracode) ([Buzzcode](https://gitlab.com/buzzcode/)) - full featured Bamboo plugin including configuration UI, wait for scan to complete, and "break the build" functionality

- [Bamboo/Jira](https://github.com/buildcom/VeracodeAtlassianPlugin) ([Buildcom](https://github.com/buildcom/)) - provides a pair of simple plugins for upload and results handling from within Bamboo, and a lightweight script to create Jira issues (archived project)

- [Bash/CircleCI](https://github.com/unregistered436/veracode-integrations/tree/master/shell-script) ([Unregistered436](https://github.com/unregistered436)) - Veracode Upload and Scan Bash Script, originally written for CircleCI but can be used for any build system that can run a shell script in bash.

- [Bitrise-step-veracode-scan](https://github.com/psoladoye-geotab/bitrise-step-veracode-scan) ([Psoladoye-geotab](https://github.com/psoladoye-geotab/)) - add Veracode scanning to Bitrise CI.

- [CircleCI](https://github.com/ctcircleci/Verademo/blob/master/.circleci/config.yml) ([ctcircleci](https://github.com/ctcircleci)) - Example configurations for building a project with Maven, then executing policy scan, agent-based SCA, and pipeline scan in a CircleCI pipeline.

- [CircleCI](https://github.com/buzzcode/NodeGoat/blob/master/.circleci/config.yml) ([buzzcode](https://github.com/buzzcode)) - Example configuration for zipping a project, then executing policy scan, agent-based SCA, and pipeline scan in a CircleCI pipeline.

- [ConcourseCI, Gitlab, Travis](https://github.com/ctcampbell/veracode-ci-examples) ([Ctcampbell](https://github.com/ctcampbell)) - Example configurations for integrating Veracode scanning in various continuous integration systems.

- [Concourse (Veracode-Resource)](https://github.com/cardinal-health/veracode-resource) ([Cardinal Health](https://github.com/cardinal-health)) - A concourse resource-type to allow publishing and retrieving scan results from Veracode.

- [easy_sast](https://github.com/seisollc/easy_sast) - A [docker container](https://hub.docker.com/r/seiso/easy_sast) for use in CI pipelines which integrates with Veracode's static analysis tool.

- [Jenkins (Jenkins Shell)](https://github.com/ian-c-leonard/veracode_jenkins_shell) ([Ian C Leonard](https://github.com/ian-c-leonard)) - unofficial Veracode shell integration for Jenkins Freestyle projects.

- [Unofficial Veracode Pipeline Scan](https://github.com/ctcampbell/unofficial-veracode-pipeline-scan) ([Ctcampbell](https://github.com/ctcampbell/)) - NPM package for Veracode Pipeline Scan API.

- [Veracode Azure YML Samples](https://github.com/Clintpollock/VeracodeAzureYMLSamples/) ([Clintpollock](https://github.com/Clintpollock)) - Samples of Azure YML files that work with Veracode scanning

- [veracode-badges](https://github.com/Lerer/veracode-badge) ([Lerer](https://github.com/Lerer/)) - produces badges for READMEs and other artifact repositories showing the status of Veracode policy scans.

- [Veracode Community SAST Azure DevOps Extension](https://github.com/MetLife/VeracodeCommunitySAST) ([MetLife](https://github.com/MetLife/)) - Seamlessly integrate Veracode SAST scans with Azure DevOps build pipelines (using Pipeline Scan).

- [Veracode Community SCA Azure DevOps Extension](https://github.com/MetLife/VeracodeCommunitySCA) ([MetLife](https://github.com/MetLife/VeracodeCommunitySCA)) - Seamlessly integrate Veracode Agent-Based SCA scans with Azure DevOps build or release pipelines.

- [Veracode Dynamic Analysis Azure Sample](https://github.com/jphillips-vc/Veracode-Dynamic-Analysis-Azure-Example) ([Jphillips-vc](https://github.com/jphillips-vc/)) - Veracode Dynamic Analysis Azure Sample including script based authentication, and ISM configuration.

- [Veracode Flaw Importer](https://github.com/julz0815/veracode_flaw_importer) ([Julz0815](https://github.com/julz0815/)) - GitHub Action to import static policy findings to GitHub Security Code Scanning Alerts.

- [Veracode for Azure DevOps Pipelines](https://github.com/zoekdestep/veracode-ado-pipelines) ([zoekdestep](https://github.com/zoekdestep/)) - Yaml files to get started with Veracode on Azure DevOps. Accompanies this [blog post](https://community.veracode.com/s/blog/user-story-how-we-set-up-veracode-in-a-large-azure-project-MCT4HNONEE55CIFA6O3ULXNUW2BI).

- [veracode-scripts](https://gitlab.com/aszaryk/veracode-scripts) - Various example scripts for Jenkins and GitLab pipelines, including both static and dynamic examples.

- [veracode-serverless-webhooks](https://github.com/Lerer/serverless-veracode-webhooks) ([Lerer](https://github.com/Lerer)) - enables Veracode customers who want to use the Veracode Upload-and-Scan Static and SCA (not the Pipeline or the IDE scans) and get updates back in an asynchronous manner.

- [XebiaLabs Release Veracode Plugin](https://github.com/xebialabs-community/xlr-veracode-plugin) ([XebiaLabs-Community](https://github.com/xebialabs-community)) - XL Release for Veracode test automation.

### Build tools

- [Gradle](https://github.com/calgaryscientific/veracode-gradle-plugin) ([CalgaryScientific](https://github.com/calgaryscientific), based on [Kctang](https://github.com/kctang/)) - Set of Gradle tasks, usable either as a command line submission tool or integrated as part of a continuous integration build process, to perform Veracode submission for applications and scan results for flaws.

- [Sbt-veracode](https://github.com/sullis/sbt-veracode) ([Sullis](https://github.com/sullis/)) - sbt plugin for Veracode.

### IDEs

- [VSCode-Veracode](https://gitlab.com/buzzcode/VSCode-Veracode) ([Buzzcode](https://gitlab.com/buzzcode/VSCode-Veracode)) - a plugin for Visual Studio Code that enables integration with Veracode Static Analysis. Currently, this only supports flaw download, but will be enhanced to support upload as well in the future.

- [vsccode-veracode-sca](https://github.com/Lerer/vscode-veracode-sca) ([Lerer](https://github.com/Lerer/)) - A very simple plugin for Veracode SCA to get agent-base SCA results into VSCode IDE.

- [unofficial-vs-code-veracode-pipeline-scan](https://github.com/ctcampbell/unofficial-vs-code-veracode-pipeline-scan) ([Ctcampbell](https://github.com/ctcampbell/)) - Scan an app with Veracode Pipeline Scan, and load results from a Veracode Pipeline Scan.

### API testing tools

- [Insomnia](https://github.com/ctcampbell/insomnia-plugin-veracode-hmac) ([Ctcampbell](https://github.com/ctcampbell/)) - Adds an HMAC authentication header to Veracode API requests in Insomnia.

- [Postman pre-request authentication header](https://gist.github.com/ctcampbell/c82d895b0940c08408fb1800aa6718b0) ([Ctcampbell](https://github.com/ctcampbell/)) - Postman pre-request to add Veracode HMAC header.

### Other

- [Ansible](https://github.com/telusdigital/ansible-veracode-scanner) ([Telus Digital](https://github.com/telusdigital)) - allows uploading and scanning with Veracode from Ansible, with an option to send results to a Slack channel

- [Flowdock](https://github.com/brian1917/vcodeFlowdockNotifier) ([Brian1917](https://github.com/brian1917/)) - Utility designed to be run in a build process after a Veracode scan to notify a Flowdock flow that the scan completed. Optional to include policy compliance info in notification.

- [PowerShell](https://github.com/unregistered436/veracode-integrations/tree/master/powershell) ([Unregistered436](https://github.com/unregistered436)) - PowerShell script for pushing binaries to Veracode using Java API.

- [Slack](https://github.com/ctcampbell/veracode-slack-slash-command) ([Ctcampbell](https://github.com/ctcampbell)) - AWS Lambda commands that provide the ability to access Veracode application and build information from Slack.

- [SonarQube](https://gitlab.com/buzzcode/SonarQube-Veracode) ([Buzzcode](https://gitlab.com/buzzcode)) - Unofficial Veracode plugin for SonarQube.

- [Veracode QuickScan](https://github.com/relaxnow/veracode-quick-scan) ([relaxnow](https://github.com/relaxnow)) - PHP example of how to connect to the APIs, scan a couple of files and get results.

- [veracode-tools](https://github.com/ctcampbell/veracode-tools) ([Ctcampbell](https://github.com/ctcampbell)) - Docker image with all Veracode tools pre-installed.

- [Veracode Upload and Scan Shell Script](https://github.com/christyson/Veracode-Upload-and-Scan-Shell-Script) ([Christyson](https://github.com/christyson/)) - A shell script to upload and scan a application (zip or war etc.) and create the application if necessary. Uses Curl and hmac headers.

## Pipeline Scan projects

- [Pipeline2DetailedReport](https://github.com/jphillips-vc/pipeline2detailedreport) ([JPhillips-vc](https://github.com/jphillips-vc/)) - translate Veracode Pipeline Scan results into DetailedReport XML format, allowing you to import them into an IDE plugin for remediation.

- [Pipeline-To-Issues](https://github.com/buzzcode/pipeline-to-issues) ([Buzzcode](https://github.com/buzzcode/)) - Import Veracode Pipeline scan results to GitHub issues.

- [veracode-pipeline-PR-comment](https://github.com/Lerer/veracode-pipeline-PR-comment) ([Lerer](https://github.com/Lerer/veracode-pipeline-PR-comment)) - Sends output of Pipeline Scan to a comment on a pull request.

## Dynamic Analysis projects

- [Dynamic Scan and Wait for Result](https://github.com/christyson/dynamic-scan-and-wait-for-result) ([Christyson](https://github.com/christyson/)) - Extends the Java API Wrapper to provide "break the build" style scanning. Includes instructions on how to integrate this workflow into Jenkins.

- [veracode-da-reset-scheduler](https://github.com/dennismedeiros/veracode-da-reset-recheduler) ([dennismedeiros](https://github.com/dennismedeiros)) - Resets all recurrent scheduled analysis jobs configured for one year that have expired.

- [Veracode Dynamic Analysis Examples](https://github.com/anon-veracoder/veracode-dynamic-analysis-api-examples) ([anon-veracoder](https://github.com/anon-veracoder)) - Dynamic Analysis API Examples.  Currently includes example code for using the Scanner Variables feature, where credentials can be defined and updated at the account level, and referenced in Selenium login scripts.

## Results collection and display

- [Excel (XLS)](https://github.com/Komiblanka/Veracode2xls), [(XLSX)](https://github.com/Komiblanka/Veracode2xlsx) ([Komiblanka](https://github.com/Komiblanka/))- Python scripts to format Veracode XML results into Excel workbook formats for easier human consumption.

- [Hygieia](https://github.com/mickfeech/hygieia_veracode_collector) ([Mickfeech](https://github.com/mickfeech/)) - Veracode scan collector and parser for the [Hygieia dashboard](https://github.com/Hygieia/ExecDashboard).

- [JupiterOne](https://github.com/JupiterOne/jupiter-integration-veracode) ([JupiterOne](https://github.com/JupiterOne/)) - A JupiterOne managed integration for Veracode.

- [JupiterOne Graph Veracode](https://github.com/JupiterOne/graph-veracode) ([JupiterOne](https://github.com/JupiterOne/)) - A graph conversion tool for Veracode.

- [SCA Extractor](https://github.com/brian1917/vcodeSCAExtractor) ([Brian1917](https://github.com/brian1917)) - Creates a CSV file with open source vulnerability (SCA) findings for all builds in the input file.

- [Stats](https://github.com/ctcampbell/veracode-stats) ([Ctcampbell](https://github.com/ctcampbell)) - Summary statistics for a Veracode account on the command line.

- [VeraData](https://github.com/sebcoles/VeraData) ([Seb Coles](https://github.com/sebcoles)) - Console application that will retrieve data (all scans, flaws, mitigations etc) for a given AppId and store the results in a relational schema (only supports MSSQL Server currently) ready for plugging your favourite BI tool into!

- [VeraCustomTriage](https://github.com/sebcoles/VeraCustomTriage) ([Seb Coles](https://github.com/sebcoles)) - App that generates a .xlsx remediation plan from a set of scan results augmented with text from JSON configuration files. Custom text is added when flaw criteria is met (such as a CWE ID, module name, file or line number). This allows custom text such as internal workflows, wiki links, training, code snippets, 2nd party information or other languages into the auto generated remediation plan. Enables app sec teams to triage large volumes of flaws quickly whilst sharing a core advice repository in code.

- [Veracode Report Converter (CSV)](https://github.com/dipsylala/VeracodeReportConverter-Windows) ([Dipsylala](https://github.com/dipsylala/)) - .NET Framework utility to extract useful data from Detailed Report XML file into CSV format

- [Veracode Report Converter - Portable (CSV)](https://github.com/dipsylala/VeracodeReportConverter-Portable) ([Dipsylala](https://github.com/dipsylala/)) - .NET Core utility to extract useful data from Detailed Report XML file into CSV format

- [Veracode - Gitlab SCA results report generation](https://gitlab.com/julz0815/scaresultsreport) ([julz0815](https://gitlab.com/julz0815/)) - Rewrites Veracode's Agent Based SCA json results in Gitlab readable report format in order to display results as dependency scanning on the pipeline run

- [veracode-to-csv](https://github.com/ctcampbell/veracode-to-csv) ([Ctcampbell](https://github.com/ctcampbell)) - This script outputs one CSV file per scan per application profile visible in a Veracode platform account. The output can be imported into  Splunk for further analysis.

- [VCCLI](https://github.com/michaelhorty/VCCLI) ([Michaelhorty](https://github.com/michaelhorty)) - Veracode AST and Security Labs utility in .NET Core.

## Application vulnerability correlation

- [DefectDojo](https://github.com/DefectDojo/django-DefectDojo) - DefectDojo is an open-source application vulnerability correlation and security orchestration application. DefectDojo supports importing Veracode results.

- [Veracode Archer](https://github.com/veracode/veracode-archer) - Script to export a Veracode Archer report file to disk. Usage: set on a timer and run daily or weekly, then import the results into RSA Archer.

## HMAC Signing libraries

Projects in this category implement HMAC digest signing, which is required to use Veracode APIs that use a [Veracode ID and Key](https://help.veracode.com/reader/lsoDk5r2cv~YrwLQSI7lfw/Z70twkx761Oc2RjWUDAWFA). Also see the Postman and Insomnia examples in [API Testing Tools](#api-testing-tools).

- [auth.js](https://gist.github.com/ThibaudLopez/fe1baeaa4461cbf0bfa8fd258ff43243) - Veracode custom HMAC request signing algorithm (used for API authorization), written in JavaScript -- uses Web Crypto API instead of the Node Crypto library

- [PythonHMAC](https://github.com/veracode/veracode-python-hmac-example) - simple example of usage of the Veracode API signing library provided in the Veracode Help Center

- [NodeJS](https://gist.github.com/mrpinghe/f44479f2270ea36bf3b7cc958cc76cc0) - NodeJS lib, written in JavaScript, to generate authorization header with Veracode API Key and ID. Sample usage in the comment of the gist

- [vcodeHMAC](https://github.com/brian1917/vcodeHMAC) ([Brian1917](https://github.com/brian1917/)) - Go package that creates an authorization header using Veracode API Key and ID.

- [vcodeHMAC-CLI](https://github.com/brian1917/vcodeHMAC-CLI) ([Brian1917](https://github.com/brian1917/)) - CLI tool to generate an authorization header for Veracode APIs using API ID and Key. Given an HTTP method and URL, and the location of your Veracode API credentials file, you will get the value of an Authorization header printed out for piping into curl, httpie, or other scripting uses.

- [veracode-go-hmac-authentication](https://github.com/antfie/veracode-go-hmac-authentication) ([antfie](https://github.com/antfie/)) - A simple Go package that follows the format of the existing HMAC Authentication Examples found in the [Veracode Help Center](https://help.veracode.com/reader/LMv_dtSHyb7iIxAQznC~9w/CUv4heF9z9tOBnZ1uiB8UA).

- [Veracode_HMAC_Auth](https://github.com/rafaelzm2000/Veracode_HMAC_Auth) ([rafaelzm2000](https://github.com/rafaelzm2000/)) - A PowerShell example for doing HMAC authentication to the Veracode APIs.

- [Using curl and openssl to access the Veracode API endpoint](https://gist.github.com/m9aertner/7ae804a5297617456f81c8b5a3a9305b) ([m9aertner](https://gist.github.com/m9aertner)) - short article illustrating use of built-in shell tools to handle HMAC signing and send API requests from the command line.

## API wrappers

- [.NET Core Nuget Package Wrapper](https://github.com/sebcoles/VeracodeServicesCore) ([Seb Coles](https://github.com/sebcoles)) - C# NuGet package that wraps XML APIs

- [Go wrapper](https://github.com/brian1917/vcodeapi) ([Brian1917](https://github.com/brian1917)) - Wrapper written in Go for easy use of Veracode APIs

- [node-veracode-api-client](https://github.com/m4l1c3/node-veracode-api-client) ([M4l1c3](https://github.com/m4l1c3/)) - Node.js API client.

- [veracode-api (Ruby)](https://github.com/mort666/veracode-api) ([Mort666](https://github.com/mort666/)) - Ruby Wrapper for the Veracode API.

- [veracode-api-clients](https://github.com/jourzero/veracode-api-clients) ([Jourzero](https://github.com/jourzero/)) - Client code using the Veracode REST and XML APIs. Includes handlers for Veracode Dynamic Analysis scanning.

- [veracode-python](https://github.com/chuckorde/veracode-python) ([Chuckorde](https://github.com/chuckorde/)) - A python wrapper for communicating with the Veracode APIs.

- [veracode-api-py](https://github.com/tjarrettveracode/veracode-api-py) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - Python helper library for working with the Veracode APIs. Handles retries, pagination, and other features of the modern Veracode REST APIs.

## Other integrations

- [Bash shell](https://github.com/aparsons/Veracode) ([Aparsons](https://github.com/aparsons/)) - Bash script for scanning a directory of code with the Veracode platform.

- [F5 WAF](https://github.com/julz0815/veracode-dynamic-2-F5-waf-export) ([Julz0815](https://github.com/julz0815/)) - Transforms Veracode dynamic result files into the F5 generic scanner result format for import into the F5 web application firewall.

- [verapi](https://github.com/fsclyde/verapi) ([Fsclyde](https://github.com/fsclyde/)) - Lambda function for automating Veracode static scans

- [veracode-api (Node)](https://github.com/kinichahau87/veracode-api) ([Kinichahau87](https://github.com/~kinichahau87)) - Node.js package for automating Veracode scanning from the command line.

- [Veracode-cli](https://github.com/adidas/veracode-cli) ([Adidas](https://github.com/adidas)) - Automated way to check application status and DevSecops compliance.

- [Veracode Notifier](https://github.com/ctcampbell/veracode-notifier) ([Ctcampbell](https://github.com/ctcampbell)) - Lambda function that sends a message to a web hook, for instance for use with Slack

- [VeraHooks Mitigation Webhooks](https://github.com/sebcoles/VeraHooks) ([Seb Coles](https://github.com/sebcoles)) - React .NET Core solution for creating custom webhooks that watch application profiles and trigger when mitigations meet specified conditions.

## Secure coding examples

- [Secure cryptography examples for Java](https://github.com/1MansiS/java_crypto) ([1MansiS](https://github.com/1MansiS/)) - Code samples showing how to use the Java Crypto API securely. Accompanying code for the [Java Crypto blog series](https://www.veracode.com/blog/research/how-get-started-using-java-cryptography-securely).

## Insecure applications

- [VeraDemo](https://github.com/jtsmith2020/verademo-java) ([Jtsmith2020](https://github.com/jtsmith2020/)) - Sample insecure application written in Java and Javascript, showing vulnerabilities in realistic Java code.

- [NodeGoat](https://github.com/buzzcode/NodeGoat) ([Buzzcode](https://github.com/buzzcode/)) - NodeGoat, built w/CircleCI, showing how to use a yaml file to scan w/Veracode.
