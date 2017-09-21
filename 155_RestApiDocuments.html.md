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
Because the release notes contain critical information and act as an important communication tool, follow these guidelines so that the documentation is informative and consistent. When authoring release notes, follow the [Styles and Standards](001_Overview.html.md) for many agreed-upon standards, including word choices, use of acronyms, and product names.

##### Headlines
A headline is short, but interesting, and summarizes your release notes. Write headlines in sentence case.

##### Write about new features
When writing about new features, write an enticing paragraph instead of a short, bulleted list. This is an opportunity to market the new feature to customers from a business perspective.

##### Write about resolved issues
When writing about resolved issues, don't call them bugs. Use the term <i>resolved issues</i> because it has a more positive tone. A bulleted list of resolved issues is okay, but ensure that the descriptions make sense.

##### Bulleted lists
For ease of reading, use the same sentence structure throughout a bulleted list. For example, the following items match in sentence structure:
* Feature xyz - This one is really cool.
* Feature abc - This one is really, really, cool.</br>
**Don't add an entry that doesn't match, such as:**
* Feature JKL: it's not so cool

##### Version changes
For a new version of an existing service, such as a v2 or v3 release, make sure you include this information in your release note:

* The new version's benefits and features, including one or more examples of how to use it
* When the old service version becomes deprecated, and how long users have to migrate
* How to migrate to the new service version
* Where to find more information on the new service version, typically a link to the the new version documentation

### Services

This page lists documents for services. Provide each of these documents so the purpose and use of each service is easy to understand. It is a good idea to familiarize yourself with the Service documentation before creating it. When writing any documentation, including API Documentation, follow the [Styles and Standards](001_Overview.html.md).

##### RAML file
Services can use the RESTful API Modeling Language (RAML) to describe their own APIs in a natural and intuitive way. Follow the <a href="https://devportal.yaas.io/tools/apiguidelines">API Guidelines</a> and create consistent and straightforward RAML API definitions.<br/>

For a coherent user experience, include up-to-date examples and clear descriptions. Make the explanations concise and move the more extensive content to the **Details** or **Tutorial** section. The [Styles and Standards](001_Overview.html.md) guidelines apply when you document your endpoints and methods in the RAML file:
<ul>
    <li>Focus on the user's task and avoid unnecessary words.</li>
    <li>Use second person, active voice, and present tense.</li>
    <li>Stick to the preferred terminology and format standards.</li>
    <li>Use appropriate articles and punctuation.</li>
</ul>
For example: </br>"Use the <code>/all</code> endpoint to return a list of all tenants for a given client."

#### Overview document

The Overview document is concise and briefly describes the purpose and intended use of the service. Use the proper metadata as described in the <a href="/tools/documentationsdk/#Metadata"> Metadata</a> section of the Documentation SDK. Make sure to include the following:

  <ul>
    <li>Describe who might use the service and why.</li>
    <li>List the key features of the service in bullet points. Provide more in-depth information in the <strong>Details</strong> section. Do <i>not</i> explain RESTful API basic functions as a feature of the service.</li>
    <li>Describe how this service relates to other services, and describe any dependencies, including appropriate links to those dependencies.</li>
    <li>Optionally, list business examples.</li>
    <li>Optionally, list any prerequisites with a short description and relevant links to tutorials or documentation.</li>
  </ul>

#### API Console and API Reference documents

If you follow the instructions to register your service in the <a href="/tools/documentationsdk/">Documentation SDK</a>, the following occurs:
  <ul>
    <li>The API Console link displays automatically in a yellow button at the top of the API documentation.</li>
    <li>The API Reference content and navigation node automatically generates. Even though this is automatically generated, check the RAML file to ensure it is up to date with samples and clear descriptions.</li>
    <li>A link to the API Reference appears at the bottom of each tutorial for more information about error messages, so make sure the RAML file also describes error messages.
    <li>The RAML file is available at the top of the API documentation for users to copy or download. Make sure to put the <code>displayName:Managing Data</code> description under the root <strong>/resource</strong> in the RAML file. This display name is then visible instead of the root resource name.</li>
  </ul>

