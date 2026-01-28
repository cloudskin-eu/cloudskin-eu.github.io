---
layout: page
title: Surgery
background: grey
permalink: /usecases/surgery/
---

<div class="container">
    <div class="col-lg-12 text-center mb-4">
        <h2 class="section-heading text-uppercase">Surgery</h2>
    </div>

    <h3>Brief introduction</h3>
    <p class="text-justify">In minimally invasive surgery, AI-powered video analytics assist surgeons by detecting instruments, recognizing operative phases, and segmenting anatomical structures in real-time. At the National Center for Tumor Diseases (NCT) Dresden, endoscopic cameras generate high-volume video streams that must be processed with low latency while handling sensitive patient data. CloudSkin enables a smart infrastructure for computer-assisted surgery that spans from operating room edge devices to central cloud resources.</p>

    <h3>Introduction of the problem</h3>
    <p class="text-justify">Deploying surgical AI video analytics presents several challenges. First, different AI models have varying software dependencies and hardware requirements, making deployment manual and error-prone. Second, surgical workloads compete for limited edge CPU and GPU resources, where naive allocation leads to poor utilization or degraded performance. Third, surgery rooms exhibit daily usage patterns that cause workload fluctuations - scaling streaming infrastructure up or down can introduce latency spikes that threaten real-time ingestion and inference. Finally, current streaming systems tier data from edge to cloud in a simplistic manner, missing opportunities for in-transit data enrichment and data management.</p>

    <h3>How CloudSkin will address the challenge</h3>
    <p class="text-justify">CloudSkin addresses these challenges through three integrated solutions. For efficient resource allocation, a Kubernetes-based orchestration layer with GPU bin-packing consolidates multiple video streams onto shared GPUs while maintaining real-time performance. For dynamic workloads, an LSTM-based predictive auto-scaling algorithm learns from surgery room usage patterns to provision streaming storage proactively, minimizing latency spikes.</p>

    <h3>How it will work</h3>
    <p class="text-justify">Video streams from operating room endoscopes are ingested via Pravega, a streaming storage system providing durability and elastic scaling. Surgical AI models - packed in unified Docker containers with standardized GStreamer pipelines - process video frames for instrument detection, phase recognition, and liver segmentation. The Kubernetes scheduler uses First-Fit Decreasing bin-packing to place workloads based on profiled CPU and GPU requirements. An LSTM model trained on NCT operating room traces predicts workload fluctuations, enabling proactive scaling of Pravega instances to meet latency SLOs. Nexus streamlets transparently enrich video data during tiering, adding semantic metadata and providing edge-side buffering without impacting real-time inference.</p>

    <h3>Summary of some results</h3>
    <p class="text-justify">CloudSkin’s bin-packing achieves 3x higher workload density (12 concurrent streams vs. 4 baseline), improving GPU utilization from 20% to 50% while maintaining the 30 FPS target. Predictive auto-scaling reduces scaling events by 7x compared to reactive approaches and improves worst-case p90 latency by nearly 6x, keeping 99.9% of requests under 150ms. The Nexus buffering streamlet fully masks storage outages, maintaining 10 MB/s ingestion when native systems stall, while the annotation streamlet enriches video metadata to enable rapid retrieval of specific surgical segments. These results demonstrate that hospitals can support more concurrent computer-assisted surgeries with better resource efficiency, lower latency, and enhanced data management.</p>
</div>
<div style="height: 50px;"></div>