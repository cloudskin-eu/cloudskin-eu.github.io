---
layout: page
title: Software Results
background: grey
permalink: /software/
---

<div class="col-lg-12 text-center mb-4">
	<h2 class="section-heading text-uppercase">Software Results</h2>
</div>

<div class="col-lg-12 text-center">
	<table class="table table-striped" style="text-align: left">
		<thead>
			<tr>
				<th style="width: 80%;">Title / Description</th>
				<th style="width: 20%; text-align: center;">Repository</th>
			</tr>
		</thead>
		<tbody>
			{% for item in site.data.sitetext.results.software %}
			<tr>
				<td>{{ item.title }}</td>
				<td style="text-align: center;">
                    <a href="{{ item.url }}" target="_blank">
                        <i class="fab fa-github fa-2x"></i>
                    </a>
                </td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>

<div style="height: 150px;"></div>