# CODE IQ HUB

## AWS Cloud Services  

### Day – 1 : Cloud Basics  

#### What to Learn  
- What is Cloud Computing (on-demand servers, pay-as-you-go)  
- Benefits: Scalability, Cost Savings, Flexibility  
- AWS Global Infrastructure → Regions, Availability Zones, Edge Locations  

---

## What is Cloud Computing?  

- Cloud computing means using the internet to access servers, storage, databases, and services instead of buying and maintaining physical computers.  
- Cloud Computing is the delivery of computing services (like servers, storage, databases, networking, software, and more) over the internet.  
- Instead of storing and processing data on a local computer or server, resources are accessed online from the cloud.  
- **Example:** Instead of buying a server for your website, you rent one from AWS and pay only for the hours you use it.  
- **Main Idea:** It’s like using electricity — you pay for what you use.  

---

## Benefits of Cloud Computing  

- **Scalability:** Increase or decrease resources easily.  
  - *Example:* If your website suddenly gets 1000 visitors, AWS automatically adds servers.  

- **Cost Savings:** Pay-as-you-go; no need to buy expensive hardware.  

- **Flexibility:** Access from anywhere; choose services as needed.  

- **Reliability:** Data is stored across multiple locations.  

- **Security:** AWS provides strong data center security.  

---

## AWS Global Infrastructure  

AWS (Amazon Web Services) has a very large and powerful global network that makes its cloud services fast, reliable, and secure.  

### 1. Regions  
- Geographic locations around the world where AWS has multiple data centers.  
- **Example:** Mumbai (*ap-south-1*), US-East (*N. Virginia*).  
- **Use:** Choose a Region based on where most of your users are to reduce latency (delay).  
- **Fact:** As of 2025, AWS has over 30 regions globally.  
- **Link:** [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)  

### 2. Availability Zones (AZ)  
- Each Region has multiple isolated data centers called Availability Zones.  
- Usually **2 to 6 AZs per region**.  
- If one AZ fails (e.g., power outage), your app can still run from another AZ in the same region.  
- **Explanation:** Think of AZs like branches of the same bank in one city — if one is closed, you can still go to another.  

### 3. Edge Locations  
- Smaller data centers located in many cities around the world.  
- **Use:** Deliver content (like websites, videos, and apps) faster using Amazon CloudFront (CDN).  
- Data is cached closer to users, reducing loading time.  
- **Example:** A user in India watching a video hosted in the US will get it from the nearest Indian Edge Location instead of directly from the US.  

---

## Main Meanings  
- **Regions** → Big areas (like countries/cities).  
- **Availability Zones** → Multiple secure buildings inside each region for high reliability.  
- **Edge Locations** → Small delivery stations close to users for speed.  
