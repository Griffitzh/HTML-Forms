# HTML Forms

## Objectives

- Get to know HTML Form elements created for user input
- Get familiar with client-side form validation
- Be able to send form data to a REST API endpoint

## Materials

| Material                                                                                                               |  Time |
| :--------------------------------------------------------------------------------------------------------------------- | ----: |
| [My First HTML Form](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/My_first_HTML_form)                 |  read |
| [Styling HTML 5 Forms #1 - Introduction](https://www.youtube.com/watch?v=HiHHvTcHiEk)                                  |  6:26 |
| [Styling HTML 5 Forms #4 - Styling Text Inputs](https://www.youtube.com/watch?v=3Bhrx2DumvI)                           |  6:18 |
| [Styling HTML 5 Forms #5 - Styling Select Boxes](https://www.youtube.com/watch?v=IPtyr11fjcI)                          |  3:37 |
| [JavaScript DOM Tutorial #11 - Interacting with Forms](https://www.youtube.com/watch?v=n4B7vY9SIds)                    |  5:42 |
| [POST Form Data as JSON with Fetch API in JavaScript](https://www.youtube.com/watch?v=DqyJFV7QJqc)                     |  9:24 |
| [JavaScript Client-side Form Validation](https://www.youtube.com/watch?v=rsd4FNGTRBw)                                  | 29:06 |
| [HTML input types](https://www.w3schools.com/html/html_form_input_types.asp)                                           |  read |

### Optional

| Material                                                                                                               |  Time |
| :--------------------------------------------------------------------------------------------------------------------- | ----: |
| [How do you Submit an HTML Form? How does it work?](https://www.youtube.com/watch?v=TCEgdiN0A8s)                       | 17:01 |
| [HTML5 form types](https://css-tricks.com/video-screencasts/99-overview-of-html5-forms-types-attributes-and-elements/) | 49:12 |
| [Change event on MDN](https://developer.mozilla.org/en-US/docs/Web/Events/change)                                      |  read |
| [HTML Forms on MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms)                                         |  read |
| [Web form usability](http://www.smashingmagazine.com/2011/11/extensive-guide-web-form-usability/)                      |  read |

## Material Review

- Form creation
  - `<form>` element
    <!--
    - for user interaction, they can send information to the server
    -->
  - `<input>` element
    <!--
    - interactive controls for web-based forms in order to accept data from the
      user
    -->
  - `<input>` element's `type` attribute
    <!--
    - type of the input from the user we accept, see below
    -->
    - text
    - email
    - password
    - tel
      <!--
      A control for entering a telephone number.
      Displays a telephone keypad in some devices with
      dynamic keypads.
      -->
    - number
    - date
    - search
      <!--
      - A single-line text field for entering search strings.
      - Line-breaks are automatically removed from the input value.
      - May include a delete icon in supporting browsers that
        can be used to clear the field.
      - Displays a search icon instead of enter key
        on some devices with dynamic keypads.
      -->
    - color
    - range
    - button
    - hidden
      <!--
      A control that is not displayed but whose value is
      submitted to the server.
      -->
    - submit
      <!--
      - can be an input field with the 'submit' type
      - can be a simple button, the default behaviour of it will be submit anyway
      -->
  - predefined options to choose from
    - checkboxes
      <!--
      - a user can select one or more options of a limited number of choices
      - input name attribute will group them together
      -->
    - radio button
      <!--
      - only one radio button in a given group can be selected
      - typically rendered as small circles, which are filled or highlighted when
        selected
      - input name attribute will group them together
      -->
    - dropdown menu
      <!--
      - select tag is the wrapper
      - option is the options
      - should have a label too
      - usually there is a default option:
        - <option value="">--Please choose an option--</option>
      -->
  - `value`, `checked` attributes
    <!--
    - when submitting the form we can get the info by grabbing the value of the
      field
    - name will be the key, value will be its value
    - if I give a checked value to a checkbox typed input field, it will be
      automatically checked when the form loads
    -->
  - `<textarea>` element
  - `<label>` element
    - `for` attribute
      <!--
      - the label's for attribute will connect with the input's ID attribute
      <label for="username">Username</label>
      <input type="text" name="username" id="username">
      - if we wrap the input with the label, clicking on it will result in
      focusing the input field, and no need for the 'for' attribute in the
      label:
        <label>
          Username
          <input type="text" name="username">
        </label>
      - clicking on the label will put the input into focus (highlight the
      border, activates the input field)
      -->
  - `<input>` element's attributes
    - placeholder
      <!-- will disappear when we start typing -->
    - autofocus
      <!--
      It supports only the following elements: <button>, <input>, <select> and
      <textarea>
      -->
    - autocomplete
      <!--
      - Hint for form autofill feature,
      - it's not a boolean(!),
      - it can be turned off giving the "off" value to it
      -->
    - disabled
      <!--
      - A Boolean attribute which, if present,
      indicates that the user should not be able to interact
      with the input.
      - Disabled inputs are typically rendered with a dimmer color
      or using some other form of indication that the field
      is not available for use.
      - Specifically, disabled inputs do not receive the click event,
      and disabled inputs are not submitted with the form.
      -->
    - readonly
      <!--
      - A Boolean attribute which, if present,
      indicates that the user should not be able to edit
      the value of the input.
      - The readonly attribute is supported
      text, search, url, tel, email, date, month, week,
      time, datetime-local, number, and password input types.
      -->
    - maxlength
      <!-- to specify the maximum number of characters allowed in a text field -->
    - min, max, step
      <!-- for range input -->
    - required
      <!-- won't let you submit without filling in the required fields -->
    - novalidation
      <!-- will exclude the validation of the field -->
  - `<fieldset>` and `<legend>` elements

- Form validation
  - Why do we validate form data on the client?
  - Why do we validate form data on the server?
  - Shall we do both?
  - How does HTML5 form validation work?
    <!--
    - with the type of the inputs and regex
    - regex: restrict the input options with the pattern attribute
    - licence plate is a good example
      <label for="license">license plate</label>
      <input type="text" pattern="[A-Z]{3}-[0-9]{3}" id="license"
        placeholder="ABC-123"/>
    -->
  - How does JavaScript form validation work?
    <!-- on the frontend with functions -->

- Sending JSON data
  - How do we get the data to send?
    <!-- from the DOM -->
    - `value`, `checked` attributes
  - How do we send the data?
    <!-- `submit` event and `fetch` -->
  - What kind of response data are we supposed to receive?
    <!-- JSON -->
  - How do we prevent the page from being reloaded?
    <!-- event.preventDefault() -->

### Optional

- Form's default behaviour (sending URL encoded form data)
  - What is the difference between URL encoded form data and JSON data?
  - How do we get the data to send?
    - `name` attributes
  - How do we send the data?
    <!-- `submit` event's default behaviour -->
    - `method` attribute
      <!--
      - The HTTP method that the browser uses to submit the form
      - GET: form data are appended to the action attribute URL with a '?' as
        separator, and the resulting URL is sent to the server: not safe!
      - POST: form data are included in the body of the request and sent to the
        server.
      -->
    - `action` attribute
      <!--
      - The URL that processes the form information
      - redirect here after submitting
      - default behaviour of submitting is:
        - sending a GET request
        - navigating to the URL given in the action attribute
      -->
  - How do we receive the data on the server?
    - `express.urlencoded()` middleware
  - What kind of response body are we supposed to send back to the client?
    <!-- HTML -->

## Workshop

### Form Design and Validation

- [Login Form](login-form/login.md)
- [Button Disable](button-disable/button-disable.md)
- [Movie selector](movie-selector/movie-selector.md)
- [Newsletter](newsletter/newsletter.js.md)

### Form Submission

- [Sign Up Form](sign-up-form/sign-up.js.md)

## Individual Workshop Review

Please follow the styleguide:
[Our HTML & CSS styleguide](../../styleguide/html-css.md)

- What HTML element did you use for the button and why?
- Are you sure you don't have unnecessary duplications in your code?
