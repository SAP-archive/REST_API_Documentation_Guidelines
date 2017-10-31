## Syntax Guidelines

These are the guidelines for formatting text and using specific elements such as lists, tables, headings, links, and images in the documentation.

### Code formatting
 It is important to consistently format items such as code or filenames to quickly distinguish them while reading technical documentation. The following table outlines when to use **bold** font and when to use `code` font:

##### Use bold font for these items:

Items       | Examples
----------- | ----------------------------------------------------------------------
Parameters  | The **partial** attribute is optional.
Events      | The service publishes a **password-reset-requested** event.
File names  | Open the **pom.xml** file.
Path names  | Save the file in the **\services\repository** folder.
Scopes      | Use the **hybris.profile_graph_view** scope to view data in the graph.
UI elements | Click on **Subscribe**.
Variables   | Click **Project** > **{Your Project Name}**. Variables are also enclosed in single curly braces.

##### Use code font for these items:

Items                     | Examples
------------------------- | -----------------------------------------------------------------------------------------------
Code examples             | Verify the installation with the `mvn help:system` command.
Values                    | Set the partial attribute to `true` to perform a partial replacement. 
Endpoints                 | Send a POST request to the `/{tenant}/categories/{categoryId}/media/{mediaId}/commit` endpoint.
Status and error codes    | A successful response includes a status code of `200 OK`.
Parameter and value pairs | To perform a partial replacement, include `partial=true` in your request.

### Content formatting
Format the content in an attention-grabbing way. In general, content is easier to read when it is in chunks. Consider breaking up endless paragraphs by using a list or table. Use action verbs and present tense for headings to engage the reader, and also follow the guidelines for the best way to include links and images.

#### Ordered and unordered lists
As you write about your topic, use lists to create visual clarity within your content. List items in a category, or list items in a sequence. Use an ordered, or numbered, list for sequential, instructional steps. Unordered lists are appropriate for items that have no sequential order, such as a list of valid file types. Follow these guidelines:
* Make list content consistent in structure. For example, make all the bullet points sentences, questions, or sentence fragments, but do not mix types. 
* Punctuate bullet points consistently. If they are all sentences, use periods. If they are sentence fragments, do not use periods.
* Avoid ending bullet points with punctuation such as semicolons or commas.
* Capitalize the first letter of each bullet point consistently. Capitalize the first letter unless the list items are always lowercased, as with parameters names.
* Emphasize the beginning of the bullet point to capture the main idea.
* If readers must perform list items in order, as in a step-by-step procedure, use an ordered list, and maintain the consistency in structure.