<div class="panel note">If your service does not expose its API, set the <strong>raml</strong> attribute to <code>false</code> in the registry JSON file, and neither the API Console or API Reference displays in the documentation. Also, set the <strong>baseUri</strong> attribute to <code>Not applicable</code> to display this text instead of the link to the RAML file. See the JSON templates for more details. For an example, see the <a href="/services/profileenricher/latest/index.html">Profile Enricher</a> documentation.</div>

If the API Console or API Reference is <i>not</i> available after following the registration instructions, check the following:
  <ul>
    <li>The <strong>baseURI</strong> link to the service provided in the Dev Portal registry</a> exists and is up to date with your service version.</li>
    <li>By default, the Dev Portal collects the first RAML file found in your project and uses it for generation. If you are using more then one RAML file in your project, specify which file to use in the registry.</li>
    <li>When including hybris traits in your RAML file, use the full URL including the HTTP or HTTPS protocol.</li>
  </ul>

### Events document

The Events document is required for services that use the PubSub service to broadcast events that other services can consume.

First, list the <strong>topic owner client</strong> above the table. This is one per service, such as <strong>hybris.authorization</strong> for the OAuth2 service. Then, in the table, list the event type, a description, the link to the schema, and a payload example. You do not need to explain how to consume the event.

<div class="expand-collapse" data-caption="See the Events template">

<p>The Events template is printed below, or you can download the template:</p><br>
  <p>- - - - - - - - - - - - - - - - - copy these lines below - - - - - - - - - - - - - - - - -</p><br>
---<br>
title: 'Events'<br>
---<br>
  <p>
    `<%- @partial('template_events') %>`
  </p><br>
<p>The topic owner client is:</p>
Event | Description | Schema | Payload Example<br>
------------|----------|----------|----------|----------<br>
Event | Description | Schema | Payload Example<br>
<br><br/>
<p>
  `<%- @partial('template_events_2') %>`
</p>
<p>- - - - - - - - - - - - - - - - - - - comments below - - - - - - - - - - - - - - - - - - -</p><br>
<p>To fill out the metadata above:<br>
title: It must say 'Events'.<br>
</p>
<p>Leave the partials shown in the preceding table as they are. They contain a link to the PubSub documentation and information about the schema key of the event.</p>
<p>List the topic owner client, such as <strong>hybris.authorization</strong>.</p>
<p>The top line in the table shows the column headings. Leave them as is.</p>
<p>Replace the bottom line in the table with the event type, description, link to the schema, and a payload example:</p>
  <ul>
    <li>Event type – This is always listed in past tense, such as <strong>subscription-created</strong>.</li>
    <li>Description – A short description of your event, such as <strong>The OAuth2 authorization provider created and processed the subscription.</strong></li>
    <li>Schema – A link to the schema, such as <a href="https://api.yaas.io/hybris/schema/v1/hybris/subscriptionCreated_v1">subscriptionCreated_v1</a>.</li>
    <li>Payload Example – Provide an example of the event payload, as shown in the following sample.</li>
<br>

   <center><button class="btn btn-primary" onClick="location.href='templates/Events.zip'">Download This Template</button><br></center>
</div>

<div class="expand-collapse" data-caption="See a Sample">
<section id="Events" class="group">

<h1>Events</h1>

<div class="panel tip events">
For more information about consuming these events, see the <a href="/services/pubsub/latest/index.html">PubSub</a> documentation.
</div>

<p>The topic owner client is: <strong>hybris.authorization</strong>

