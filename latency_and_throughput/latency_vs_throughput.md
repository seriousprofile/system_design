## Latency vs Throughput

Latency and throughput are two key metrics used to measure system performance.  
Improving one can sometimes negatively impact the other.

---

## Latency

**Definition:**  
Latency is the amount of time it takes for a system to respond to a request.

### Key Points
- Often measured in **milliseconds (ms)** or **microseconds (µs)**
- Represents the delay between sending a request and receiving a response

### Relationship to Performance
- **High latency → Low performance**
- **Low latency → High performance**

### Example
A user clicks a button on a website:
- If the page loads in **50 ms**, latency is low
- If the page loads in **2 seconds**, latency is high

---

## Throughput

**Definition:**  
Throughput is the number of requests a system can handle within a given time period.

### Key Points
- Often measured in:
  - **Requests per second (RPS)**
  - **Transactions per second (TPS)**
  - **Bits per second (bps)**
- Represents the system's processing capacity

### Relationship to Performance
- **High throughput → System can handle more work**
- **Low throughput → System becomes a bottleneck**

### Example
A server can process:
- **1,000 requests per second** → High throughput
- **50 requests per second** → Low throughput

---

## Trade-off: Latency vs Throughput

Increasing throughput can sometimes increase latency.

### Why This Happens
- Allowing more users into the system increases load
- Shared resources (CPU, memory, network) become more contested
- Response times may slightly slow down

### Simple Intuition

- **Latency:**  
  "How fast does one request finish?"

- **Throughput:**  
  "How many requests can we handle overall?"

---

## Quick Interview Insight

- **Low latency** is critical for:
  - Real-time systems
  - User-facing applications
  - APIs

- **High throughput** is critical for:
  - Batch processing systems
  - Data pipelines
  - Streaming systems
