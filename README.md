[![Build Status](https://travis-ci.org/rajkumarajce/hipaa-dea-number-input.svg?branch=master)](https://travis-ci.org/rajkumarajce/hipaa-dea-number-input)

_[Demo and API docs](https://rajkumarajce.github.io/hipaa-dea-number-input/components/hipaa-dea-number-input)_

# \<hipaa-dea-number-input\>

`<hipaa-dea-number-input>` is a single-line text field to hold valid Hipaa compliant DEA number.

```html
<hipaa-dea-number-input label="Input label"></hipaa-dea-number-input>
```

It includes an optional label,error message,invalid,autovalidate and required attributes.

```html
<hipaa-dea-number-input label="Input label"></hipaa-dea-number-input>
<hipaa-dea-number-input error-message="Invalid input!"></hipaa-dea-number-input>
<hipaa-dea-number-input invalid="boolean value"></hipaa-dea-number-input>
<hipaa-dea-number-input autoValidate="boolean value"></hipaa-dea-number-input>
<hipaa-dea-number-input required="boolean value"></hipaa-dea-number-input>
```

### Listening for input changes

By default, it listens for changes on the `bind-value` attribute on its children nodes and perform
tasks such as auto-validating and label styling when the `bind-value` changes.

### Validation

If the `auto-validate` attribute is set, element validates the input whether it is Hipaa compliant DEA number and update
the label styling when the input value changes.

