# Accessible Checkbox

<p align="center">![Alternate text](https://github.com/iAty/accessible-checkbox/blob/master/img/accessibility-pattern.jpg)
</p>

First, not all your forms are necessarily going to be impacted by the GDPR. If you’re not collecting personally identifiable information on users, your form’s not impacted. 
However… Are you asking for a Name? Email? Address? The GDPR impacts that form.

Explicit consent has to be obtained before data collection can take place. In other words, before the user submits the form. They must be made aware that this form is collecting personal data with the intent to store
that data. You’re also responsible for letting the user know how that data will be stored and used.

See the [live demo](https://github.com/iAty/accessible-checkbox.git).

## Install

Clone it:

```
$ git clone https://github.com/iAty/accessible-checkbox.git
```

Or [download a zip of the repository](https://github.com/iAty/accessible-checkbox.git).

### Native JavaScript

The :  

```js
    window.onload = function() {
        var CookiePolicyConsent = document.getElementById("CookiePolicyConsent");
        CookiePolicyConsent.onclick = function() {
            var ThisIsChecked = (this.getAttribute("aria-checked") === "true");
            this.setAttribute("aria-checked", !ThisIsChecked);
        };
    }
```

The :

```html
      <div class="form-group">
        <label class="material-checkbox">
          <input type="checkbox" id="CookiePolicyConsent" role="checkbox" aria-checked="false" tabindex="0">
          <span>I agree to the Privacy Policy</span>
        </label>
      </div>
```

## License

[MIT license](https://github.com/iAty/accessible-checkbox/blob/master/LICENSE.md).
