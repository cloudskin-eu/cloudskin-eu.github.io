---
layout: page
title: Metabolomics
background: grey
permalink: /usecases/metabolomics/
---

<div class="container">
    <div class="col-lg-12 text-center mb-4">
        <h2 class="section-heading text-uppercase">Metabolomics</h2>
    </div>

    <div class="row justify-content-center mb-5">
        <div class="col-lg-10">
            <div class="embed-responsive embed-responsive-16by9 shadow-lg rounded">
                <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/islDuT3ZlJs" title="Metabolomics Use Case" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <h3>Brief introduction</h3>
    <p class="text-justify">Modern metabolomics relies on large-scale analysis of mass spectrometry images to support biomedical research. The METASPACE platform provides automated image annotation using artificial intelligence, helping researchers distinguish meaningful biological signals from artefacts in complex datasets.</p>

    <div class="row mb-4">
        <div class="col-md-6 mb-3">
            <img src="/assets/img/usecases/metabolomics.png" class="img-fluid rounded shadow" alt="Metabolomics Interface 1">
        </div>
        <div class="col-md-6 mb-3">
            <img src="/assets/img/usecases/metabolomics2.png" class="img-fluid rounded shadow" alt="Metabolomics Interface 2">
        </div>
    </div>

    <h3>Introduction of the problem</h3>
    <p class="text-justify">The demand for image analysis in METASPACE is highly unpredictable: some days involve processing tens of thousands of images, while at other times there is almost no activity. This situation is similar to a concert ticket website, which may be almost idle most of the time but suddenly experiences massive traffic when tickets for a popular artist go on sale. Traditional cloud systems must either keep resources running all the time or react too slowly when demand suddenly spikes.</p>
    <p class="text-justify">In METASPACE, the previous solution kept computing resources permanently active and only scaled up after high demand was detected. This led to unnecessary costs during idle periods and long waiting times when many images arrived at once. Furthermore, sensitive images from private companies such as AstraZeneca had to be processed in the public cloud without strong privacy guarantees.</p>

    <h3>How CloudSkin will address the challenge</h3>
    <p class="text-justify">CloudSkin introduces a smarter approach that combines cloud and edge computing. It uses serverless cloud functions to scale instantly and cost-efficiently when large numbers of non-sensitive images need processing, while sensitive data is handled securely on local edge infrastructure using confidential computing. This removes idle costs, improves response times, and protects sensitive information.</p>

    <h3>How it will work</h3>
    <p class="text-justify">For this use case, CloudSkin provides <strong>Lithops Serve</strong>, an intelligent serving layer that automatically manages where and how image analysis runs. For non-sensitive metabolomics images, Lithops Serve executes AI inference using serverless cloud functions, which can rapidly scale to thousands of parallel tasks and shut down when no work is present, ensuring fast processing at low cost.</p>
    <p class="text-justify">When images contain sensitive data, Lithops Serve transparently redirects computation to on-premises edge resources protected by <strong>SCONE</strong>. SCONE runs the analysis inside hardware-based secure enclaves, so images and model data remain encrypted and confidential even during execution. By coordinating serverless cloud resources with secure edge execution, CloudSkin delivers efficient, scalable, and privacy-preserving metabolomics image analysis.</p>

    <h3>Summary of some results</h3>
    <p class="text-justify">With CloudSkin, image analysis jobs complete up to tens of times faster than before while costing less overall. The system achieves much higher throughput during peak demand and eliminates wasted resources during idle periods. At the same time, privacy tests confirm that sensitive images cannot be reconstructed from protected processing, demonstrating strong confidentiality alongside high performance.</p>
</div>
<div style="height: 50px;"></div>