For more details about lists, see the [Top Tips for Using Lists](https://github.com/YaaS/REST_API_Documentation_Guidelines/wiki/003-Top-Tips-for-Using-Lists) blog post.<br>
##### Example
See the example in the [Release Notes](030_REST_API_Documents.html.md#release-notes) section.

#### Tables
Another effective way to chunk content is to use tables. Use tables when content needs comparison, or as a way to provide information mapping. Think of a table as a list, but with optional columns to provide and organize more information than belongs in a list. Make sure tables are not too long or hard to read, causing the reader to scroll a lot. Break up a long table into multiple tables, if possible. For an example, see the [Style and Standards](010_About_Style_And_Standards.html.md#style-and-standards) section.

#### Headings
Ideally, headings fit onto one line in the generated output, but balance brevity with a heading that adequately describes the main point of the document, section, or topic. Follow these guidelines when writing headings:

* Write headings within a document in sentence case. For example, **Create a product category**.
* Use action verbs and present tense verbs in headings when possible, especially in tutorials. For example, **Add a document type**.
* While gerunds are acceptable in body-level content, DO NOT use gerunds in headings, as in **Creating a storefront**.
* Avoid stacked headings, which are headings without body-level content in between. For example, DO NOT use a Heading 3 (H3) to introduce one or more Heading 4s. Instead, add a paragraph after the H3 that describes the main idea of the content in the headings that follow.

#### Links
Linking is a great tool to use to incorporate a lot of content into your document with fewer words. That being said, overuse of linking can create "link rot" when links break, and if a page has more links than content, it is not very pleasing to read. Choose carefully when and how to link by using these best practices.

- Every link has the potential to go bad over time, and the more links you include, the higher the chance that one will break. If something is not central to the subject at hand, is well-known by your audience, or can be found with a simple search, there is no point in linking.
- For external links, link to the main page of the external website and then describe how to access the destination link. For example, `Go to the <a href="www.raml.org">RAML</a> website and click on the download link.` Main page URLs are less likely to change.
- Choose the link text carefully. Do not link entire phrases which become overemphatic. Instead, choose the noun, such as an article or specification within the phrase that helps the reader understand where the navigation leads them. Or use the title of the article or book as the link, but do not include the author and publisher.
- Link to web pages instead of PDFs whenever possible.
- Do not include spaces or other characters in the link that require escape characters for translation.
- Check your links often to make sure they are still operational. There are free online tools to make it easier.

##### Good examples
- For more information about mixins, see the <a href="https://devportal.yaas.io/services/document/latest/index.html#OperateonMixins">Operate on Mixins</a> topic in the Document service documentation.
- See the <a href="https://devportal.yaas.io/overview/yaasinanutshell/index.html">YaaS in a Nutshell</a> page for more information.
- The recommended reading is a book entitled <a href="http://shop.oreilly.com/product/0636920033158.do">Building Microservices</a> by Sam Newman, O'Reilly Media.

#### Images and screenshots
As someone once said, a picture is worth a thousand words. Therefore, whenever possible, use a diagram, image, or screenshot to convey a lot of information visually. Follow these guidelines when placing a diagram, screenshot, or other image in your content.

Images and screenshots can quickly convey a lot of important information in your documentation. Do not use directional indicators, such as "above" and "below" to refer to images. Instead, include a brief introduction before each image that describes the purpose of the image and any necessary details. Do not overuse images such as including multiple screenshots of the same screen. Either condense them into one screenshot, or crop the images to show different areas. Follow the rest of these guidelines to make or use images, or capture screenshots:
 <ul>
   <li>Make or capture your images using any tool that outputs high quality images, such as <a href="https://www.techsmith.com/screen-capture.html">Snagit</a>. The desired image format is SVG (vector), but PNG and JPG (raster) are acceptable.</li>
   <li>Use an online tool such as <a href="https://tinypng.com/">TinyPNG</a> to compress images and limit the size of each image to 1MB, or smaller.</li>
   <li>If you want to control the size of the image relative to the screen size, use one of these standard percentages: 100%, 75%, 50%, or 25%.</li>
   <li>Align images to the left, unless it is a special case, such as images in a table.</li>
   <li>Do not include the mouse pointer in your screenshots, unless it shows a function related to the content.</li>
   <li>To highlight certain areas of an image, crop the image, or use <strong><font color="#F0AB00">yellow</font></strong> (RGB: 240,171,0 or HEX: #F0AB00) for arrows or boxes around elements with a three point line width.</li>
   <li>For multiple screenshots, use your best judgment as to whether you include one introduction, or whether you introduce each screenshot separately.</li>
   <li>Describe multiple areas using <strong><font color="#8A5FF6">purple</font></strong> round stamps with white numbers. In Snagit, you can create a number in this style and add it to the quick  menu:</li><br><br>
<div class="row">
    <div class="col-sm-4">
    <img src="img/snagit_win.png" width="375" height="375" alt alt="Snagit Editor"></div>
    <div class="col-sm-3">
    <img src="img/snagit_mac.png" width="375" height="375" alt="Snagit Editor Styles Menu"></div>
  </div>
   <li>Introduce the image with a sentence, similar to this example:<br/><br/>
   See this example for the screenshot highlight, border, and color guidelines:
   <br><br>
     <img src="img/images_example.png" alt="Example"></li>
 </ul>


<br>[< PREV](010_About_Style_And_Standards.html.md) | [NEXT >](030_REST_API_Documents.html.md)