<table>
<thead>
<tr>
<th>Type</th>
<th>Description</th>
<th>Schema</th>
<th>Payload Example</th>
</tr>
</thead>
<tbody>
<tr>
<td>subscriptionCreated</td>
<td>The OAuth2 authorization provider created and processed the subscription.</td>
<td><a href="https://api.yaas.io/hybris/schema/v1/hybris/subscriptionCreated_v1">subscriptionCreated_v1</a></td>
<td><pre><code>{"id":"MDF23X45","subscriber":{"id":"testproject","org":"532506aegf6ed545y397589u"},"package":{"id":"3kztl5ruyevu","version":"450a4fb2a16ef916704f8925","provider":{"id":"toad","org":"44d72ad9cb5e48d2d82d04a2"},"includedServices":[{"id":"moqsowxp1v78","name":"product"},{"id":"bgpbokbmzga6","name":"somename"}]},"validFrom":"2015-11-03T12:22:59.569+0000"}</code></pre></td>
</tr>
</tbody>
</table>

<div class="panel tip events">
Each event includes the <strong>schema</strong> key in its metadata section. This allows you to identify the version of the payload that the event contains.
</div>

</div>

<div class="panel tip events">
If your payload is really long, use the following template.
<div class="expand-collapse" data-caption="See a Sample">
  ```
  ---
  title: 'Events'
  ---

   `<%- @partial('template_events') %>`
  <p>The topic owner client is:</p>

     <table>
     <!-- Header -->
       <tr>
       <th>Event</th>
       <th>Description</th>
       <th>Schema</th>
       <th>Payload Example</th>
      </tr>
     <!-- End of a header -->

     <!-- First row -->
     <tr>
       <td>Your Event Type</td>
       <td>Your Description</td>
       <td>Your Schema 1 Name</td>
       <td>
       <div class="expand-collapse" data-caption="Your Payload Example"> Copy Payload example here </div>
      </td>
    </tr>
   <!-- End of a first row -->

   <!-- Second row -->
      <tr>
        <td>Your Event Type 2</td>
        <td>Your Description 2</td>
        <td>Your Schema 2 Name</td>
        <td>
        <div class="expand-collapse" data-caption="Your Payload Example 2"> Copy Payload example 2 here </div>
        </td>
      </tr>
     <!-- End of a second row -->

     </table>

  `<%- @partial('template_events_2') %>`

  ```

</div>
</div>

### Details document

The Details documentation contains more in-depth details about the service. Use the proper metadata as described in the <a href="/tools/documentationsdk/#Metadata"> Metadata</a> section of the Documentation SDK. The details are listed in a logical order, starting with the architecture, scopes, and limitations of the service.

  <ul>
    <li>Include a diagram of the service to illustrate the service execution flow, especially for complex services or a mashup.</li>
    <li>Define scopes for all services. List the information in a table, including the name of the scope and a short description of what the scope does.</li>
    <li>List any limitations of the service.</li>
  </ul>

Give more details about the main features listed in the Overview, and any other features not listed. Each feature is described in a separate heading, and more complex details in sub-headings within the feature. Make sure to include the following:
  <ul>
    <li>Describe the service in detail, including who would use it, when, and why.</li>
    <li>Include relevant use cases, describing any real world problems the service can solve.</li>
    <li>Explain any YaaS terms using the glossary feature, and add any relevant links to the tutorials or FAQs.</li>
    <li>List any considerations, tricks, or workarounds that help users make the most of using the service.</li>
  </ul>

### Tutorials
Tutorials in your documentation explain and demonstrate in step-by-step fashion how to use the service. Because the website navigation indicates that these documents are tutorials, the titles should be succinct. Do NOT include "How To" in the title.

<p>The tutorials are targeted at developers with different amounts of experience with YaaS. For that reason, structure the tutorials so that a beginner can follow the most basic steps, and more experienced developers can learn more fine-grained details, such as troubleshooting or more use cases. Be sure to include the following:</p>

