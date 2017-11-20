## About the Style and Standards

This guide explains the documentation requirements and provides guidelines to ensure your documentation follows the <a href="#style-and-standards">Style and Standards</a>.

It is important to follow these requirements and guidelines so that there is consistency throughout all of the documentation. The goal is to have all contributors write in the same way to ensure a uniform flow throughout the website. For example:<br><br>
<img src="img/DocGuidelinesOview.png" width="1400" height="400" alt="Consistency is key.">

These basic principals are explained in more detail in this guide, so read on for further information.

### Definition of done

The product is not done until the documentation is done. For instance, if you have a new service, feature, or solution to publish, you also need adequate documentation to release at the same time. This ensures readers fully understand the product and how to use it.

Review documentatoin before publishing to ensure the content meets the requirements and guidelines.

### Style and standards

The Style and Standards topic describes the grammar and preferred word choices, and ensures that your content meets the requirements for publication. Because this guide relies on the <a href="http://www.amazon.com/Microsoft-Manual-Style-4th-Edition/dp/0735648719">Microsoft Manual of Style - 4th Edition</a> (MMoS), this page documents only those standards that are applied differently, or that the MMoS does not address. Search this page for any term to read about the standard.

#### Grammar

[Active voice](010_About_Style_And_Standards.html.md#active-voice) | [Tenses](010_About_Style_And_Standards.html.md#tenses) | [Imperative Mood](010_About_Style_And_Standards.html.md#imperative-mood) | [Pronouns](010_About_Style_And_Standards.html.md#pronouns) | [Serial commas](010_About_Style_And_Standards.html.md#serial-commas) | [Colon vs. semicolon](010_About_Style_And_Standards.html.md#colon-vs-semicolon) | [Articles](010_About_Style_And_Standards.html.md#articles) | [Terminology](010_About_Style_And_Standards.html.md#terminology)

##### Active voice
Active voice is clear and concise, and avoids misinterpretation. It's also easier for non-native speakers to understand. Passive voice is weak and indirect, uses more words, and can lead to misinterpretation because it reverses the logical order of events. The proper order for sentence structure is subject, verb, and sometimes mentions an object. Passive voice uses object, passive verb, and sometimes the subject. Also, active voice uses the present tense of verbs which is more desirable than using past tense.

:white_check_mark: The endpoint path includes your service name.<br>
:no_entry: Your service name is to be included in the endpoint path.

For more information, see the [Write in Active Voice](https://github.com/YaaS/REST_API_Documentation_Guidelines/wiki/002-Write-in-Active-Voice) blog post.

##### Tenses

Use present tense. In technical writing, present tense is easier to read than past or future tense. Simple verbs are easier to read and understand than complex verbs, such as verbs in the progressive or perfect tense.

The more concise and straightforward you can be, the better.

:white_check_mark: If the information does not match, an error message appears.<br>
:no_entry: If the information does not match, an error will appear.

##### Imperative Mood

Use the imperative mood to write instructional documentation such as procedures and tutorials. The imperative mood tells the reader, directly, to do something. Other moods can imply optional behavior when you might not intend to present an action as optional.

For example, in instructions for uploading documents, clicking Upload is not a suggested, optional action. If the document provides instructions for how to upload documents, assume the readers wants to perform that action. Do not use language such as, "If you want to upload a document, you can click Upload" or, "By clicking Upload, you can choose how many documents you want to upload." Instead write, "Click Upload and select one or more documents."

:white_check_mark: Click **Run** to execute the program.<br>
:no_entry: The user should click **Run** to execute the program.

##### Pronouns

Use the second person and the pronouns "you," "your," and "yours" to speak directly to the reader. Do not use the first person pronouns "we," "us," or "let's."

:white_check_mark: You can save your files in the cloud or on your local machine.<br>
:no_entry: Let's save our files in the cloud or on our local machine.

##### Serial commas

Use serial commas. A missing serial comma can create confusion about whether the statement applies to each list item individually, or whether the last two items are connected.

:white_check_mark: In your request, include the values for the request date, name, and ID.<br>
:no_entry: In your request, include the values for the request date, name and ID.

For more details, see the [Serial Commas: The Price of Omission]( https://github.com/YaaS/REST_API_Documentation_Guidelines/wiki/004-Serial-Commas-The-Price-of-Omission) blog post.

##### Colon vs. semicolon

Use colons and semicolons sparingly. Use the colon ( : ) to introduce a list of things. The items after a colon are not complete sentences by themselves. The semicolon ( ; ) separates two distinct clauses within one sentence. The phrase after a semicolon is a complete sentence.

If the sentence needs a colon but does not need a bulleted list, consider rewriting the sentence to avoid using a colon.
If the sentence has a semicolon, try to separate it into two different sentences, or find a cleaner way to combine them into one sentence.
See the examples for ways to write the same sentence with and without a colon or semicolon. The preferred method for such a sentence is without a colon or semicolon.

:white_check_mark: Of my three brothers, John is my favorite.<br>
:no_entry: I have three brothers: John is my favorite.<br>
:no_entry: There are three brothers in the family; John is my favorite.

##### Articles

Always verify the use of the articles "a", "an", and "the" where appropriate. Use "the" when you are talking about a specific example. Use "a" when you are talking about something non-specific or hypothetical.

:white_check_mark: Use the service to remove an item from a cart. In this tutorial, create a cart item and then delete the item from the cart.<br>
:no_entry: Use the service to remove an item from a cart. In this tutorial, create a cart item and then delete an item from a cart.

For more information, see the [Articles in English Grammar](https://github.com/YaaS/REST_API_Documentation_Guidelines/wiki//005-Articles-in-English-Grammar) blog post.

##### Terminology
Search this section for any terminology problem you struggle with. Click on a given term or expression to expand the view and read about the standards in detail.<br>

<details> 
  <summary> American English vs. British English </summary>
	<br>
  <p>
   Use American English. Do not use British spelling in the documentation.<br>
	   
   <strong>Example:</strong> The color of the message changes from blue to red if there are errors.
  </p>
</details>
<br> 
<details> 
  <summary> app vs. application </summary>
	<br>
  <p>
   Use "application."<br>
	   
   <strong>Example:</strong> You can create a new application with the name of your choice.
  </p>
</details>
<br> 
<details> 
  <summary> as shown below </summary>
	<br>
  <p>
  Use "as shown in the example" instead of indicating direction, such as "above" or "below", whenever possible. This helps to ensure that there are no issues if the text is modified, rewritten, or reorganized. You can also write "the following" or "the preceding."<br>
	   
   <strong>Example:</strong> In your request, supply the values for the following parameters:
  </p>
</details>
<br>
<details> 
  <summary> back end vs. backend vs. back-end </summary>
	<br>
  <p>
   Per the MMoS, use a more specific term when possible, such as server, operating system, database, or network. However, if you must use this term, use back end, two words, no hyphen, as a noun. Use back-end, hyphenated, as an adjective to modify a noun. Do not use "backend.".<br>
	   
   <strong>Example 1:</strong> Set up accounts in your back-end system with command line requests.<br>
   <strong>Example 2:</strong> Configure the application on the back end.
  </p>
</details>
<br> 

<br>
<table class="table table-striped table-glossary techne-table">
<thead>

  <tr>
   <th>
   Item
   </th>
   <th>
   Standard
   </th>
      <th>
   Example
   </th>
  </tr>
</thead>

 <tr>
  <td>
  <p><a id="americanEnglish"></a>American English vs. British English</p>
  </td>
  <td>
  <p>Use American English. Do not use British spelling in the documentation.</p>
  </td>
  	<td>
  	<ul>
  		<li>The color of the message changes from blue to red if there are errors.</li>
  	</ul>
	</td>
 </tr>

<tr>
  <td>
  <p><a id="app"></a>app vs. application</p>
  </td>
  <td>
  <p>Use &quot;application.&quot;</p>
  </td>
  	<td>
    <ul>
    	<li>
	You can create a new application with the name of your choice.
    	</li>
    </ul>
	</td>
 </tr>

  <tr>
  <td>
  <p><a id="asShownBelow"></a>as shown below</p>
  </td>
  <td>
  <p>Use &quot;as shown in the example&quot; instead of indicating direction, such as &quot;above&quot; or &quot;below&quot;, whenever possible. This helps to ensure that there are no issues if the text is modified, rewritten, or reorganized. You can also write &quot;the following&quot; or &quot;the preceding.&quot;</p>
  </td>
  	<td>
  	<ul>
  	<li>In your request, supply the values for the following parameters:</li>
	</ul>
	</td>
 </tr>

<tr>
  <td>
  <p><a id="backend"></a>back end vs. backend vs. back-end</p>
  </td>
  <td>
  <p>Per the MMoS, use a more specific term when possible, such as server, operating system, database, or network. However, if you must use this term, use back end, two words, no hyphen, as a noun. Use back-end, hyphenated, as an adjective to modify a noun. Do not use &quot;backend.&quot;</p>
  </td>
  	<td>
  		<ul>
  			<li>Set up accounts in your back-end system with command line requests.</li>
  			<li>Configure the application on the back end.</li>
  		</ul>
	</td>

 </tr>

<tr>
  <td>
  <p><a id="using"></a>by using vs. using</p>
  </td>
  <td>
  <p>To avoid ambiguity for worldwide audiences, use &quot;by using&quot; instead of &quot;using&quot; by itself, even if the preposition seems unnecessary. </p>
  <p>However, in most cases, you can rewrite the sentence more directly, by highlighting the action verb in the sentence, as shown in the example.</p>
  </td>
  	<td>
  	    <ul>
    	<li>
	Schedule regular backups with the backup utility to avoid data loss.
    	</li>
    </ul>
	</td>
 </tr>

  <tr>
  <td>
  <p><a id="click"></a>&quot;Click <b>Add</b>&quot; vs. &quot;Click the <b>Add</b> button.&quot;</p>
  </td>
  <td>
  <p>If the button has a label with text, use the label name without the word &quot;button.&quot;</p>
 <p> If the button or icon does not have a text label, use a descriptive name with the word &quot;button.&quot;
  Bold the label or icon name in both cases.</p>
  </td>
  	<td>
	<ul>
  		<li>Click <b>Add</b>.</li>
  		<li>Click the <b>Maximize</b> icon.</li>
  	</ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="email"></a>e-mail vs. email</p>
  </td>
  <td>
  <p>Use &quot;email&quot; as a noun, not as a verb. For a verb form, use &quot;send&quot; instead. Do not write &quot;e-mail&quot; with a hyphen.</p>
  </td>
  	<td>
  	<ul>
  		<li>You can send an email using Outlook.</li>
  	</ul>
	</td>
 </tr>

<tr>
  <td>
  <p><a id="fillIn"></a>fill in vs. complete</p>
  </td>
  <td>
  <p>Use &quot;fill in.&quot;</p>
  </td>
  	<td>
  	    <ul>
    	<li>
Fill in the remaining fields and click <b>Save</b>.
    	</li>
    </ul>
	</td>
 </tr>

  <tr>
  <td>
  <p><a id="id"></a>id vs. ID</p>
  </td>
  <td>
  <p>Use &quot;ID,&quot; capitalized, as the abbreviation for &quot;identification.&quot; &quot;Id,&quot; or &quot;id,&quot; has a <a href="https://en.wikipedia.org/wiki/Id,_ego_and_super-ego" target="_blank">different meaning</a> in English. &quot;id&quot; is only appropriate when you are documenting code, as shown in the second example. </p>
  </td>
  	<td>
  	<ul>
  	<li>Enter your user ID in the provided field.</li>
  	<li>Provide a value for the <b>id</b> parameter.</li>
	</ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="forExample"></a>i.e. vs. e.g. vs. for example</p>
  </td>
  <td>
  <p>Do not use i.e. or e.g. Use &quot;that is&quot; or &quot;for example&quot; instead. Depending on the context, &quot;such as&quot; may be appropriate, as well.</p>
	<p>Do not use &quot;for example&quot; in the middle of a sentence. Instead of &quot;This smartphone has many uses, for example making calls, sending text messages, and taking pictures,&quot; provide the information in two sentences: &quot;This smartphone has many uses. For example, it can make calls, send text messages, and take pictures.&quot;</p>
  </td>
  	<td>
  	    <ul>
    	<li>
  	There are many reasons to visit Colorado. For example, there are 300 days of sunshine per year. You can enjoy a variety of activities in Colorado, such as skiing, hiking, and visiting museums and breweries.
    	</li>
    </ul>
	</td>
 </tr>

<tr>
  <td>
  <p><a id="whenever"></a>whenever</p>
  </td>
  <td>
  <p>Try to avoid the word &quot;whenever.&quot; You can typically use &quot;when&quot; instead of &quot;whenever.&quot;</p>
  </td>
  	<td>
  	<ul>
  		<li>When you click <b>OK</b>, a new window opens.</li>
	</ul>
	</td>
 </tr>

  <tr>
  <td>
  <p><a id="keyValue"></a>key-value pairs</p>
  </td>
  <td>
  <p>Use &quot;key-value pairs.&quot; Do not write key/value, key value, or key:value.</p>
  </td>
  	<td>
  	    <ul>
    	<li>
  	The Configuration service uses independent key-value pairs to store all configuration information.
    	</li>
    </ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="kindType"></a>kind vs. type</p>
  </td>
  <td>
  <p>Use &quot;type.&quot;</p>
  </td>
  	<td>
  	    <ul>
    	<li>
  	There are three types of files in this folder.
    	</li>
    </ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="login"></a>sign in, sign out, and register</p>
  </td>
  <td>
  <p>Use only &quot;sign in,&quot; &quot;sign out,&quot; and &quot;register.&quot;</p>
 </td>
  	<td>
  	<ul>
  		<li>Sign in to your account.</li>
  	</ul>
	</td>
 </tr>

  <tr>
  <td>
  <p><a id="possible"></a>possible vs. can or cannot</p>
  </td>
  <td>
  <p>Use &quot;can&quot; and &quot;cannot.&quot; Do not write &quot;it is possible&quot; or &quot;it is not possible.&quot;
 </p>
  </td>
  	<td>
  	<ul>
  		<li>You cannot enter more than eight characters.</li>
  	</ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="replace"></a>replace by vs. replace with</p>
  </td>
  <td>
  <p>Use &quot;replaces&quot; or &quot;replace with.&quot; Do not use &quot;replace&quot; as a noun.</p>
  </td>
  	<td>
  	<ul>
  		<li>Replace the selected text with the new text.</li>
	</ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="should"></a>should vs. must vs. have to</p>
  </td>
  <td>
<p>While the MMoS advises using &quot;should&quot; only to describe a recommended, but optional, user action, &quot;should&quot; is ambiguous. When you write &quot;should&quot;, it is not always clear whether the reader needs to perform an action. If it is recommended to back up files regularly, you can just say &quot;Back up your files regularly.&quot; Then explain the potential danger of not backing up files.</p>
  	<ul>
		<li>Use &quot;must&quot; only to describe a user action that is required.</li>
		<li>Do not use the phrase &quot;have to.&quot; Use &quot;must&quot; instead.</li>
		<li>Do not use &quot;should&quot; to indicate probability. Wherever possible, express certainty. When that is not possible, use &quot;may&quot; or rephrase.</li>
	</ul>
  </td>
  	<td>
  	<ul>
  		<li>Your computer must have at least 128 MB of RAM to run this program.</li>
  	</ul>
	</td>
 </tr>

 <tr>
  <td>
  <p><a id="singleSignOn"></a>single sign-on vs. single sign on</p>
  </td>
  <td>
  	<p>Use single sign on (SSO) to refer to authentication that allows a user to sign into multiple applications with one set of credentials. When referring to the act of signing in, write &quot;sign in.&quot;</p>
  </td>
  	<td>
  	    <ul>
    	<li>The platform has single sign on (SSO) to make it easier to use related applications.</li>
    </ul>
	</td>
 </tr>


  <tr>
  <td>
  <p><a id="thirdParty"></a>Third-party names and acronyms</p>
  </td>
  <td>
  <p>Refer to the originator's official documentation for the correct spelling and capitalization of third-party tools such as JavaScript, Enterprise JavaBeans (EJB), and cron.</p>
  </td>
  	<td>
  	    <ul>
    	<li>Enterprise JavaBeans (EJB), is a managed, server-side component architecture for modular construction of enterprise applications.</li>
    		</ul>
	</td>
 </tr>

  <tr>
  <td>
  <p><a id="topic"></a>topic vs. section in cross-references</p>
  </td>
  <td>
  <p>Use &quot;section.&quot;</p>
  </td>
  	<td>
  	    <ul>
    	<li>
  	For more information about creating email templates, see the <a href="https://devportal.yaas.io/services/email/latest/">Email</a> section.
    	</li>
    </ul>
	</td>
 </tr>

<tr>
  <td>
  <p><a id="typically"></a>typically vs. usually</p>
  </td>
  <td>
  <p>Use &quot;typically.&quot;</p>
  <ul>
		<li>If you use &quot;typically&quot; at the beginning of a sentence, use a comma after, as shown in the example.</li>
		<li>Do not use a comma before or after &quot;typically&quot; in the middle of a sentence.</li>
		<li>Avoid using &quot;typically&quot; at the end of a sentence.</li>
	</ul>
  </td>
  	<td>
  	<ul>
  		<li>Typically, the winter is very cold.</li>
  	</ul>
	</td>
 </tr>

<tr>
  <td>
  <p><a id="via"></a>via</p>
  </td>
  <td>
  <p>Do not use &quot;via.&quot; Instead, write &quot;through,&quot; &quot;in,&quot; &quot;using,&quot; &quot;with,&quot; &quot;by,&quot; or another appropriate American English term. </p>
  </td>
  	<td>
  	<ul>
  		<li>You can also make the request through a command line interface.</li>
  	</ul>
	</td>
 </tr>

   <tr>
   <td>
   <p><a id="weUsLetsOur"></a>we, us, let's, or our</p>
   </td>
   <td>
   <p>Do not use &quot;we,&quot; &quot;us,&quot; &quot;let's,&quot; or &quot;our.&quot; Instead of &quot;We released a new feature for the Email service,&quot; write &quot;A new feature is available for the Email service.&quot;</p>
   </td>
   	<td>
   	    <ul>
		    <li>An issue in the PubSub service is now resolved.</li>
		</ul>
	</td>
  </tr>

</table>


#### Voice and tone

<p>
Voice and tone standards apply to the different types of documentation. First, it is important to understand the difference between voice and tone, and then follow the guidelines for writing content in the proper tone, depending on the destination for your documentation.
</p>

<h5>Difference between voice and tone</h5>

The difference between voice and tone can be a bit hard to differentiate at first. But think about the sound of your own voice, or a certain phrase that you use often. Those characteristics define your voice. When you address different people, or write documentation for different situations, you still have the same voice, but you might use a different tone. For instance, if you beat a friend in foosball, you might say, "I crushed you!" But if you beat your child at foosball, you might say, "Good game, kid."

<h5>Tones in technical documentation</h5>

There are different tones for the different types of technical documentation. The documentation can range from instructional to somewhat conversational, but always with the goal of helping users understand how to use the product for practical purposes and, in blogs and release notes, also helping business users understand changes so they can plan according to their business needs.<br><br>
[NEXT >](020_Syntax_Guidelines.html.md)
