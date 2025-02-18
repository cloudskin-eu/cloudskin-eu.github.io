---
layout: page
background: grey
---

<div class="col-lg-12 text-center mb-4">
	<h2 class="section-heading text-uppercase">Cloudskin project review</h2>
</div>

#### Review Agenda

__Meeting Subject__: Project midterm review

__Venue__: Online  - Microsoft Teams

__Date__: July 11, 2024

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
			{% for event in site.data.sitetext.review.events %}
			<tr>
				<td>{{ event.time }}</td>
				<td>{{ event.subject }}</td>
				<td>{{ event.duration }}</td>
				<td>{{ event.lead }}</td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
	* We assume reviewers watched videos previously
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
			{% for item in site.data.sitetext.review.slides %}
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
			{% for video in site.data.sitetext.review.videos %}
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

<!--
#### Summary reports
 <div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left; white-space: pre;">
		<thead>
			<tr>
				<th>Partner short name</th>
				<th>Partner</th>
				<th>PDF</th>
			</tr>
		</thead>
		<tbody>
			{% for summary in site.data.sitetext.review.summaries %}
			<tr>
				<td>{{ summary.shortname }}</td>
				<td>{{ summary.partner }}</td>
				<td><a href="{{ summary.link }}"><i class="fas fa-external-link-alt"></i></a></td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div> -->

#### Software results
<div class="col-lg-12 text-center mt-4 mb-4">
	<table class="table table-striped" style="text-align: left;">
		<thead>
			<tr>
				<th>Title</th>
				<th>Description</th>
				<th>Repository</th>
			</tr>
		</thead>
		<tbody>
			{% for artifact in site.data.sitetext.review.artifacts %}
			<tr>
				<td>{{ artifact.title }}</td>
				<td>{{ artifact.description }}</td>
				<td><a href="{{ artifact.link }}"><i class="fas fa-external-link-alt"></i></a></td>
			</tr>
			{% endfor %}
		</tbody>
	</table>
</div>