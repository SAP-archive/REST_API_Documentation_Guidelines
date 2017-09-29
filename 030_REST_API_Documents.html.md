## REST API Documentation Guidelines
There are certain documents required when you create a service with REST API so that the purpose and use of the service is clearly stated and easy to understand. With every new release, provide engaging release notes as well, as described in these guidelines.

### Required documents for services
It is a good idea to familiarize yourself with the Service documentation before creating it. Provide each of these documents so that each service is documented consistently, and is easy to find.

##### Descriptor files
Services use the descriptor files such as a RAML file to describe the API in a natural and intuitive way. Create consistent and straightforward definitions in these files for a coherent user experience. Also, include up-to-date examples and clear descriptions. Make the explanations concise and move the more extensive content to the **Details** or **Tutorials** section. The [Style and Standards](010_About_Style_And_Standards.html.md#style-and-standards) guidelines apply when you document your endpoints and methods in the descriptor files:
<ul>
    <li>Focus on the user's task and avoid unnecessary words.</li>
    <li>Use second person, active voice, and present tense.</li>
    <li>Stick to the terminology and format standards.</li>
    <li>Use appropriate articles and punctuation.</li>
</ul>
For example: </br>"Use the <code>/all</code> endpoint to return a list of all tenants for a given client."

#### Overview document
The Overview document is concise and briefly describes the purpose and intended use of the service. Make sure to include the following:

  <ul>
    <li>Describe who might use the service and why.</li>
    <li>List the key features of the service in bullet points. Provide more in-depth information in the <strong>Details</strong> section. Do <i>not</i> explain RESTful API basic functions as a feature of the service.</li>
    <li>Describe how this service relates to other services, and describe any dependencies, including appropriate links to those dependencies.</li>
    <li>Optionally, list business examples.</li>
    <li>Optionally, list any prerequisites with a short description and relevant links to tutorials or documentation.</li>
  </ul>

#### Events document
Write an Events document for services that send events consumed by other services.

First, list the <strong>topic owner client</strong> above the table. This is one per service, such as <strong>hybris.authorization</strong> for the OAuth2 service. Then, in the table, list the event type, a description, the link to the schema, and a payload example. You do not need to explain how to consume the event.

##### Sample Events document

<h5>Events</h5>

<p>The topic owner client is: <strong>hybris.authorization</strong><br><br>

| Type |Description |Schema |Payload example |
| ---- |---------- | ------ | --------------|
| subscriptionCreated | The OAuth2 authorization provider created and processed the subscription.| <a href="https://api.yaas.io/hybris/schema/v1/hybris/subscriptionCreated_v1">subscriptionCreated_v1</a> | `{"id":"MDF23X45", "subscriber":{"id":"testproject", "org":"532506aegf6ed545y397589u"}, "package":{"id":"3kztl5ruyevu", "version":"450a4fb2a16ef916704f8925", "provider":{"id":"toad", "org":"44d72ad9cb5e48d2d82d04a2"}, "includedServices":[{"id":"moqsowxp1v78", "name":"product"}, {"id":"bgpbokbmzga6","name":"somename"}]}, "validFrom":"2015-11-03T12:22:59.569+0000"}` |

Each event includes the <strong>schema</strong> key in its metadata section. This allows you to identify the version of the payload that the event contains.

#### Details document
The Details documentat contains more in-depth details about the service. The details are listed in a logical order, starting with the architecture, scopes, and limitations of the service.

  <ul>
    <li>Include a diagram of the service to illustrate the service execution flow, especially for complex services or a mashup.</li>
    <li>Define scopes for all services. List the information in a table, including the name of the scope and a short description of what the scope does.</li>
    <li>List any limitations of the service.</li>
  </ul>

Give more details about the main features listed in the Overview, and any other features not listed. Each feature is described in a separate heading, and more complex details in sub-headings within the feature. Make sure to include the following:
  <ul>
    <li>Describe the service in detail, including who would use it, when, and why.</li>
    <li>Include relevant use cases, describing any real world problems the service can solve.</li>
    <li>Add any relevant links to the tutorials or FAQs.</li>
    <li>List any considerations, tricks, or workarounds that help users make the most of using the service.</li>
  </ul>

#### Tutorials
Tutorials in your documentation explain and demonstrate in step-by-step fashion how to use the service. The titles of your tutorials should be succinct. Do NOT include "How To" in the title, because it is redundant. Use titles that start with action verbs in the Tutorials section to clearly indicate what action is performed

<p>The tutorials are targeted at developers with different amounts of experience. For that reason, structure the tutorials so that a beginner can follow the most basic steps, and more experienced developers can learn more fine-grained details, such as troubleshooting or more use cases. Be sure to include the following:</p>

<ul>
  <li>Title – Give the tutorial a descriptive title, without the words "How To".</li>
  <li>Introduction – Introduce each tutorial separately, or as a whole. Be sure to explain any common use-case theme, such as a certain store name with certain products for sale. Also, state the objective of the tutorials and any prerequisites.</li>
  <li>Step-by-step – Include detailed steps in a quick start guide, or create detailed, interactive steps.</li>
  <li>Request and response examples - If you include a sample request, list optional and required attributes separately in the request body.</li>
  <li>Errors – Include the description of the error codes.</li>
  <li>Optional troubleshooting - Besides providing the error codes, give tips on how to troubleshoot a problem after receiving an error.
  <li>Optional use cases – Show more than one use case to highlight different features.</li>
</ul>

#### Security document
The Security document is required only for services with data protection requirements that are not supported locally. This document contains all of the details needed to ensure data privacy, which varies from service to service.

Refer to the documentation for the <a href="https://devportal.yaas.io/services/us/document/latest/">Document service</a> and the <a href="https://devportal.yaas.io/services/us/documentbackup/latest/">Document Backup service</a> for examples.

### Release notes 
Information in release notes must provide readers with everything they need to know to understand the change in the software. A lot of business decisions are made based on the information in release notes. Therefore, always write from the user's perspective, not the developer's perspective. The content of release notes answers the following questions:

* What changed because of this feature or resolved issue?
* How was the behavior different before this release?
* Are there changes to the UI?
* Are there changes to the functionality?
* Does an error message appear?
* Was the enhancement based upon customer feedback?

#### Prerequisites and requirements
Because the release notes contain critical information and act as an important communication tool, follow these guidelines so that the documentation is informative and consistent. When authoring release notes, follow the [Style and Standards](010_About_Style_And_Standards.html.md#style-and-standards) for many agreed-upon standards, including word choices, use of acronyms, and product names.

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

<br>[< PREV](020_Syntax_Guidelines.html.md) | [NEXT>](040_More_Documentation.html.md)
