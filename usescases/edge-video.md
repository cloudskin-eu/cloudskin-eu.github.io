---
layout: page
title: Edge orchestration and video analytics
background: grey
permalink: /usecases/edge-video/
---

<div class="container">
    <div class="col-lg-12 text-center mb-4">
        <h2 class="section-heading text-uppercase">Edge orchestration and video analytics</h2>
    </div>

    <div class="row justify-content-center mb-5">
        <div class="col-lg-10">
            <div class="embed-responsive embed-responsive-16by9 shadow-lg rounded">
                <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/pb_R3PUivLw" title="Edge Video Analytics Use Case" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <h3>Brief introduction</h3>
    <p class="text-justify">In mobility and automotive environments, data must be processed where it is generated to enable real-time decisions. Video analytics for connected vehicles places extreme demands on latency, resilience, and service continuity. CloudSkin enables a seamless cloud-to-edge continuum that allows these workloads to run at the optimal location, ensuring high performance and reliability in dynamic scenarios.</p>

    <div class="row align-items-center mt-4 mb-5">
        <div class="col-md-7 mb-3">
            <div class="hover-zoom">
                <img src="/assets/img/usecases/cars.png" 
                    class="img-fluid rounded shadow-lg" 
                    alt="Connected Cars" 
                    style="width: 100%; transition: transform .3s;">
            </div>
        </div>
        <div class="col-md-5 mb-3">
            <div class="hover-zoom">
                <img src="/assets/img/usecases/dashboard.png" 
                    class="img-fluid rounded shadow-lg" 
                    alt="Analytics Dashboard" 
                    style="width: 100%; max-height: 400px; object-fit: contain; background: #fff; transition: transform .3s;">
            </div>
        </div>
    </div>

    <style>
        .hover-zoom:hover img {
            transform: scale(1.02);
        }
        h3 { margin-top: 40px; border-left: 5px solid #007bff; padding-left: 15px; }
    </style>

    <h3>Introduction of the problem</h3>
    <p class="text-justify">In automotive testing environments, such as racing circuits, we face a critical challenge: video analytics for vehicle detection requires real-time processing. Traditional cloud-only solutions introduce delays that compromise performance and safety. We needed a way to intelligently orchestrate workloads across cloud and edge resources, ensuring applications can migrate dynamically to maintain quality of service under strict latency constraints.</p>

    <h3>How CloudSkin will address the challenge</h3>
    <p class="text-justify">CloudSkin addresses this challenge by enabling intelligent orchestration of video analytics workloads across cloud and edge infrastructures. Using AI-driven decision-making, CloudSkin ensures that applications are dynamically placed and migrated to meet strict latency and service-level requirements. This allows automotive use cases to maintain ultra-low latency and consistent performance even in highly dynamic and mobile environments.</p>

    <h3>How it will work</h3>
    <p class="text-justify">CloudSkin continuously monitors application performance, network conditions, and infrastructure availability. Based on predictive analytics, it anticipates workload behavior and proactively migrates video analytics services between centralized cloud and distributed edge nodes. The NearbyOne orchestrator manages cloud-native services and Kubernetes clusters across multiple sites, ensuring seamless connectivity and service continuity for mobile and distributed deployments.</p>

    <h3>Summary of some results</h3>
    <p class="text-justify">The evaluation of service migration strategies clearly demonstrates the benefits of an intelligent, proactive approach over traditional reactive methods. By anticipating service degradation before quality thresholds are breached, proactive migration enables more timely and effective workload reallocation, significantly improving overall service continuity. The results show that this strategy not only enhances the accuracy of migration decisions, reducing missed opportunities to act, but also minimizes unnecessary reactions. As a consequence, quality-of-service disruptions are shorter and less severe, leading to a more stable operational environment. From a business perspective, the reduction in service degradation and SLA breaches translates directly into improved service quality and lower operational risk, reinforcing proactive orchestration as a key enabler for reliable, cost-efficient cloud-to-edge services.</p>
</div>
<div style="height: 50px;"></div>