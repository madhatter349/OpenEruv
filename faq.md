# OpenEruv FAQ

Welcome to the **OpenEruv** FAQ! Below you’ll find answers to common questions about the project, its purpose, technology, and how to get involved.

## Table of Contents
1. [General Questions](#general-questions)
2. [Technical Questions](#technical-questions)
3. [Contribution Questions](#contribution-questions)
4. [Community and Usage Questions](#community-and-usage-questions)

---

## General Questions

### What is OpenEruv?
**OpenEruv** is an open-source project that aims to modernize the monitoring of eruvin by automating the inspection process. It uses tension sensors, mesh networking, and solar-powered devices to monitor the integrity of eruv wires in real time and send alerts when issues are detected.

### Why is automating eruv monitoring important?
Traditionally, eruvin are manually checked every week to ensure their integrity, which is labor-intensive and prone to human error. Automating the monitoring process provides real-time alerts when the eruv is compromised, reducing the burden on inspectors and ensuring the community can rely on the eruv's status during Shabbat.

### Who is OpenEruv for?
OpenEruv is designed for:
- **Jewish Communities** who want a more reliable and real-time way of monitoring their eruv.
- **Developers and Technologists** who are interested in combining modern technology with traditional practices.
- **Hardware Enthusiasts** who want to contribute to an open-source project that has a tangible impact on communities.

---

## Technical Questions

### What hardware is used in the OpenEruv system?
The primary hardware components are:
- **ESP32 Microcontrollers**: For controlling sensors and communication.
- **Tension Sensors**: Used to measure the tension on the eruv wire, indicating if it is intact or broken.
- **LoRa Modules**: For establishing a mesh network for low-power, long-range communication between nodes.
- **Solar Panels**: To power the nodes continuously.
- **GSM Module for the Gateway**: For cellular communication to send alerts in case of issues.

### How does the mesh network work?
The mesh network is set up using **LoRa/Meshtastic** technology. Each sensor node can communicate with neighboring nodes, and the data eventually reaches a central gateway. This gateway then forwards the collected information (including any alerts) to the cloud via a GSM module or other internet connection.

### What happens if a node stops working?
The mesh network is resilient. If a node stops working, the other nodes will continue to communicate, and the network will reroute messages. The system is designed to have multiple nodes so that even if one node fails, the remaining nodes can continue to monitor the integrity of the eruv.

### How is the system powered?
Each node is equipped with a **solar panel** and a **rechargeable lithium battery** to ensure uninterrupted operation, even during the night or cloudy days. This makes the system largely maintenance-free once installed.

### How are notifications sent?
The central gateway, which collects data from all the sensor nodes, sends notifications when a potential fault is detected. This is typically done through a GSM module, which sends a text message or triggers an alert in a monitoring application.

### What if the eruv crosses areas without good sun exposure?
In areas where sunlight is insufficient, an alternative power source may be required. This could include a larger battery, connection to an existing power grid, or placing the solar panel in a more favorable location with cabling extended to the node.

### Is the system secure?
Yes, data security is considered in the project. The LoRa network uses encryption to secure the communication between nodes. In addition, the gateway is configured to transmit data securely to the server to prevent unauthorized access.

---

## Contribution Questions

### How can I contribute to the project?
We welcome contributions from everyone! You can help by:
- Improving the **firmware** or **gateway software**.
- Contributing to the **hardware design**.
- Writing **documentation** to make it easier for others to get involved.
- Creating **issues** or **pull requests** if you find a bug or want to add a new feature.
Please refer to **CONTRIBUTING.md** for a detailed guide on how to get started.

### I’m not a developer. How can I help?
There are many ways you can contribute even if you are not a developer:
- **Test and Report Issues**: Help test the system in your community and report any problems you encounter.
- **Documentation**: Help improve the clarity of the documentation so that others can understand and use the project.
- **Outreach**: Help spread the word about OpenEruv to Jewish communities that could benefit from automated eruv monitoring.

### Are there any specific skills needed to contribute?
This project welcomes contributors of all skill levels. However, the following skills would be particularly helpful:
- **Embedded Systems Development**: Experience with ESP32 or similar microcontrollers.
- **Electronics Knowledge**: Understanding sensors, circuits, and microcontroller integration.
- **Networking and LoRa**: Experience in configuring mesh networks and optimizing long-range, low-power communication.
- **Web/App Development**: For those interested in creating monitoring dashboards.

---

## Community and Usage Questions

### How can a community set up OpenEruv?
Setting up OpenEruv involves:
1. **Acquiring Hardware**: Collecting ESP32 boards, tension sensors, LoRa modules, solar panels, and other components.
2. **Building Nodes**: Setting up each node with the firmware provided and installing it along the eruv boundary.
3. **Configuring the Gateway**: Connecting the central gateway to the mesh network and setting it up to send alerts.
4. **Testing**: Ensuring the mesh network and tension sensors are working as expected.
Detailed instructions are available in the **SETUP.md** document.

### How much does it cost to set up OpenEruv?
The cost can vary depending on the size of the area and the number of nodes required. The approximate costs include:
- **ESP32 Boards**: ~$5-$10 each.
- **Tension Sensors**: ~$10-$15 each.
- **LoRa Modules**: ~$10-$20 each.
- **Solar Panels and Batteries**: ~$20 per node.
- **GSM Module for Gateway**: ~$20-$30.
Overall, the cost for each node is estimated to be between $50 to $75, and additional costs for the gateway. For a typical eruv, the total cost will depend on the area being covered.

### Does this system require regular maintenance?
The system is designed to be as low-maintenance as possible. The solar panels and batteries should be checked periodically to ensure they are clean and functioning, but otherwise, the system will run autonomously. Alerts will notify if there is a failure in any node.

### Can OpenEruv be used in different types of environments?
Yes, OpenEruv is designed to be versatile. The hardware components are weather-resistant and can be used in urban, suburban, and rural environments. It can be customized to fit various types of eruv infrastructure, such as using different tension sensors for different types of eruv wires.

### What happens if the gateway loses its internet connection?
If the gateway loses its internet connection, it will attempt to reconnect and buffer any alerts until the connection is re-established. However, if the outage lasts for an extended period, alerts may be delayed. We recommend using a GSM module with a reliable cellular provider to minimize this risk.

### How can I contact the community for help?
You can reach the community through:
- **GitHub Discussions**: Join the discussion board at [GitHub Discussions](https://github.com/madhatter349/OpenEruv/discussions).
- **Email**: Send an email to [openeruv@example.com](mailto:openeruv@example.com).
- **Twitter**: Follow us for updates and join the conversation.

---

### Have More Questions?
If you have any other questions that aren’t covered in this FAQ, feel free to ask on the **GitHub Discussions** board, create an **issue**, or reach out via email. We're here to help!

---

**Let’s Build a Better Eruv Together!**

We’re excited to see what this community can achieve with modern technology, innovation, and a shared goal of making life a bit easier for observant Jews around the world. Thank you for your interest and support in **OpenEruv**!
