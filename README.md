[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![Community](https://img.shields.io/badge/Join-Community-blue)](https://developer.ibm.com/callforcode/solutions/projects/get-started/)

# OrientAgro - Global Challenge

- [Project summary](#project-summary)
  - [The issue we are hoping to solve](#the-issue-we-are-hoping-to-solve)
  - [How our technology solution can help](#how-our-technology-solution-can-help)
  - [Our idea](#our-idea)
- [Technology implementation](#technology-implementation)
  - [IBM AI service(s) used](#ibm-ai-services-used)
  - [Other IBM technology used](#other-ibm-technology-used)
  - [Solution architecture](#solution-architecture)
- [Presentation materials](#presentation-materials)
  - [Solution demo video](#solution-demo-video)
  - [Project development roadmap](#project-development-roadmap)
- [Additional details](#additional-details)


## Project summary

### The issue we are hoping to solve

Orientagro aims to tackle the inefficiencies and environmental impact of traditional soil and gas emission management in agriculture. By providing real-time data on soil conditions and greenhouse gas emissions like nitrous oxide, methane, and CO2, we aspire to promote sustainable farming practices and contribute to climate change mitigation. This will allow farmers to optimize their use of resources like water and fertilizers, thus improving productivity while reducing environmental harm.

### How our technology solution can help

OrientAgro's AI-powered portable sensors offer real-time soil and gas emission analysis for sustainable agriculture.

### Our idea

OrientAgro is confronting the pressing challenges in agricultural practices in both the United States and Brazil, focusing primarily on the harmful emissions of greenhouse gases like nitrous oxide (N2O), methane, and CO2. These emissions, largely arising from the use of nitrogen-based fertilizers, are significant contributors to both ozone depletion and global warming. Traditional soil analysis methods further compound the problem. They are not only slow and costly but also environmentally hazardous, relying on external labs that use harmful reagents.

Our solution revolutionizes this status quo with a portable, AI-powered sensor system that offers real-time, accurate monitoring of soil conditions and greenhouse gas emissions. Integrated with IBM Watson Machine Learning, the system includes a variety of soil and gas sensors. Unlike traditional methods that depend on manual, lab-based processes, our technology leverages artificial intelligence to classify soil types, calibrate sensor data, and offer actionable insights. This drastically shortens the time needed for soil analysis, enhances the reliability of the data, and ultimately allows for quicker, more informed farming decisions.

Moreover, our use of AI extends beyond immediate sensor calibration. We are working towards employing machine learning algorithms to offer precise recommendations about fertilizer application. This not only has the potential to reduce the resource cost but also to minimize greenhouse gas emissions. This additional layer of AI-enabled smart decision-making opens avenues for more efficient and environmentally-friendly farming practices.

Importantly, we've validated our technology's feasibility for integration into the carbon credit market. By offering real-time, verified data, our product serves as a credible source for carbon credit assessments. This adds an economic incentive for farmers to adopt our technology, integrating OrientAgro into a larger ecosystem aimed at sustainability and climate resilience.

In summary, OrientAgro offers a holistic, AI-powered solution to address both the environmental and operational inefficiencies in current agricultural practices. By providing real-time data and actionable insights, we're not just improving soil and emission management but also contributing significantly to climate change mitigation efforts. Our technology promises a paradigm shift towards more responsible and efficient farming practices, not just in Brazil and the United States but also globally, making substantial contributions to mitigating climate change and environmental degradation.


## Technology implementation

### IBM AI service(s) used

- [Watson Machine Learning](https://cloud.ibm.com/catalog/services/watson-machine-learning) - IBM Watson Machine Learning is integrated into our solution to enhance the accuracy and reliability of the data collected by our soil and gas sensors. Given the limitations of sensor availability and their varying degrees of precision, Watson's machine learning algorithms are crucial in bridging the gaps. Firstly, we use Watson Machine Learning to classify soil types based on the data collected from our sensors and validated against our growing soil bank, developed in partnership with entities in Brazil. This classification serves as a basis to adjust and correct sensor measurements, enhancing their reliability. It allows us to calibrate the data and estimate the values of soil variables that our sensors are not equipped to measure directly. Secondly, the AutoML feature within IBM Watson assists us in feature selection, helping to identify which sensors are most critical for accurate soil classification. This not only improves the performance of our monitoring system but also has the potential to reduce costs. By identifying less impactful sensors, we can streamline our hardware, making the solution more cost-effective without sacrificing quality. By employing IBM Watson Machine Learning, we can deliver a more accurate, efficient, and cost-effective solution for monitoring soil health and gas emissions, thereby contributing to sustainable agricultural practices.

### Other IBM technology used

In addition to leveraging IBM Watson Machine Learning for data analytics and decision-making, we are in the process of migrating our existing data storage solutions to IBM Cloud Object Storage. This transition aims to provide a more scalable, secure, and cost-effective storage solution, ensuring that our expanding datasets can be efficiently managed and accessed. 


### Solution architecture

Diagram and step-by-step description of the flow of our solution:

![Video transcription/translaftion app](./images/orientagro-solutionArchitecture.png)

1. Initial Setup: The user positions the device in the designated area of the farm for monitoring, replacing traditional manual soil analysis done by agronomists.
2. Data Collection Configuration: Using the mobile app, the user selects between real-time monitoring or schedules a specific time for data collection (e.g., 15-minute intervals for each portion of the farm).
3. Sensor Activation: The device begins collecting data on variables such as NPK (Nitrogen, Phosphorus, Potassium), CO2, N2O, and other soil and gas conditions. 
The device features local data storage, which can also be removed.
4. Bluetooth Connectivity: Users connect to the device via Bluetooth through the mobile app, enabling real-time data visualization. This allows for comparative analysis between different farm regions, specifically concerning gas emissions. Bluetooth was chosen due to limited internet accessibility in many Brazilian farms.
5. Data Transmission: On pressing the 'Generate Report' button on the interface, all collected data is sent to the server.
6. IBM Watson Machine Learning: Data reaches the server, where WatsonX Machine Learning processes it to classify the soil type and returns this classification to our service.
7. Data Calibration: Based on the classified soil type, our server adjusts the sensor data and estimates values for unmeasured variables using our soil bank.
8. Report Generation: A comprehensive soil analysis report is generated, sent to the user's email, and also displayed on the mobile app.
9. Future Work: The system will offer actionable suggestions based on the collected data, such as optimizing fertilizer use depending on soil conditions. It will also allow users to track N2O emissions for potential conversion into carbon credits.


## Presentation materials

### Solution demo video

[![Watch the video](./images/video-cover-2.png)](https://vimeo.com/876595727?share=copy)

### Project development roadmap

The project currently offers the following features:

- Real-time Soil and Gas Monitoring: Our portable device, equipped with various sensors, can measure critical soil parameters such as NPK (Nitrogen, Phosphorus, Potassium) levels as well as greenhouse gas emissions (CO2, N2O, etc.) in real-time.
- Machine Learning for Soil Classification: Utilizing IBM Watson Machine Learning, we classify the type of soil based on sensor data. This allows us to adjust and calibrate the sensor measurements for more accurate readings.
- Data Storage and Report Generation: All the collected data is sent to our server, where it's stored. Users can generate detailed soil analysis reports, which can be viewed via a mobile app or sent to the user's email.
  
In the future, we plan to:

- AI-Driven Fertilizer Recommendations: Leverage the power of AI to provide precise fertilizer application suggestions to farmers, thus reducing both costs and greenhouse gas emissions.
- Carbon Credit Market Integration: Extend the solution's capabilities to validate and quantify reductions in greenhouse gas emissions, making it eligible for the carbon credit market.
- Enhanced Machine Learning Models: Expand our soil bank and continuously improve and refine our machine learning models to adapt to different soil types and conditions.
- Expand to Other Crops and Geographies: Adapt the system for specific needs related to different types of crops and expand our market reach beyond Brazil and the United States.

See below for our proposed schedule on next steps after Call for Code 2023 submission.

![Roadmap](./images/orientagro-roadmap.png)

## Additional details

The content presented is protected under the patent titled "METHOD AND PORTABLE DEVICE WITH GAS AND SOIL SENSORS ABLE TO DETECT, INTERPRET GASEOUS AND PROTONATED MOLECULES, IN THE SOIL, AIR, AND PLANTS", registered with the National Institute of Industrial Property (INPI) as number BR102022001072-2, published in the Industrial Property Journal issue 2743 on 01/08/2023, and also safeguarded by the WIPO PROOF WTS/TIMESTAMPS/0000011332.

---
