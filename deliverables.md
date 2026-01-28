---
layout: page
title: Deliverables
background: grey
permalink: /deliverables/
---

<div class="col-lg-12 text-center mb-4">
	<h2 class="section-heading text-uppercase">Deliverables</h2>
</div>

<div class="container">
    <div class="d-flex align-content-around flex-wrap justify-content-center">
        {% for deliverable in site.data.sitetext.results.deliverables %}
        <div class="m-2">
            <div class="card" style="width: 18rem;">
                <div class="card-body">
                    <h5 class="card-title">{{ deliverable.title }}</h5>
                    <h6 class="card-subtitle mb-2 text-muted">{{ deliverable.subtitle }}</h6>
                    <a href="{{ deliverable.file }}" class="card-link"><i class="fas fa-file-pdf"></i> PDF</a>
                </div>
            </div>
        </div>
        {% endfor %}
    </div>
    <div class="col-lg-12 text-center mt-4">
        <i>* Deliverables pending approval</i>
    </div>
</div>

<div style="height: 100px;"></div>