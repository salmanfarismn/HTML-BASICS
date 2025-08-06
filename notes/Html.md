HTML - Hyper Text Markup Language

- Defines structure of the webpage.
- Should have .html extension for files
- Example: index.html
- Not a programming language.

- BASIC STRUCTURE:
<!DOCTYPE html> <!-- Declares HTML5 -->
<html lang="en">
<head> <!-- Includes meta, title, link -->
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body> <!-- visible content -->
	<!-- Page Content Here -->
</body>
</html>

- Key Tags:
	Document:
		<html>, <head>, <body>, <title>, <meta>, <link>, <script>
	Layout:
		→ Non-semantic:
			• <div> - generic container
			• <span> - inline container
		→ Semantic:
			• <header> - It will be at the top of the page or section, typically containing branding.
			• <nav> - Used within the header (or standalone) to group navigation links.
			• <main> - Encapsulates all the primary, page specific-content (excludes header/footer). Use only once in a page.
			• <section> - Thematic grouping of content that has a heading. 
						  (Thematic - The process of identifying the commonalities in the data)
			• <article> - Article is used for news article, blog posts, user comments. It is a standalone and reusable content.
			• <aside> - Used for side content like external links, Ads, related topics etc..
			• <figure> - Used to wrap media contents like image, charts, code snippets, diagrams and Audio/video embeds.
			• <footer> - footer is commonly used at the bottom of the page for links, contacts, copyright and trademarks etc..
						 It is also used in nesting like <footer> in a <article> to represent the author, tags etc at the bottom of the article
			• <figure> - Used to wrap self-contained media content like: Images, Charts, Diagrams, Audio/Video embeds etc.
			• <figcaption> - It is used inside the <figure> to give the content a caption or description
	Text:
		→ Headings: <h1> to <h6>
		→ Paragraph: <p>
		→ Emphasis: <strong>, <em>, <b>, <i> [Emphasis is used to indicate that a phrase should be stressed or highlighted]
		→ Line break: <br>
		→ Horizontal rule: <hr>
	Media:
		→ Image: <img src="..." alt="image">
		→ Video: <video controls>
					<source src="..." type="video/mp4">
				 </video> 
		→ Audio: <audio src="..." controls></audio>
	Links & Navigation:
		→ <a href="url">Link</a>
	Lists:
		→ Ordered list: <ol> 
							<li>...</li> 
						</ol>
		→ Unordered list: <ul> 
							<li>...</li> 
						  </ul>
		→ Description: <dl> 
							<dt>
								<dd>...<dd>
							</dt> 
						</dl>
	Forms:
		→ Form: <form action="...">
		→ inputs: <input>, <textarea>, <select>, <option>, <button>
			
- Inline v/s Block Elements:
	Inline: Takes up only necessary width. Don't start from new line. example: <a>, <img>, <span>
	Block: Takes up the full width available and start from new line. example: <div>, <h1> - <h6>, <p>

- HTML5 includes the HTML Standard, along with Javascript APIs to enhance storage, multimedia and hardware access.
- Emmets is a shorthand tool for writing HTML/CSS faster.

- Tables in HTML:
	Tables are used to represent real life table data.

- Basic Structure
<table>
	<caption>Table Title</caption>
	<thead>
		<tr>
			<th>Name</th>
			<th>Roll No</th>
		</tr>
	</thead>
	</tbody>
		<tr>
			<td>John</td>
			<td>66</td>
		</tr>
	</tbody>
</table>

- <thead> and <tbody> are semantic tags and it will give more clarity to the table.
- <tr> is used to display the row.
- <th> is used to display the table heade.r
- <td> is used to display the table data.
- There is one more semantic tag in the table, ie; <tfoot> which can be used for giving sum, result etc.

- Colspan & Rowspan attribute:
	Here, span is the amount of area to occupy by a cell in HTML table.
