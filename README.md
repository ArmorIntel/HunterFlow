# 🕵️‍♂️ HunterFlow - Automated Threat Intelligence & Hunting Assistant

**Warning, this project is under heavy development.**

**HunterFlow** is an open-source automation project designed to augment **Threat Intelligence (CTI)** and **Threat Hunting** operations using **n8n**.
It connects, correlates, and operationalizes intelligence from multiple sources to empower defenders, analysts, and hunters with actionable insights.

---

## 🚀 Project Overview

HunterFlow aims to automate the entire cycle of **threat intelligence ingestion, enrichment, detection, and reporting**.
It transforms scattered cyber threat data into contextual knowledge, enabling proactive detection and faster incident response.

The project’s architecture is modular, allowing users to deploy, use, and extend each part independently, to fit their needs and environment (SOC, CERT, lab, etc.).

---

## ⚙️ Core Capabilities

### 🧠 1. Threat Intelligence Ingestion

* Automatically collects IOCs and TTPs from public and private sources (MISP, OTX, Abuse.ch, RSS, X, etc.).
* Normalizes indicators into standardized formats like STIX2 or JSON for interoperability.
* Tags and classifies threats using the MITRE ATT&CK framework.

### 🔍 2. Enrichment & Correlation

* Enriches IOCs with data from VirusTotal, GreyNoise, Shodan, and other APIs.
* Performs automated correlation and attribution across data sets.
* Scores indicators by confidence and relevance for prioritization.

### 🎯 3. Detection & Hunting

* Generates and deploys Sigma, YARA, or Suricata rules automatically.
* Executes hunting queries across EDR/SIEM platforms (e.g., Sentinel, Splunk, Elastic).
* Sends real-time alerts to Slack, Teams, or email upon matches.

### 📊 4. Reporting & Sharing

* Produces structured weekly intelligence summaries in Markdown.
* Updates dashboards for live monitoring.
* Publishes validated IOCs and rules to GitHub or RSS feeds.

### 🧩 5. Integration & Response

* Integrates seamlessly with platforms such as **OpenCTI**, **TheHive**, and **Cortex**.
* Automates response playbooks (IOC blocking, ticket creation, etc.).
* Closes the loop by feeding new intelligence from incidents back into the system.

---

## 🧩 Example Use Cases

* Automate IOC collection and enrichment from daily feeds
* Convert MITRE ATT&CK techniques into detection rules
* Correlate IOCs from TheHive with CTI feeds
* Generate hunting queries for EDR and SIEM tools
* Create and publish weekly cyber threat bulletins automatically

---

## 🧱 Architecture

HunterFlow is designed to be a master workflow, composed of several interconnected **n8n workflows**:

| Workflow            | Purpose                      | Example Nodes                    |
| ------------------- | ---------------------------- | -------------------------------- |
| CTI Feed Collector  | Collect & normalize IOCs     | HTTP Request, RSS Read           |
| IOC Enrichment      | Correlate via external APIs  | VirusTotal, Shodan, GreyNoise    |
| Detection & Hunting | Generate and deploy rules    | Execute Command                  |
| Reporting Engine    | Build reports and dashboards | Markdown                         |
| Automation Bridge   | Connect with SIEM/EDR        | Webhook, API, HTTP Request       |

---

## 🛠️ Tech Stack

Core :
* **n8n** - Workflow orchestration
* **Python & Javascript** - Workflow functions

Plugged on :
* **OpenCTI / MISP** - Threat Intelligence management
* **Elasticsearch / Sentinel / Splunk** - Detection & hunting queries
* **TheHive + Cortex** - Incident management
* **Grafana / Kibana** - Visualization and metrics

---

## 📈 Roadmap

* [ ] Add all workflows to the repository
* [ ] Integrate Microsoft ATP API as a tool for live hunting
* [ ] Add OpenCTI MCP server for bidirectional enrichment
* [ ] Provide Docker Compose deployment (full stack n8n + tools)

---

## 🤝 Contributing

Contributions, bug reports, and feature ideas are welcome!
Fork the repository, create a feature branch, and submit a pull request.

Please add a commit message and describe your workflow logic.

---

## 🧑‍💻 Author

Developed and maintained by **ArmorIntel**
Focus areas: Threat Intelligence | Threat Hunting | Automation | Cybersecurity Research

---

## ⚖️ License

This project is licensed under the MIT License.
Feel free to use, modify, and share - attribution appreciated.
