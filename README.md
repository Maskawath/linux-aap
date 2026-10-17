# Linux Ansible Automation Platform (AAP) Repository

This repository provides enterprise-grade Ansible playbooks and reusable roles designed to run on **Ansible Automation Platform (AAP)**. It includes workflow-ready automation for package auditing, installation, and status reporting across RHEL/Debian Linux environments.

---

## 📁 Repository Structure

```text
linux-aap/
├── .ansible-lint            # Standardized linting rules for Ansible quality control
├── .gitignore               # Git ignore rules for temporary/secret files
├── README.md                # Project documentation
├── collections/
│   └── requirements.yml     # Collection dependencies required for execution
├── playbooks/               # Primary entry points targeted by AAP Job Templates
│   ├── check_package.yml    # Evaluates whether a target package is present
│   ├── install_package.yml  # Installs and enables target package/service
│   └── report_summary.yml   # Generates system audit reports for packages and ports
├── roles/                   # Modular business logic
│   ├── package_checker/     # Logic to inspect package facts
│   ├── package_installer/   # Logic to manage package states and systemd services
│   └── report_generator/   # Jinja2 templating and report formatting
└── group_vars/              # Global and group-specific Ansible variables
    └── all.yml
