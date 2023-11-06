# ML_Production_Part2

## Data - MLE in Production
- Real-world data is dynamic and usually shifting
- In ML: data is first-class citizen (data should have predictive content)
- ![image](https://github.com/hyhung12/ML_Production_Roadmap/assets/97202476/a11f9832-9104-4613-96da-193d776ddab4)

![image](https://github.com/hyhung12/ML_Production_Roadmap/assets/97202476/9f79c83f-695c-4f83-b2d6-818abf9c1b14)
- The world changes so does the data
- Camera are moved
## Model Serving
- Challenge: tradeoff between model's predictability & speed of latency
- ![image](https://github.com/hyhung12/ML_Production_Roadmap/assets/97202476/d0ed3e26-e044-4599-b665-6fb1c9d270ea)
- Caching: GGC Memorystore, AWS DynamoDB
- 2 environments to deploy: edge devices (memory constraint) & cloud (REST API) but not good for app that prediction latency is important
- gRPC maybe better than REST
- ![image](https://github.com/hyhung12/ML_Production_Roadmap/assets/97202476/59be1dba-e36a-4e2b-9502-b68833c0d0d0)
- Scaling Infrastructure: Vertical (Have a bigger car), Horizontal (Lease more cars to less rely)
- Container - convenient way to do horizontal scaling
- ![image](https://github.com/hyhung12/ML_Production_Roadmap/assets/97202476/75366b49-8125-4a60-9982-1cd4390fa104)
- Data in model -> pre-processing, data out -> post-processing
- Batch data (csv file, log file) & Streaming data (data from sensors)
- ![image](https://github.com/hyhung12/ML_Production_Roadmap/assets/97202476/fee30aa9-a21f-440c-89e4-2ae93e7394bf)
- ML - experimental science (experimenting & analyzing - heart of ML development)
- Notebooks are powerful tool but not good for production environment
- Modular code, not monolithic -> production level experiment
- Need tool for Data Versioning
## Model Decay
- Detected by observe statistical properties of logged data or using dashboard
- If it happens, can start over or fine tune
