# Veracode Community Open Source Projects

A collection of useful open source projects that integrate with the Veracode APIs to automate scanning, results retrieval and other tasks.

These projects are community contributed and not supported by Veracode. For a list of supported projects, please see the listing of projects on [Veracode.com](https://www.veracode.com/integrations).

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Contents**

- [Automating common Veracode Platform tasks](#automating-common-veracode-platform-tasks)
  - [Application Profile maintenance](#application-profile-maintenance)
  - [Mitigations](#mitigations)
  - [Sandboxes](#sandboxes)
  - [Scan status](#scan-status)
  - [Other tasks](#other-tasks)
- [Developer tools](#developer-tools)
  - [Auto Packagers (for SAST)](#auto-packagers-for-sast)
  - [CI/CD](#cicd)
    - [Azure DevOps](#azure-devops)
    - [GitHub](#github)
  - [Build tools](#build-tools)
  - [IDEs](#ides)
  - [API testing tools](#api-testing-tools)
  - [Other](#other)
- [Pipeline Scan](#pipeline-scan)
- [Dynamic Analysis](#dynamic-analysis)
- [Software Composition Analysis](#software-composition-analysis)
- [SBOM](#sbom)
- [Results collection and display](#results-collection-and-display)
- [User provisioning, management and deprovisioning](#user-provisioning-management-and-deprovisioning)
- [Application vulnerability correlation](#application-vulnerability-correlation)
- [HMAC Signing libraries](#hmac-signing-libraries)
- [API wrappers](#api-wrappers)
- [Other integrations](#other-integrations)
- [Secure coding examples](#secure-coding-examples)
- [Insecure applications](#insecure-applications)
- [Automating Security Labs tasks](#automating-security-labs-tasks)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Automating common Veracode Platform tasks

### Application Profile maintenance

- [Veracode Bulk Application Creator](https://github.com/cadonuno/Veracode-Bulk-Application-Creator) ([cadonuno](https://github.com/cadonuno/)) - This script allows for bulk importing application profiles into the Veracode platform.

- [Veracode Bulk Application Update](https://github.com/cadonuno/Veracode-Bulk-Application-Update) ([cadonuno](https://github.com/cadonuno/)) - This script allows for bulk updating application profiles in the Veracode platform.

- [Veracode Application Profile Splitting Helper](https://github.com/cadonuno/Veracode-Application-Profile-Splitting-Helper) ([cadonuno](https://github.com/cadonuno/)) - This script is a helper for splitting application profiles. This is usually recommended when working with microservices to ensure that all of them can be scanned individually.

- [Veracode Add Repo URL](https://gitlab.com/buzzcode/veracode-add-repo-url) ([Kevin Rise](https://gitlab.com/buzzcode/)) - Populates the `git repo URL` field in one or more Veracode application profiles from a CSV file.

### Mitigations

- [VcodeAutoMitigate](https://github.com/brian1917/vcodeAutoMitigate) ([Brian1917](https://github.com/brian1917/)) - Command line app that mitigates flaws in Veracode based on CWE, scan type, and specific text in the description.

- [VcodeMitigationExpire](https://github.com/brian1917/vcodeMitigationExpire) ([Brian1917](https://github.com/brian1917/)) - Utility designed to be run on a regular cadence (e.g., weekly cron job) to expire mitigations. The types of mitigations, expiration references, and other settings are controlled in a JSON config file.

- [Veracode Mitigation Copier](https://github.com/tjarrettveracode/veracode-mitigation-copier) ([Tjarrettveracode](https://github.com/tjarrettveracode/)) - Copies mitigations from one Veracode profile to another if it's the same flaw based on the following flaw attributes: issueid, cweid, type, sourcefile, and line. The script will copy all proposed and accepted mitigations for the flaw. The script will skip a flaw in the copy_to build if it already has an accepted mitigation.

- [Veracode SAST Bulk Mitigator](https://github.com/antfie/veracode_bulk_mitigator) ([antfie](https://github.com/antfie/)) - This tool performs bulk mitigation actions on open SAST flaws reported in multiple application profiles. The definitions of what to mitigate (e.g. file name, line number) and the mitigation comments and actions to apply are defined via a JSON file. Application profile names to target are specified via a text file or alternatively a flag can be set to process all application profiles.

### Sandboxes

- [Veracode Create List of Sandboxes](https://github.com/cadonuno/veracode-create-list-of-sandboxes) ([cadonuno](https://github.com/cadonuno/)) - This plugin creates a list of sandboxes in all available application profiles.

- [Veracode Promote Named Sandbox](https://github.com/cadonuno/Veracode-Promote-Named-Sandbox) ([cadonuno](https://github.com/cadonuno/)) - This will promote the latest scan of a named sandbox.

- [Veracode_Delete_Sandbox](https://github.com/christyson/veracode_delete_sandbox) ([Christyson](https://github.com/christyson/)) - A simple example script to delete a Sandbox if it exists in a Veracode application profile and you have the appropriate permissions.

- [Veracode Delete Sandboxes via Threshold](https://github.com/julz0815/VeracodeDeleteSandboxes) ([Julz0815](https://github.com/julz0815/)) - Java Script that will automatically delete Sandboxes from a profile via a configured threshold and the number of Sandboxes to be deleted.

### Scan status

- [Check Build Status](https://github.com/christyson/check_build_status) ([Christyson](https://github.com/christyson/)) - Script to check if an application profile in Veracode has a build running currently.  It also provides an option to delete the build if there is one running.

- [Check Pass Fail](https://github.com/christyson/check_pass_fail) ([Christyson](https://github.com/christyson)) - A simple example script to check pass/fail status of a Veracode app profile (or sandbox) or for a list of app profiles with out sandboxes.

- [Veracode Break the Build by Severity](https://github.com/christyson/Veracode-Break-The-Build-By-Severity) ([Christyson](https://github.com/christyson/)) - This project contains three python scripts useful for working with Veracode projects in a build pipeline to break the build if any findings of a given severity or higher are found.

- [Veracode Scan Counts](https://github.com/tjarrettveracode/veracode-scan-counts) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - Identify Veracode application profiles with one or more static scans in an incomplete state.

### Other tasks

- [Veracode PDF Reports](https://github.com/jphillips-vc/veracode-pdf-reports) ([Jphillips-vc](https://github.com/jphillips-vc)) - Pulls latest PDF reports from Veracode for recent Static and Dynamic scans.

- [Veracode Policy Examples](https://github.com/tjarrettveracode/veracode-policy-examples) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - A collection of example application security "policies as code" that can be added to your Veracode organization account.

## Developer tools

### Auto Packagers (for SAST)

__Note__: Veracode recommends using the [auto-packaging capability](https://docs.veracode.com/r/About_auto_packaging) in the Veracode CLI (`veracode package`). These scripts are provided for reference only.

- [JavaScript Auto Packager](https://github.com/dub-flow/veracode-javascript-packager) ([dub-flow](https://github.com/dub-flow/)) - CLI tool to automatically package a `JavaScript` application for Veracode Static Analysis

- [Go Auto Packager](https://github.com/relaxnow/vcgopkg) ([relaxnow](https://github.com/relaxnow)) - CLI tool to automatically package a `Golang` application for Veracode Static Analysis

- [.NET Auto Packager](https://github.com/nhinv11/veracode-dotnet-packager) ([nhinv11](https://github.com/nhinv11)) - CLI tool to automatically package a `.NET` application for Veracode Static Analysis

### CI/CD

- [Bamboo](https://gitlab.com/buzzcode/Bamboo-Veracode) ([Buzzcode](https://gitlab.com/buzzcode/)) - full featured Bamboo plugin including configuration UI, wait for scan to complete, and "break the build" functionality

- [Bamboo-Jira](https://github.com/buildcom/VeracodeAtlassianPlugin) ([Buildcom](https://github.com/buildcom/)) - provides a pair of simple plugins for upload and results handling from within Bamboo, and a lightweight script to create Jira issues (archived project)

- [Bash-CircleCI](https://github.com/unregistered436/veracode-integrations/tree/master/shell-script) ([Unregistered436](https://github.com/unregistered436)) - Veracode Upload and Scan Bash Script, originally written for CircleCI but can be used for any build system that can run a shell script in bash.

- [Bitrise-step-veracode-scan](https://github.com/psoladoye-geotab/bitrise-step-veracode-scan) ([Psoladoye-geotab](https://github.com/psoladoye-geotab/)) - add Veracode scanning to Bitrise CI.

- [CircleCI](https://github.com/ctcircleci/Verademo/blob/master/.circleci/config.yml) ([ctcircleci](https://github.com/ctcircleci)) - Example configurations for building a project with Maven, then executing policy scan, agent-based SCA, and pipeline scan in a CircleCI pipeline.

- [CircleCI](https://github.com/buzzcode/NodeGoat/blob/master/.circleci/config.yml) ([buzzcode](https://github.com/buzzcode)) - Example configuration for zipping a project, then executing policy scan, agent-based SCA, and pipeline scan in a CircleCI pipeline.

- [easy_sast](https://github.com/seisollc/easy_sast) - ([docker container](https://hub.docker.com/r/seiso/easy_sast)) - A docker container for use in CI pipelines which integrates with Veracode's static analysis tool.
   
- [Exemplos Veracode](https://github.com/M3Corp-Community/Veracode) ([Ivo Dias](https://github.com/IGDEXE)) - In this repository you will find several examples for Veracode implementations created by the [M3Corp](https://github.com/M3Corp-Community) team. In the [Pipelines](https://github.com/M3Corp-Community/Veracode/tree/main/Pipelines) folder you can find how to implement in the most diverse CI/CD tools, such as [Azure](https://github.com/M3Corp-Community/Veracode/tree/main/Pipelines/Az%20DevOps), [GitLab](https://github.com/M3Corp-Community/Veracode/tree/main/Pipelines/GitLab), [GitHub Actions](https://github.com/M3Corp-Community/Veracode/tree/main/Pipelines/GitHub%20Actions) and [Jenkins](https://github.com/M3Corp-Community/Veracode/tree/main/Pipelines/Jenkins). Other implementation examples such as running in a [terminal](https://github.com/M3Corp-Community/Veracode/tree/main/SOs) and [translating the results](https://github.com/M3Corp-Community/Veracode/tree/main/FreeStyle) are also available. We normally publish in Portuguese, but the examples are completely understandable in other languages

- [Jenkins (Jenkins Shell)](https://github.com/ian-c-leonard/veracode_jenkins_shell) ([Ian C Leonard](https://github.com/ian-c-leonard)) - unofficial Veracode shell integration for Jenkins Freestyle projects.

- [veracode-badges](https://github.com/Lerer/veracode-badge) ([Lerer](https://github.com/Lerer/)) - produces badges for READMEs and other artifact repositories showing the status of Veracode policy scans.

- [Veracode Community SAST Azure DevOps Extension](https://github.com/MetLife/VeracodeCommunitySAST) ([MetLife](https://github.com/MetLife/)) - Seamlessly integrate Veracode SAST scans with Azure DevOps build pipelines (using Pipeline Scan).

- [veracode-scripts](https://gitlab.com/aszaryk/veracode-scripts) ([aszaryk](https://github.com/aszaryk)) - Various example scripts for Jenkins and GitLab pipelines, including both static and dynamic examples.

- [veracode-serverless-webhooks](https://github.com/Lerer/serverless-veracode-webhooks) ([Lerer](https://github.com/Lerer)) - enables Veracode customers who want to use the Veracode Upload-and-Scan Static and SCA (not the Pipeline or the IDE scans) and get updates back in an asynchronous manner.

- [Verademo](https://github.com/christyson/verademo) ([christyson](https://github.com/christyson)) - custom fork of Verademo, featuring sample pipeline configurations for Bitbucket, Jenkins and Azure Pipelines.

- [XebiaLabs Release Veracode Plugin](https://github.com/xebialabs-community/xlr-veracode-plugin) ([XebiaLabs-Community](https://github.com/xebialabs-community)) - XL Release for Veracode test automation.  

- [veracode-yml-sample-pipelines](https://github.com/victor-secops/Veracode-yml-sample-pipelines) ([Victor-secops](https://github.com/victor-secops/)) - example YML files for Azure DevOps, Jenkins, GitLab, CircleCI. Pipelines include Veracode SCA Agent scans, Veracode Static Analysis policy and pipeline scans.

- [veracode-aws-documentation](https://github.com/ClintPollock/Veracode-AWS-Code-Suite-Getting-Started-Guide) ([Clintpollock](https://github.com/Clintpollock)) - How to setup an AWS CodeSuite with Veracode Static Analysis, Software Composition Analysis, and Dynamic Analysis.
   
- [veracode-examples](https://github.com/restonlogic/veracode-examples) ([Brandon Samuel](https://github.com/Engrave-zz)) - This repository contains veracode examples in the form of use cases that can be run in end-user environments. Kubernetes. AWS CodePipeline. CircleCi to GCP Functions. Multi-tiered application leveraging various languages.
  
#### Azure DevOps

- [Veracode Azure YML Samples](https://github.com/Clintpollock/VeracodeAzureYMLSamples/) ([Clintpollock](https://github.com/Clintpollock)) - Samples of Azure YML files that work with Veracode scanning

- [Veracode Community SCA Azure DevOps Extension](https://github.com/MetLife/VeracodeCommunitySCA) ([MetLife](https://github.com/MetLife/VeracodeCommunitySCA)) - Seamlessly integrate Veracode Agent-Based SCA scans with Azure DevOps build or release pipelines.

- [Veracode Dynamic Analysis Azure Sample](https://github.com/jphillips-vc/Veracode-Dynamic-Analysis-Azure-Example) ([Jphillips-vc](https://github.com/jphillips-vc/)) - Veracode Dynamic Analysis Azure Sample including script based authentication, and ISM configuration.

- [Veracode Examples in Portuguese](https://github.com/M3Corp-Community/Veracode) - Various examples and documents about how to use and integrate Veracode in multiples scenarios (Azure DevOps, Jenkins, Github Actions, Linux, Windows...) in Portuguese.

- [Veracode Flaw Importer](https://github.com/julz0815/veracode_flaw_importer) ([Julz0815](https://github.com/julz0815/)) - GitHub Action to import static policy findings to GitHub Security Code Scanning Alerts.

- [Veracode Flaw Importer Postprocessing](https://github.com/cadonuno/ADOWorkItemsPostProcess) ([cadonuno](https://github.com/cadonuno/)) - Plugin made to run after the regular import to update the work items with an assigned user and a linked Work Item.

- [Veracode for Azure DevOps Pipelines](https://github.com/zoekdestep/veracode-ado-pipelines) ([zoekdestep](https://github.com/zoekdestep/)) - Yaml files to get started with Veracode on Azure DevOps. Accompanies this [blog post](https://community.veracode.com/s/blog/user-story-how-we-set-up-veracode-in-a-large-azure-project-MCT4HNONEE55CIFA6O3ULXNUW2BI).

- [Azure DevOps Pipeline-Scan plugin](https://github.com/julz0815/ADO-Veracode-Pipeline-Scan-Plugin) ([Julz0815](https://github.com/julz0815/)) - This plugin should make it easier to run the Veracode pipeline scan on Azure DevOps pipelines. The full scan jar is included within the plugin and don't need to be downloaded each time when the pipeline runs. In addition it will populate an additional tab on your pipeline run to display results in a more convinient way. The plugin will automatically update itself every night if a new version of the piepline scan jar is published.  

- [SCA Findings to Work Items](https://github.com/cadonuno/SCAFindingsToWorkItems) ([Cadonuno](https://github.com/cadonuno/)) - Saves new Veracode SCA findings as Azure DevOps Work Items.

- [Azure DevOps promote scan](https://github.com/dmedeiros-veracode/devops-scripts-azure-devops/blob/main/jobs/veracode-sast-platform-release-candidate-promote-job.yml) ([dmedeiros-veracode](https://github.com/dmedeiros-veracode)) - This repository contains Azure DevOps scripts that can be referenced and used for integration with Veracode Analysis tools.  

#### GitHub

- [Veracode Application Sandboxes Helper](https://github.com/marketplace/actions/veracode-application-sandboxes-helper) ([Lerer](https://github.com/Lerer/)) - An Action to handle Sandboxes mainly as a set of clean-up activities such as: deleting a sandbox and promoting Sandbox scan to Policy Scan with or without deleting the sandbox

### Build tools

- [Gradle](https://github.com/calgaryscientific/veracode-gradle-plugin) ([CalgaryScientific](https://github.com/calgaryscientific), based on [Kctang](https://github.com/kctang/)) - Set of Gradle tasks, usable either as a command line submission tool or integrated as part of a continuous integration build process, to perform Veracode submission for applications and scan results for flaws.

- [Sbt-veracode](https://github.com/sullis/sbt-veracode) ([Sullis](https://github.com/sullis/)) - sbt plugin for Veracode.

### IDEs

- [VSCode-Veracode](https://gitlab.com/buzzcode/VSCode-Veracode) ([Buzzcode](https://gitlab.com/buzzcode/VSCode-Veracode)) - a plugin for Visual Studio Code that enables integration with Veracode Static Analysis. Currently, this only supports flaw download, but will be enhanced to support upload as well in the future.

- [vsccode-veracode-sca](https://github.com/Lerer/vscode-veracode-sca) ([Lerer](https://github.com/Lerer/)) - A very simple plugin for Veracode SCA to get agent-base SCA results into VSCode IDE.

- [Veracode Unified Plugin Unofficial Version](https://github.com/Lerer/VSCode-Veracode-Unified) ([Lerer](https://github.com/Lerer/)) - VSCode plugin which integrate with the Veracode platform and enables downloading of scan results (findings) for both Static and SCA (Upload-and-Scan), run pipeline scan, and submit mitigations [Link to the plugin in VSCode marketplace](https://marketplace.visualstudio.com/items?itemName=YaakovLerer.veracode)

- [Jetbrains family plugin](https://github.com/geraldtancl/veracode.plugin) ([GeraldTanCL](https://github.com/geraldtancl)) - Compliments Veracode's official IntelliJ IDE integration with support for other Jetbrains IDE products. It enables you to download the SAST result from Veracode Platform into your Jetbrains IDE.

### API testing tools

- [Insomnia](https://github.com/veracode/insomnia-plugin-veracode-hmac) ([Veracode](https://github.com/veracode/)) - Adds an HMAC authentication header to Veracode API requests in Insomnia.

- [Veracode-Postman](https://github.com/veracode/veracode-postman) ([Veracode](https://github.com/veracode/)) - Pre-request authentication script and instructions for accessing Veracode APIs from Postman.

- [Veracode-API-HMAC-Rapid-Api-Extension](https://github.com/literallyjustroy/Veracode-API-HMAC-Rapid-Api-Extension) ([Literallyjustroy](https://github.com/literallyjustroy)) - An extension for the RapidAPI (Paw) REST Client to authenticate into the Veracode REST APIs using HMAC.

### Other

- [Ansible](https://github.com/telusdigital/ansible-veracode-scanner) ([Telus Digital](https://github.com/telusdigital)) - allows uploading and scanning with Veracode from Ansible, with an option to send results to a Slack channel

- [Flowdock](https://github.com/brian1917/vcodeFlowdockNotifier) ([Brian1917](https://github.com/brian1917/)) - Utility designed to be run in a build process after a Veracode scan to notify a Flowdock flow that the scan completed. Optional to include policy compliance info in notification.

- [PowerShell](https://github.com/unregistered436/veracode-integrations/tree/master/powershell) ([Unregistered436](https://github.com/unregistered436)) - PowerShell script for pushing binaries to Veracode using Java API.

- [SonarQube](https://gitlab.com/buzzcode/SonarQube-Veracode) ([Buzzcode](https://gitlab.com/buzzcode)) - Unofficial Veracode plugin for SonarQube.

- [Veracode QuickScan](https://github.com/relaxnow/veracode-quick-scan) ([relaxnow](https://github.com/relaxnow)) - PHP example of how to connect to the APIs, scan a couple of files and get results.

- [Veracode Upload and Scan Shell Script](https://github.com/christyson/Veracode-Upload-and-Scan-Shell-Script) ([Christyson](https://github.com/christyson/)) - A shell script to upload and scan a application (zip or war etc.) and create the application if necessary. Uses Curl and hmac headers.

## Pipeline Scan 

- [Pipeline2DetailedReport](https://github.com/jphillips-vc/pipeline2detailedreport) ([JPhillips-vc](https://github.com/jphillips-vc/)) - translate Veracode Pipeline Scan results into DetailedReport XML format, allowing you to import them into an IDE plugin for remediation.

- [pipeline2html](https://github.com/victor-secops/pipeline2html) ([Victor-secops](https://github.com/victor-secops/)) - run a Veracode Pipeline Scan and generate a human-readable .HTML file from the Veracode pipeline verification results.json file.

- [Pipeline2JUnitXml](https://github.com/cadonuno/Pipeline2JUnitXml) ([cadonuno](https://github.com/cadonuno/)) - reads the JSON output of a Veracode Pipeline Scan and converts it into a standard JUnit test results XML file.

- [PipelineResultsCompare](https://github.com/cadonuno/PipelineResultsCompare) ([cadonuno](https://github.com/cadonuno/)) - checks if there are any issues present on a pipeline results file that aren't present on another, supporting filtering by severity.

- [veracode-pipeline-PR-comment](https://github.com/Lerer/veracode-pipeline-PR-comment) ([Lerer](https://github.com/Lerer/veracode-pipeline-PR-comment)) - Sends output of Pipeline Scan to a comment on a pull request.

- [veracode-pipeline-with-baseline](https://github.com/runkalicious/veracode-pipeline-with-baseline) ([Runkalicious](https://github.com/runkalicious/)) - GitHub Action to perform a Veracode Pipeline Scan and, optionally, compare the results against a set of baseline results.

## Dynamic Analysis 

- [veracode-da-reset-scheduler](https://github.com/dennismedeiros/veracode-da-reset-recheduler) ([dennismedeiros](https://github.com/dennismedeiros)) - Resets all recurrent scheduled analysis jobs configured for one year that have expired.

- [Veracode Dynamic Analysis Examples](https://github.com/anon-veracoder/veracode-dynamic-analysis-api-examples) ([anon-veracoder](https://github.com/anon-veracoder)) - Dynamic Analysis API Examples.  Currently includes example code for using the Scanner Variables feature, where credentials can be defined and updated at the account level, and referenced in Selenium login scripts.

- [Veracode DAST Add bulk urls to blocklist](https://github.com/AaronButler-Veracode/veracode_DAST_add_to_blocklist) ([aabutler](https://github.com/AaronButler-Veracode)) - Adds a list of urls to the blocklist for an existing DAST scan.

## Software Composition Analysis

- [Veracode-Get-EPSS-Info](https://github.com/cadonuno/Veracode-Get-EPSS-Info) ([cadonuno](https://github.com/cadonuno/)) - Gets all the SCA findings available to the user, including EPSS scores and percentiles.

- [Veracode-SCA-Webhook-Redirect](https://github.com/cadonuno/Veracode-SCA-Webhook-Redirect) ([cadonuno](https://github.com/cadonuno/)) - This Project exposes a Tomcat server that can redirect Veracode Agent-based SCA web hooks to Teams and Slack.

- [yarn-v2-workspaces-helper](https://github.com/julz0815/yarnv2-workspaces-helper) ([Julz0815](https://github.com/julz0815/)) - Creates yarn.lock files for each workspace to make the whole project scannable with Veracode's SCA solution. this is specifically for yarn version 2 and lower

- [yarn-v3-workspaces-helper](https://github.com/julz0815/yarnv3-workspaces-helper) ([Julz0815](https://github.com/julz0815/)) - Creates yarn.lock files for each workspace to make the whole project scannable with Veracode's SCA solution. this is specifically for yarn version 3 and higher  

- [veracode-bulk-cve-suppression](https://github.com/aszaryk/veracode-bulk-cve-suppression) ([aszaryk](https://github.com/aszaryk)) - Allows for bulk suppression of specific CVE across full application portfolio

- [Bulk add teams to workspaces](https://github.com/cadonuno/add-team-to-workspace) ([cadonuno](https://github.com/cadonuno/)) - Allows for adding teams to workspaces in bulk.

- [Veracode Workspace Auto Create](https://github.com/tjarrettveracode/veracode-workspace-auto-create) ([Tjarrettveracode](https://github.com/tjarrettveracode/)) - Uses the Veracode Agent Based Scan API and other Veracode REST APIs to automatically create a workspace for application profiles in a Veracode organization.

## SBOM

- [Veracode Get All SBOMs](https://github.com/cadonuno/Veracode-Bulk-SBOM) ([cadonuno](https://github.com/cadonuno/)) - Allows for bulk generation of SBOM json files. It works for both US and EU instances and has support for Upload and Scan and Agent-based scan.

- [Veracode Get Single SBOM](https://github.com/cadonuno/Veracode-Get-Sbom) ([cadonuno](https://github.com/cadonuno/)) - Gets the SBOM for a single Application Profile or Workspace/Project pair.

## Results collection and display

- Collections Report [PDF, CSV, JSON](https://github.com/tjarrettveracode/veracode-collections-report) ([tjarrettveracode](https://github.com/tjarrettveracode/)) - Python script to retrive Collection results and output to PDF, CSV and/or JSON format.

- [Excel (XLS)](https://github.com/Komiblanka/Veracode2xls) ([Komiblanka](https://github.com/Komiblanka/)) - Python scripts to format Veracode XML results into Excel workbook formats for easier human consumption.  

- [(XLSX)](https://github.com/Komiblanka/Veracode2xlsx) ([Komiblanka](https://github.com/Komiblanka/)) - Python scripts to format Veracode XML results into Excel workbook formats for easier human consumption.

- [Generate License Notice file](https://github.com/gmdavef/sca-scripts) ([Dave Ferguson](https://github.com/gmdavef)) - Python script that creates a License Notice file (sometimes called an Attribution Report) for an application that has been scanned by Veracode SCA.

- [Generate SBOM with Python](https://github.com/christyson/GenerateSBOM) ([Chris Tyson](https://github.com/christyson)) - Python script to generate a Software Bill of Materials (SBOM) for an application in either CycloneDX or SPDX format.

- [Generate SBOM with Powershell](https://github.com/christyson/GenerateSBOMPS) ([Chris Tyson](https://github.com/christyson)) - Powershell script to generate a Software Bill of Materials (SBOM) for an application in either CycloneDX or SPDX format.

- [Hygieia](https://github.com/mickfeech/hygieia_veracode_collector) ([Mickfeech](https://github.com/mickfeech/)) - Veracode scan collector and parser for the [Hygieia dashboard](https://github.com/Hygieia/ExecDashboard).

- [JupiterOne Graph Veracode](https://github.com/JupiterOne/graph-veracode) ([JupiterOne](https://github.com/JupiterOne/)) - A graph conversion tool for Veracode.

- [SCA Extractor](https://github.com/brian1917/vcodeSCAExtractor) ([Brian1917](https://github.com/brian1917)) - Creates a CSV file with open source vulnerability (SCA) findings for all builds in the input file.

- [Veracode Container Scan results to HTML](https://github.com/cadonuno/VeracodeContainerScanToHtml) ([cadonuno](https://github.com/cadonuno)) - Converts the JSON output of a Veracode container scan into HTML.

- [Veracode Scan Compare](https://github.com/antfie/scan_compare) ([antfie](https://github.com/antfie)) - Use this tool to compare two Veracode Static Analysis (SAST) scans to understand why they are different.

- [Veracode Scan Health](https://github.com/antfie/scan_health) ([antfie](https://github.com/antfie)) - Produces a SAST scan health report with guidance on changes to make in order to improve the packaging and module selection to achieve greater flaw accuracy.

- [VeraData](https://github.com/sebcoles/VeraData) ([Seb Coles](https://github.com/sebcoles)) - Console application that will retrieve data (all scans, flaws, mitigations etc) for a given AppId and store the results in a relational schema (only supports MSSQL Server currently) ready for plugging your favourite BI tool into!

- [VeraCustomTriage](https://github.com/sebcoles/VeraCustomTriage) ([Seb Coles](https://github.com/sebcoles)) - App that generates a .xlsx remediation plan from a set of scan results augmented with text from JSON configuration files. Custom text is added when flaw criteria is met (such as a CWE ID, module name, file or line number). This allows custom text such as internal workflows, wiki links, training, code snippets, 2nd party information or other languages into the auto generated remediation plan. Enables app sec teams to triage large volumes of flaws quickly whilst sharing a core advice repository in code.

- [Veracode Report Converter (CSV)](https://github.com/dipsylala/VeracodeReportConverter-Windows) ([Dipsylala](https://github.com/dipsylala/)) - .NET Framework utility to extract useful data from Detailed Report XML file into CSV format

- [Veracode Report Converter Portable (CSV)](https://github.com/dipsylala/VeracodeReportConverter-Portable) ([Dipsylala](https://github.com/dipsylala/)) - .NET Core utility to extract useful data from Detailed Report XML file into CSV format

- [Veracode Bulk Reporting API Import](https://github.com/cadonuno/veracode-reporting-api-bulk-import) ([Cadonuno](https://github.com/cadonuno/)) - Retrieves all the data available from the Veracode Reporting API from a specific start date

- [Veracode Gitlab SCA results report and issue generation](https://gitlab.com/julz0815/scaresultsreport) ([julz0815](https://gitlab.com/julz0815/)) - Rewrites Veracode's Agent Based SCA json results in Gitlab readable report format in (orde)r to display results as dependency scanning on the pipeline run

- [Veracode Gitlab static results report and issue generation](https://gitlab.com/julz0815/veracodesastresultsimport) ([julz0815](https://gitlab.com/julz0815/)) - A little Java Script will download json results from a Veracode policy or sandbox scan into Gitlab readable report format in order display results as SAST results on the pipeline run and create Gitlab issues on the findings

- [VCCLI](https://github.com/michaelhorty/VCCLI) ([Michaelhorty](https://github.com/michaelhorty)) - Veracode AST and Security Labs utility in .NET Core.

- [Veracode Container Security Display (Unofficial)](https://relaxnow.github.io/vcsd/) ([relaxnow](https://github.com/relaxnow)) - Display, sort and filter Container Security JSON results.

- [Veracode Verify Scan Results](https://github.com/cadonuno/Veracode-Verify-Scan-Results) ([cadonuno](https://github.com/cadonuno)) - This script checks for the results of the latest scan for an application profile (and optionally a sandbox) and returns all the results that meet a minimum severity criteria. Can optionally consider SCA results and fail a build.

- [TopDesk](https://github.com/daniel-marchi/Veracode.Integration.TopDesk) ([Daniel-Marchi](https://github.com/daniel-marchi)) - Integration with ITSM | CSC | ESM tool called [TopDesk](https://www.topdesk.com/).

## User provisioning, management and deprovisioning

- [Azure AD SAML SSO Autocreating teams](https://dev.azure.com/jtotzek/_git/AD-Veracode-Teams) ([Jtotzek](https://dev.azure.com/jtotzek/)) - Code and documentation on configuring Azure Active Directory to automatically create teams as part of the just-in-time provisioning workflow via SAML.

- [Veracode API Credentials Expiry](https://github.com/christyson/veracode-python-api_credentials_expiry-example) ([Christyson](https://github.com/christyson)) - A simple example to get the exiration dates of api credentials for your users.

- [Veracode Get User List](https://github.com/christyson/veracode_get_user_list) ([Christyson](https://github.com/christyson/)) - Get a list of users with their attributes.

- [Veracode Offboard](https://github.com/tjarrettveracode/veracode-offboard) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - Deactivates a provided list of users on the Veracode Platform.

- [Veracode User Bulk Role Assign](https://github.com/tjarrettveracode/veracode-user-bulk-role-assign) ([Tjarrettveracode](https://github.com/tjarrettveracode/)) - Uses the Veracode Identity API to add roles (Security Labs User, Greenlight IDE User, or eLearning) to existing users.

- [Veracode UM Powershell Tool](https://github.com/IGDEXE/Veracode-UM-Tool) ([IGD753](https://github.com/IGDEXE)) - A completed User management tool write in Powershell using the Veracode APIs. You can use to create, block, delete and update users, in Windows, Linux or Mac terminal. This a simplified and translated version from the original in [Portuguese](https://github.com/IGDEXE/Veracode-UM).

- [Veracode UM Powershell Tool in Portuguese](https://github.com/IGDEXE/Veracode-UM) ([IGD753](https://github.com/IGDEXE)) - A completed User management tool write in Powershell using the Veracode APIs. This version is completed in Portuguese, and you can use to create, block, delete and update users, in Windows, Linux or Mac terminal.

- [Veracode Bulk User Creator and Editor](https://github.com/cadonuno/Veracode-Bulk-User-Management) ([cadonuno](https://github.com/cadonuno/)) - This script allows for bulk modifying and/or creating users in Veracode.

## Application vulnerability correlation

- [DefectDojo](https://github.com/DefectDojo/django-DefectDojo) - DefectDojo is an open-source application vulnerability correlation and security orchestration application. DefectDojo supports importing Veracode results.

- [Veracode Archer](https://github.com/veracode/veracode-archer) ([Veracode](https://github.com/veracode/)) - Script to export a Veracode Archer report file to disk. Usage: set on a timer and run daily or weekly, then import the results into RSA Archer.

## HMAC Signing libraries

- [auth.js](https://gist.github.com/ThibaudLopez/fe1baeaa4461cbf0bfa8fd258ff43243) ([undefined](undefined)) - Veracode custom HMAC request signing algorithm (used for API authorization), written in JavaScript -- uses Web Crypto API instead of the Node Crypto library

- [PythonHMAC](https://github.com/veracode/veracode-python-hmac-example) ([Veracode](https://github.com/veracode/)) - simple example of usage of the Veracode API signing library provided in the Veracode Help Center

- [NodeJS](https://gist.github.com/mrpinghe/f44479f2270ea36bf3b7cc958cc76cc0) ([undefined](undefined)) - NodeJS lib, written in JavaScript, to generate authorization header with Veracode API Key and ID. Sample usage in the comment of the gist

- [vcodeHMAC](https://github.com/brian1917/vcodeHMAC) ([Brian1917](https://github.com/brian1917/)) - Go package that creates an authorization header using Veracode API Key and ID.

- [vcodeHMAC-CLI](https://github.com/brian1917/vcodeHMAC-CLI) ([Brian1917](https://github.com/brian1917/)) - CLI tool to generate an authorization header for Veracode APIs using API ID and Key. Given an HTTP method and URL, and the location of your Veracode API credentials file, you will get the value of an Authorization header printed out for piping into curl, httpie, or other scripting uses.

- [veracode-go-hmac-authentication](https://github.com/antfie/veracode-go-hmac-authentication) ([antfie](https://github.com/antfie/)) - A simple Go package that follows the format of the existing HMAC Authentication Examples found in the [Veracode Help Center](https://docs.veracode.com/r/c_hmac_signing_example_c_sharp).

- [Veracode_HMAC_Auth](https://github.com/rafaelzm2000/Veracode_HMAC_Auth) ([rafaelzm2000](https://github.com/rafaelzm2000/)) - A PowerShell example for doing HMAC authentication to the Veracode APIs.

- [Using curl and openssl to access the Veracode API endpoint](https://gist.github.com/m9aertner/7ae804a5297617456f81c8b5a3a9305b) ([m9aertner](https://gist.github.com/m9aertner)) - short article illustrating use of built-in shell tools to handle HMAC signing and send API requests from the command line.

## API wrappers

- [.NET Core Nuget Package Wrapper](https://github.com/sebcoles/VeracodeServicesCore) ([Seb Coles](https://github.com/sebcoles)) - C# NuGet package that wraps XML APIs

- [Go wrapper](https://github.com/brian1917/vcodeapi) ([Brian1917](https://github.com/brian1917)) - Wrapper written in Go for easy use of Veracode APIs

- [node-veracode-api-client](https://github.com/m4l1c3/node-veracode-api-client) ([M4l1c3](https://github.com/m4l1c3/)) - Node.js API client.

- [veracode-api (Ruby)](https://github.com/mort666/veracode-api) ([Mort666](https://github.com/mort666/)) - Ruby Wrapper for the Veracode API.

- [veracode-api-clients](https://github.com/jourzero/veracode-api-clients) ([Jourzero](https://github.com/jourzero/)) - Client code using the Veracode REST and XML APIs. Includes handlers for Veracode Dynamic Analysis scanning.

- [veracode-api-py](https://github.com/tjarrettveracode/veracode-api-py) ([Tjarrettveracode](https://github.com/tjarrettveracode)) - Python helper library for working with the Veracode APIs. Handles retries, pagination, and other features of the modern Veracode REST APIs.

## Other integrations

- [Bash shell](https://github.com/aparsons/Veracode) ([Aparsons](https://github.com/aparsons/)) - Bash script for scanning a directory of code with the Veracode platform.

- [F5 WAF](https://github.com/julz0815/veracode-dynamic-2-F5-waf-export) ([Julz0815](https://github.com/julz0815/)) - Transforms Veracode dynamic result files into the F5 generic scanner result format for import into the F5 web application firewall.

- [verapi](https://github.com/fsclyde/verapi) ([Fsclyde](https://github.com/fsclyde/)) - Lambda function for automating Veracode static scans

- [veracode-api (Node)](https://github.com/kinichahau87/veracode-api) ([Kinichahau87](https://github.com/~kinichahau87)) - Node.js package for automating Veracode scanning from the command line.

- [Veracode-cli](https://github.com/adidas/veracode-cli) ([Adidas](https://github.com/adidas)) - Automated way to check application status and DevSecops compliance.

- [VeraHooks Mitigation Webhooks](https://github.com/sebcoles/VeraHooks) ([Seb Coles](https://github.com/sebcoles)) - React .NET Core solution for creating custom webhooks that watch application profiles and trigger when mitigations meet specified conditions.

## Secure coding examples

- [Secure cryptography examples for Java](https://github.com/1MansiS/java_crypto) ([1MansiS](https://github.com/1MansiS/)) - Code samples showing how to use the Java Crypto API securely. Accompanying code for the [Java Crypto blog series](https://www.veracode.com/blog/research/how-get-started-using-java-cryptography-securely).

## Insecure applications

- [VeraDemo](https://github.com/jtsmith2020/verademo-java) ([Jtsmith2020](https://github.com/jtsmith2020/)) - Sample insecure application written in Java and Javascript, showing vulnerabilities in realistic Java code.
  
- [VeraDemoAPI](https://github.com/veracode/verademo-javascript-api) ([Veracode](https://github.com/veracode)) - Sample insecure application written in Javascript, showing vulnerabilities in realistic Javascript code.
  
- [VeraDemoJava](https://github.com/veracode/verademo-java-web) ([Veracode](https://github.com/veracode)) - Sample insecure application written in Java, showing vulnerabilities in realistic Java code.
  
- [VeraDemoDocker](https://github.com/veracode/verademo-app-docker) ([Veracode](https://github.com/veracode)) - Bringing the 2 demo apps above VeraDemoJave and VeraDemoAPI together and start them within a docker environment. You will get a Java Web Application, a JavaScript node express API. a MySQL database and a vulnerable container.  
  
- [NodeGoat](https://github.com/buzzcode/NodeGoat) ([Buzzcode](https://github.com/buzzcode/)) - NodeGoat, built w/CircleCI, showing how to use a yaml file to scan w/Veracode.

## Automating Security Labs tasks

- [Security Labs Scripts](https://github.com/gmdavef/security-labs-scripts) ([Dave Ferguson](https://github.com/gmdavef)) - Python scripts to automate various administrative tasks in Veracode Security Labs.
