---
title: 'REST API documents'
---

### Release notes 

Information in release notes must provide readers with everything they need to know to understand the change in the software. A lot of business decisions are made based on the information in release notes. Therefore, always write from the user's perspective, not the developer's perspective. The content of release notes answers the following questions:

* What changed because of this feature or resolved issue?
* How was the behavior different before this release?
* Are there changes to the UI?
* Are there changes to the functionality?
* Does an error message appear?
* Was the enhancement based upon customer feedback?

#### Prerequisites and requirements
Because the release notes contain critical information and act as an important communication tool, follow these guidelines so that the documentation is informative and consistent. When authoring release notes, follow the <a href="#AbouttheStyleandStandards">Styles and Standards</a> for many agreed-upon standards, including word choices, use of acronyms, and product names.

#### Headlines
A headline is short, but interesting, and summarizes your release notes. Write headlines in sentence case.

#### Write about new features
When writing about new features, write an enticing paragraph instead of a short, bulleted list. This is an opportunity to market the new feature to customers from a business perspective.

#### Write about resolved issues
When writing about resolved issues, don't call them bugs. Use the term <i>resolved issues</i> because it has a more positive tone. A bulleted list of resolved issues is okay, but ensure that the descriptions make sense.

#### Bulleted lists
For ease of reading, use the same sentence structure throughout a bulleted list. For example, the following items match in sentence structure:
* Feature xyz â€“ This one is really cool.
* Feature abc â€“ This one is really, really, cool.</br>
**Don't add an entry that doesn't match, such as:**
* Feature JKL: it's not so cool

##### Examples
For examples of well-written release notes, see the <a href="/rn/services/document/latest/release_notes.html">Document</a> service's release notes.

#### Filename
The filename for release notes for services and tools is in the format <strong>YYYY-MM-DD-ReleaseNotesServiceName.html.md</strong>. For example, <strong>2016-02-09-ReleaseNotesEmail.html.md</strong>.

#### Version changes
For a new version of an existing service, such as a v2 or v3 release, use the template in this section for your release note, and make sure you include this information:

* The new versionâ€™s benefits and features, including one or more examples of how to use it
* When the old service version becomes deprecated, and how long users have to migrate
* How to migrate to the new service version
* Where to find more information on the new service version, typically a link to the the new version documentation in the Dev Portal

### Release notes template
To write and publish release notes, copy the template shown in this section to the <strong>docu/release_notes</strong> directory, and follow the instructions inside the template. The images shown represent a release note for the Email service.</p>

<p>The first image represents the title box that displays on the <strong>Release Notes</strong> page and illustrates how the Dev Portal uses the <strong>date</strong>, <strong>headline</strong>, <strong>service</strong>, and <strong>official_version</strong> metadata:</p>

<img src="img/RN_headline.png" class="img-click-modal" width="400" vspace="20" alt="Release Note Heading">
<br></br>
<p>The second image represents the actual release note after you click the title box, and illustrates how the Dev Portal uses the <strong>previous_version_shutdown_date</strong> metadata. This image also illustrates how to use Heading 3 as the first heading, followed by the body text:</p>

<img src="img/RN_details.png" class="img-click-modal" width="660" vspace="20" alt="Release Note">

<div class="expand-collapse" data-caption="Download Template">
<p>View or download the Release Notes template:</p><br>

<h5>Template for Services</h5>
---<br>
headline: 'headline'<br>
date: Month dd, yyyy<br>
previous_version_shutdown_date: Month dd, yyyy<br>
official_version: 'version'<br>
---<br>

Features <-- Use H3
<p>Write a paragraph that highlights the main features if this is a new service or product, or describes the new or modified features if it's an update.</p>

<h4>Resolved issues</h4>
<p>List of issues resolved</p>

<p>- - - - - - - - - - - - - - - - - - - comments below - - - - - - - - - - - - - - - - - - -</p><br>

<p>To fill out the metadata:</p>
  <ul>
    <li><strong>headline:</strong> A short, but interesting headline that summarizes your release notes</li>
    <li><strong>date:</strong> The date of the post in the format October 20, 2016</li>
    <li><strong>previous_version_shutdown_date:</strong> The date when the previous version of the service shuts down, in the format May 28, 2016. This information displays in a yellow note panel until two weeks past the shutdown date.</li>
    <li><strong>official_version:</strong> The v version, included in the proxy link</li>
    <li>The title of the release notes automatically generates. It is a combination of <strong>service+official_version</strong>.</li>
  </ul>

<p>Note the following:</p>
  <ul>
    <li>The date in the filename controls where your release notes display in the news feed, and should match the <strong>date</strong> metadata.</li>
    <li>The <strong>previous_version_shutdown_date</strong> metadata displays, in a yellow note panel, when the previous version shut down or will shut down. This shutdown date pertains to the previous <strong>official_version</strong>, such as v1. This information displays until two weeks past the shutdown date.</li>
    <li>Use Heading 3 (h3) for the first heading, whether it's <strong>Features</strong> or <strong>Resolved issues</strong>. Do not use anything bigger than Heading 3.</li>
    <li>If the new feature resulted from a customer request for an enhancement, include this as part of the description in the release note. For example, "The XYZ feature included in this release resulted from customer feedback. It does the following..."</li>
  </ul><br>

<center><button class="btn btn-primary" onClick="location.href='templates/YYYY-MM-DD-ReleaseNotesTemplate.zip'">Download This Template for Services</button><br></center>
</div>
