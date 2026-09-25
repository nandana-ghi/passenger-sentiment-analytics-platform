# Serverless Passenger Sentiment Analytics Platform ✈️📊

A cloud-native, event-driven data pipeline built on AWS to automate the ingestion, classification, and storage of real-time passenger flight reviews. 

## ✈️ Aviation Business Case
Global airlines like Emirates process thousands of daily customer touchpoints. Manually reviewing inflight feedback forms or social mentions is highly inefficient. This serverless solution automates feedback analysis, instantly routing data payloads into structured sentiment variations so operational teams can monitor brand reputation and service bottlenecks in real-time.

## 🛠️ System Architecture Diagram & Data Flow
1. **API Client (Mobile App/Travel Portal):** Transmits passenger review strings via secure HTTPS POST requests.
2. **Amazon API Gateway:** Serves as the microservice entry point, securely handling concurrent global traffic.
3. **AWS Lambda (Python 3.12):** A lightweight serverless compute layer that scales elastically from zero, processing incoming text blocks instantly.
4. **Natural Language Processing (NLP):** Designed logic configurations classifying structural patterns into Positive, Negative, or Neutral indicators.
5. **Amazon DynamoDB:** A high-speed NoSQL database cluster that indexes and archives analysis results with unique UUID markers (`ReviewID`).

## 📡 Sample Test Payload (ReqBin / Postman)
### Request body:
```json
{
  "review": "The inflight entertainment on my Emirates flight was very good, but the food arrived cold."
}
```

### Response body:
```json
{
  "status": "Success",
  "sentiment": "POSITIVE"
}
```

## 🚀 Key Quantifiable Outcomes
* **Zero Idle Costs:** Built using a 100% serverless infrastructure pattern; incurs $0 overhead fees when idle.
* **Low Latency execution:** Data moves from global application ingestion to active database archiving in under 2 seconds.
* **Elastic Scalability:** Automatically scales up or down to match standard airline hub transit spikes without manual infrastructure configuration.
*