- <tr>
	<td rowspan="2"></td>
	<td colspan="2">Average</td>
	<td rowspan="2">Red eyes</td>
  </tr>
  <tr>	
	<td>Weight</td>
	<td>Height</td>
  </tr>

- Forms in HTML:
	→ Forms are used to collect data from the user.
	→ Action attribut: It is used to define what action need to be performed when a form is submitted or where the form data
	  should be send.
	→ <form action="/action.php"> - Here you specified a file in your project itself
	→ <form action="/action"> - Here you are sending the data in the form to "/action" route.

- Form Elements:
	input:
		→ <input type="text"> - There are more types like password, email, tel, number, time, color etc.
		→ Used to create multiple form controls
		→ By using <input> you can create multiple types of input by using the type attribute.
	button:
		→ The button element is used to submit or perform any custom action
		→ <button> Submit </button>
		→ The button has a default type and that is "submit". Even if the button is inside or outside of the form the type
		   attribute will be "submit". When it is outside the form it has no effect because it is not associated to any form.
		→ The button has three types:
			<button type="submit"> Submit </button> - It is used to submit the form
			<button type="button"> Submit </button> - It is used to perform custom action by using the "onClick" attribute.
			<button type="reset"> Reset </button>   - It is used to reset or clear the page
	checkbox:
		→ It can be used to select multiple choices 
		→ <input type="checkbox" name="age" id="age" checked>
		  <label for="age">Iam 18+</age>
		→ eg: ⏹️ Iam 18+
		→ "checked" keyword can be used to pre-select the checkbox
	radio button:
		→ It only allows you to select only one option from the multiple choices
		→ <input type="radio" name="fruit" id="apple" value="apple">
			• "name" attribute is used as a common group name to restrict the radio button from allow the user to select multiple
			  choices
			• "id" attribute is used to uniquely identify the element
			• "value" attribute is used to pass the value of the selected radio button to the name attribute
				name = value
				 👇     👇
				fruit = "apple" (Here apple is taken as the example value from the above input)
		→ All radios should have been grouped under a same name.
		→ "checked" keyword can be used to pre-select an option.
	select:
		→ used to create dropdown menus
		→ <select name="country" id="country">
		  	<option value=""> Select a country </option>
		  	<option value="IN"> India </option>
			<option value="UAE"> United Arab Emirates </option> 
		  </select>
		→ The value from the seleted option will be sent to the server when the form is submitted.
		→ "name" attribute is required to sumit the selected value
			• So here, when we select an option the value from the selected option is given to the name attribute in the <select>.
		→ "selected" keyword can be used to set a default option.
		→ "disable" keyword can be used to disable a specific option
	range:
		→ <label for="volume"> Volume </label>
		  <input type="range" name="volume" id="volume" min="0" max="100" value="30">
		  	• min is the minimum value in the range that can be selected
			• max is the maximum value in the range that can be selected
			• value is the default value for the range option
		→ It is like a slider
		→ The "step" attribute represent how incremention should be occur per increase in the rage slider.
	textarea:
		→ <label for="feedback"> Write your feedback </label>
		  <textarea id="feedback"></textarea>
		→ Can adjust the width and height of the textarea using "rows" and "cols" attributes.

- Placeholders & Labels:
	placeholder:
		→ It is a grey hint inside the input, which disappears when user starts typing
		→ <input type="text" placeholder="Enter your name">
		→ It is a attribute
	labels:
		→ It is a tag unlike placeholders
		→ It describes the input field
		→ Improves user experience, as it focus the input box when clicked on the label
		→ <label for="email"> Email: </label>
		  <input type="text" id="email" name="user_email">
		→ Note: The value of the "for" attribute(label) should match the value of the "id"(input)
			ie, for = id. 

- Name attribute:
	→ Name of the form control that is submitted with the form as part of name/value pair.
	→ <input type="text" name="username" />
	→ The "name" attribute retrieves the data from the form after the form is submitted
	→ Holds the data from the form

<!-- The End -->