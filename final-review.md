---
layout: page
background: grey
permalink: /final-review/
---

<div class="col-lg-12 text-center mb-4">
	<h2 class="section-heading text-uppercase">Cloudskin final review</h2>
</div>

#### Review Agenda

__Meeting Subject__: Project Final Review

__Venue__: Barcelona Supercomputing Centre (BSC)

__Date__: February 19, 2026

__Chair__: Marc Sánchez-Artigas (Coordinator)


<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left; white-space: pre;">
		<thead>
			<tr>
				<th>Time</th>
				<th>Subject</th>
				<th>Time (mins)</th>
				<th>Lead partner</th>
			</tr>
		</thead>
		<tbody>
			{% for event in site.data.sitetext.final_review.events %}
			<tr>
				<td>{{ event.time }}</td>
				<td>{{ event.subject }}</td>
				<td>{{ event.duration }}</td>
				<td>{{ event.lead }}</td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>

#### Review Slides
<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left; white-space: pre;">
		<thead>
			<tr>
				<th>Document</th>
				<th>PDF</th>
			</tr>
		</thead>
		<tbody>
			{% for item in site.data.sitetext.final_review.slides %}
			<tr>
				<td>{{ item.title }}</td>
				<td><a href="{{ item.link }}"><i class="fas fa-external-link-alt"></i></a></td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>

#### Videos and presentations
<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left; white-space: pre;">
		<thead>
			<tr>
				<th>Title</th>
				<th>Video</th>
				<th>Slides</th>
			</tr>
		</thead>
		<tbody>
			{% for video in site.data.sitetext.final_review.videos %}
			<tr>
				<td>{{ video.title }}</td>
				<td><a href="{{ video.video }}"><i class="fas fa-external-link-alt"></i></a></td>
				<td> {% if video.slides != "#" %} <a href="{{ video.slides }}"><i class="fas fa-external-link-alt"></i></a> {% endif %}</td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>


#### Deliverables
<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left; white-space: pre;">
		<thead>
			<tr>
				<th>Title</th>
				<th>PDF</th>
			</tr>
		</thead>
		<tbody>
			{% for deliverable in site.data.sitetext.results.deliverables %}
			<tr>
				<td>{{ deliverable.title }}  {{ deliverable.subtitle }}</td>
				<td><a href="{{ deliverable.file }}"><i class="fas fa-external-link-alt"></i></a></td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>

#### Publications
<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left">
		<thead>
			<tr>
				<th>Title</th>
				<th>Venue</th>
				<th>Link</th>
				<th>DOI</th>
			</tr>
		</thead>
		<tbody>
			{% for publication in site.data.sitetext.results.publications %}
			<tr>
				<td>{{ publication.title }}</td>
				<td>{{ publication.journal-conf }}</td>
				<td>
                    {% if publication.url contains "http" %}
                        <a href="{{ publication.url }}" target="_blank"><i class="fas fa-external-link-alt"></i></a>
                    {% else %}
                        <span class="text-muted" style="font-size: 0.8em;">{{ publication.url }}</span>
                    {% endif %}
                </td>
				<td> {% if publication.doi != "" %} <a href="https://doi.org/{{ publication.doi }}">{{ publication.doi }}</a> {% endif %} </td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>

#### Software results
<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left;">
		<thead>
			<tr>
				<th>Title and description</th>
				<th>Repository</th>
			</tr>
		</thead>
		<tbody>
			{% for artifact in site.data.sitetext.final_review.artifacts %}
			<tr>
				<td>{{ artifact.title }}</td>
				<td><a href="{{ artifact.link }}"><i class="fas fa-external-link-alt"></i></a></td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>
