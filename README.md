# online_registration_v4 (Front End Web Development Project 3)

### Project Overview

-   #### Build the layout using a mobile first design:

    -   Make sure the HTML file includes the viewport meta tag in the head of the document, see [Configuring the Viewport](https://developers.google.com/speed/docs/insights/ConfigureViewport#overview) to understand why and how to add this tag.
    -   Look at the provided mockup (mobile-form.png) and add the same content into your index.html file.
    
````
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="css/styles.css">
  <title>The Code Review | Signup for our newsletter</title>
</head>
````

-   #### Create the form structure:

    Only use one `<form>` tag. The `<form>` tag should contain all the form elements. Add a fieldset and legend for each of the following sections:

    -   "Contact Information" section of the page, and
    -   The "Newsletter" section of the page

    Note: You don't need to make a functioning form -- that is, it doesn't have to do anything when the form is submitted. To do that, you'd need to add some server-side programming to actually process the user's input.

-   #### Make sure you include the following form field types:

    -   text input
    -   email input
    -   telephone input
    -   select menu
    -   checkboxes
    -   radio buttons
    -   textarea
    -   submit button

-   #### Form fields should include the following attributes:

    -   `input`: should include `id`, `type` and `name` attributes.
    -   `select` and `textarea`: should include `id` and `name` attributes.
    
-   #### Add labels to each form element using the [HTML `<label>` tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label). The text inside the labels should match the names of the form fields in the mockups.

    -   Make sure you properly pair each `<label>` element with its corresponding form control via the `for` attribute. See the link above for an example. And don't forget about the textarea element. That needs a functioning label too.

    NOTE: Remember that to associate a label with a form input element, the label's "for" attribute should match the input's *unique* `id`.

-   #### Use the input field's `placeholder` attribute to add the text "required" to:

    -   the Full Name field
    -   the Email address field
    
````
<label for="fullName" class="contact-labels">Full Name</label>
<input type="text" name="Full Name" value="" class="input-field text" id="fullName" placeholder="Required" required>
<label for="emailAddress" class="contact-labels">Email Address</label>
<input type="email" name="Email Address" value="" class="input-field text" id="emailAddress" placeholder="Required" required>
<label for="phoneNumber" class="contact-labels">Phone Number</label>
<input type="tel" name="Phone Number" value="" class="input-field text" id="phoneNumber" placeholder="Phone">
<label for="streetAddress" class="contact-labels">Street Address</label>
<input type="text" name="Street Address" value="" class="input-field text" id="streetAddress" placeholder="Street Address">
<label for="city" class="contact-labels">City</label>
<input type="text" name="City" value="" class="input-field text" id="city" placeholder="City">
<label for="state" class="contact-labels">State</label>
<select name="State" class="input-field select" id="state">
  <option selected disabled>Choose State</option>
````

-   #### Once you have everything in place for the mobile layout, use a media query to add a breakpoint to adjust the layout for wider tablet and desktop screens.

    -   Match the design as it should look on a tablet or desktop that is 768px wide using the desktop-form.png mockup.
    -   Use a mobile-first approach by writing your media queries using the `min-width` property in your CSS.

-   #### Once all your breakpoints are in place, double check your layout matches both the mockups.

    -   Check that the label text position matches both mockups:
        -   *Mobile*: Text should be above the form field.
        -   *Desktop*: Text should be to the left side of the form field.
````
@media (min-width: 768px) {

  .sub-title-banner h3 {
    font-size: 1.6em;
  }

  .sub-title-banner p {
    margin: 0em 0 1.8em 0;
  }

  .contact-info {
    display: flex;
    flex-wrap: wrap;
  }

  .contact-info h3 {
    width: 100%;
  }

  .contact-labels {
    display: inline-flex;
    width: 40%;
    margin: 0.5em 0 0.5em 0;
  }

  .text, select {
    display: inline-flex;
    width: 60%;
    margin: 0.5em 0 0.5em 0;
  }

  .zip {
    width: 25%;
    margin-right: 35%;
  }
}
````
-   #### Use a Google Font for the text. The design uses the ["Merriweather" font](https://www.google.com/fonts/specimen/Merriweather) but, you can use any Google Font that you'd like.

-   #### Add `:focus` states to the form for when a user clicks or tabs into a text field.

````
.text:focus, textarea:focus {
  outline: none;
  border: medium solid black;
  background-color: #ADDFDC;
}

select:focus {
  outline: none;
  border: medium solid black;
}
````
