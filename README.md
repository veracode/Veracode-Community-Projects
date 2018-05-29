Veracode Community Open Source Projects
=======================================

A collection of useful open source projects that integrate with the CA Veracode APIs to automate scanning, results retrieval and other tasks. These are community contributed and not supported by CA Veracode.

Developer tools
---------------

* [Ansible](https://github.com/telusdigital/ansible-veracode-scanner) ([Telus Digital](https://github.com/telusdigital)) - allows uploading and scanning with Veracode from Ansible, with an option to send results to a Slack channel

* [Bamboo](https://gitlab.com/buzzcode/Bamboo-Veracode) ([Buzzcode](https://gitlab.com/buzzcode/)) - full featured Bamboo plugin including configuration UI, wait for scan to complete, and "break the build" functionality

* [Bamboo/Jira](https://github.com/buildcom/VeracodeAtlassianPlugin) ([Buildcom](https://github.com/buildcom/)) - provides a pair of simple plugins for upload and results handling from within Bamboo, and a lightweight script to create Jira issues

* [ConcourseCI, Gitlab, Travis](https://github.com/ctcampbell/veracode-ci-examples) ([Ctcampbell](https://github.com/ctcampbell)) - Example configurations for integrating Veracode scanning in various continuous integration systems.

* [Dynamic Scan and Wait for Result](https://github.com/christyson/dynamic-scan-and-wait-for-result) ([Christyson](https://github.com/christyson/)) - Extends the Java API Wrapper to provide "break the build" style scanning. Includes instructions on how to integrate this workflow into Jenkins.

* [Gradle](https://github.com/kctang/vt) ([Kctang](https://github.com/kctang/)) - Set of Gradle tasks, usable either as a command line submission tool or integrated as part of a continuous integration build process, to perform Veracode submission for applications and scan results for flaws.

* [Slack](https://github.com/ctcampbell/veracode-slack-slash-command) ([Ctcampbell](https://github.com/ctcampbell)) - AWS Lambda commands that provide the ability to access Veracode application and build information from Slack.


Results collection and display
------------------------------

* [Excel (XLS)](https://github.com/Komiblanka/Veracode2xls), [(XLSX)](https://github.com/Komiblanka/Veracode2xlsx) ([Komiblanka](https://github.com/Komiblanka/))- Python scripts to format Veracode XML results into Excel workbook formats for easier human consumption.

* [go Veracode results](https://github.com/m4l1c3/go-veracode-results) ([M4l1c3](https://github.com/m4l1c3/)) - Go utility for processing Veracode results

* [Hygieia](https://github.com/mickfeech/hygieia_veracode_collector) ([Mickfeech](https://github.com/mickfeech/)) - Veracode scan collector and parser for the [Hygieia dashboard](https://github.com/Hygieia/ExecDashboard).

* [SCA Extractor](https://github.com/brian1917/vcodeSCAExtractor) ([Brian1917](https://github.com/brian1917)) - Creates a CSV file with open source vulnerability (SCA) findings for all builds in the input file.

* [Stats](https://github.com/ctcampbell/veracode-stats) ([Ctcampbell](https://github.com/ctcampbell)) - Summary statistics for a Veracode account on the command line.

* [Veracode Report Converter (CSV)](https://github.com/dipsylala/VeracodeReportConverter-Windows) ([Dipsylala](https://github.com/dipsylala/)) - .NET Framework utility to extract useful data from Detailed Report XML file into CSV format

* [Veracode Report Converter - Portable (CSV)](https://github.com/dipsylala/VeracodeReportConverter-Portable) ([Dipsylala](https://github.com/dipsylala/)) - .NET Core utility to extract useful data from Detailed Report XML file into CSV format


Application vulnerability correlation
-------------------------------------

* [DefectDojo](https://github.com/DefectDojo/django-DefectDojo) - DefectDojo is an open-source application vulnerability correlation and security orchestration application. DefectDojo supports importing Veracode results.

Other integrations
------------------

* [Bash shell](https://github.com/aparsons/Veracode) ([Aparsons](https://github.com/aparsons/)) - Bash script for scanning a directory of code with the Veracode platform.

* [Go wrapper](https://github.com/brian1917/vcodeapi) ([Brian1917](https://github.com/brian1917)) - Wrapper written in Go for easy use of Veracode APIs

* [verapi](https://github.com/fsclyde/verapi) ([Fsclyde](https://github.com/fsclyde/)) - Lambda function for automating Veracode static scans

* [Veracode Notifier](https://github.com/ctcampbell/veracode-notifier) ([Ctcampbell](https://github.com/ctcampbell)) - Lambda function that sends a message to a web hook, for instance for use with Slack

Secure coding examples
----------------------

* [Secure cryptography examples for Java](https://github.com/1MansiS/java_crypto) ([1MansiS](https://github.com/1MansiS/)) - Code samples showing how to use the Java Crypto API securely. Accompanying code for the [Java Crypto blog series](https://www.veracode.com/blog/research/how-get-started-using-java-cryptography-securely).


Insecure applications
---------------------

* [VeraDemo](https://github.com/jtsmith2020/verademo-java) ([Jtsmith2020](https://github.com/jtsmith2020/)) - Sample insecure application written in Java and Javascript, showing vulnerabilities in realistic Java code.