<ul>
  <li>Title – Give the tutorial a descriptive title, without the words "How To".</li>
  <li>Introduction – Introduce each tutorial separately, or as a whole. Be sure to explain any common use-case theme, such as a certain store name with certain products for sale. Also, state the objective of the tutorials and any prerequisites.</li>
  <li>Step-by-step – Include detailed steps in a quick start guide, or create detailed, interactive steps.</li>
  <li>Request and response examples - If you include a sample request, list optional and required attributes separately in the request body.</li>
  <li>Errors – At the end of the tutorial, use the <strong>errors_global.html.md</strong> partial which inserts the wording, "For more information about error codes, see the API Reference."</li>
  <li>Optional troubleshooting - Besides providing the error codes, give tips on how to troubleshoot a problem after receiving an error.
  <li>Optional use cases – Show more than one use case to highlight different features.</li>
</ul>

### Security document
The Security document is required only for services with data protection requirements that are not supported locally. This document contains all of the details needed to ensure data privacy, which varies from service to service.

Refer to the documentation for the <a href="https://devportal.yaas.io/services/us/document/latest/">Document service</a> and the <a href="https://devportal.yaas.io/services/us/documentbackup/latest/">Document Backup service</a> for examples.

### Glossary document
Use the Glossary to define terms that are specific to each service. The Glossary generates at the bottom of each API document, after the tutorials. A glossary term should be succinct, and no more than a sentence long so that it displays nicely as a tooltip.

To add a term to the glossary:
  <ul>
    <li>Create the <strong>docu/partials</strong> directory if it doesn’t already exist.</li>
    <li>In the <strong>partials</strong> directory, create an HTML file in the form, <strong>servicename_term.html</strong>. For example: <strong>avalaratax_avalara.html</strong></li>
    <li>Use only the metadata provided in the template, and note the spaces after each <code>:</code>.

By default, a term in the glossary table renders exactly how it is typed in the <strong>term</strong> metadata. To render the term with an initial capital letter instead, change the <strong>lock_case</strong> metadata to <code>true</code>. For example:

<code>term: mixin</code><br>
<code>lock_case: false</code> (default) = mixin<br>
or<br>
<code>lock_case: true</code> = Mixin<br>

After creating a partial for the glossary term, you can use it in your documentation with the partial code, as described in the <a href="/tools/documentationsdk/#ReuseContent">Reuse Content</a> section of the Documentation SDK. For example, if you include <code>&lt;%- @partial('avalaratax_avalara') %&gt;</code> in your document, the result is:<a class="btn btn-link" data-toggle="tooltip" data-placement="top" title="A company that provides services for sales tax management.">Avalara</a>

Any documents containing partials must have a <code>.eco</code> extension. For example:
<strong>overview.html.eco</strong> or <strong>overview.html.md.eco</strong>.

<div class="expand-collapse" data-caption="See the Glossary template">
The Glossary template is printed below, or you can download the template:<br/>
<br/>

- - - - - - - - - - - - - - - - - copy these lines below - - - - - - - - - - - - - - - - -<br/>
<br/>
---<br/>
term: The term you want to add to the glossary<br/>
description: A short description of your term<br/>
lock_case: An optional field, to control the case of your term in the glossary. The default setting is <code>false</code>, which renders the case exactly as it is written above. The <code>true</code> setting renders the term with an initial capital, no matter how appears in the partial.<br/>
---<br/>
<br/>
- - - - - - - - - - - - - - - - - - - comments below - - - - - - - - - - - - - - - - - - -<br/>

There is no content other than the metadata above.<br/>

<center>or</center>
<center>
<button class="btn btn-primary" onClick="location.href='templates/Glossary.zip'">Download This Template</button><br/></center>
</div>

<div class="expand-collapse" data-caption="See a Sample">

<br/>
---<br>
term: mixin<br>
description: Customizable definition of additional properties for the product. One product can use many mixins, and many products can use one mixin.<br>
---<br>

</div>
