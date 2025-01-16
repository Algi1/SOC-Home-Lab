# SOC Home Lab (SHL)

Welcome to **SOC Home Lab (SHL)**, a modular and evolving open-source project aimed at building a practical, scalable, and dynamic Security Operations Center (SOC) Lab. This project provides a foundation for security enthusiasts, professionals, and students to simulate SOC operations, analyse data, and learn industry-relevant tools.

---

## 🌐 **Project Overview**


![SOC Home Lab Diagram](architecture/SOC-Home-Lab-v1.excalidraw.png)

The **SOC Home Lab (SHL)** serves as a starting point for creating and managing SOC environments. It integrates essential tools for log ingestion, processing, storage, and visualisation, providing a platform for learning, experimenting, and growing.

### Current Features

- **Cribl**: For log ingestion and enrichment.
- **Elasticsearch**: For storing and indexing logs.
- **Kibana**: For visualising and analysing data.

### Planned Features

- Integration with additional data sources (Linux, Windows, Firewall, IDS).
- Threat intelligence integration.
- SIEM detection rules and alerting.
- Automation tools (SOAR platforms, workflow scripts).

This is an ongoing project, so your feedback and contributions are highly encouraged!

---

## 🗃️ **Project Structure**

Here's an overview of the current project structure:

```plaintext
soclab/
├── README.md                # Project documentation
├── architecture/            # Architecture diagrams and assets
│   └── SOC-Home-Lab-v1.excalidraw.png
soclab/
├── README.md                # Project documentation
├── kibana/                  # Kibana service
│   └── docker-compose.yml   # Kibana-specific configuration
├── cribl/                   # Cribl service
│   ├── docker-compose.yml   # Cribl-specific configuration
│   └── cribl-config/        # Persistent configuration for Cribl
├── elasticsearch/           # Elasticsearch service
│   └── docker-compose.yml   # Elasticsearch-specific configuration
```

---

## 🚀 **Getting Started**

Follow these steps to set up and run the SOC Home Lab (SHL):

### Prerequisites

- Docker and Docker Compose installed on your system.
- A basic understanding of containerized environments.

### Installation

1. Clone the repository:
    
    ```bash
    git clone https://github.com/Algi1/soc-home-lab.git
    cd soclab
    ```
    
2. Start the lab environment:
    
    ```bash
    docker compose -p soclab -f cribl/docker-compose.yml -f elasticsearch/docker-compose.yml -f kibana/docker-compose.yml up -d
    ```
    
3. Access the Cribl service:
    
    - **Cribl**: `http://localhost:9000`

3. Access the Kibana service:
    
    - **Kibana**: `http://localhost:5601`
  
3. Access the Elasticsearch service:
   
    - **Elasticsearch**: `http://localhost:9200`


## 🤝 **Contributing**

I welcome and appreciate contributions of all kinds! Here are a few ways you can help:

1. **Feature Suggestions**: Share ideas for tools, configurations, or integrations that can make this lab better.
2. **Bug Reports**: If you encounter any issues, let me know by opening an issue in the repository.
3. **Code Contributions**: Feel free to submit pull requests for enhancements, fixes, or new features.
4. **Documentation**: Help improve the README, guides, or any documentation.

---

## 📅 **Future Plans**

As this project evolves, I aim to:

- Add support for IDS tools like Suricata and Zeek.
- Integrate more advanced SOAR tools.
- Develop threat detection use cases and pre-configured dashboards.
- Include comprehensive simulation scenarios for SOC analysts.

I’d love to hear your suggestions for new features or enhancements!

---

## 📧 **Contact**

If you have questions, feedback, or ideas, feel free to reach out:

- **📧 Email**: [algicodes@gmail.com](mailto:algicodes@gmail.com)
- **🔗 GitHub**: [Algi1](https://github.com/Algi1)

Let’s build a better SOC Lab together!
