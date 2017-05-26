[![Build Status](https://travis-ci.org/biztek/hipaa-dea-number-input.svg?branch=master)](https://travis-ci.org/biztek/hipaa-dea-number-input)

_[Demo and API docs](https://biztek.github.io/hipaa-dea-number-input/components/hipaa-dea-number-input)_

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
### DEA Numbers Validation.
#### A DEA number (DEA Registration Number) is a number assigned to a health care provider.

A valid DEA number consists of total 9 characters.
- The first character is a letter, a code identifying the type of registrant. 
- The second character is a letter or a digit 9.
- The next six characters are digits from [0-9].
- The last character is a check digit, `DEA numbers` can be verified by using the last charcter, which is known as the `Check Digit`.

Right Format DEA Numbers example: BJ6125341 , FN5623740, AS5623740.

Wrong Format DEA Numbers : B23456789, 73636373D.

### Listening for input changes

By default, it listens for changes on the `bind-value` attribute on its children nodes and perform
tasks such as auto-validating and label styling when the `bind-value` changes.

### Validation

If the `auto-validate` attribute is set, element validates the input whether it is Hipaa compliant DEA number and update
the label styling when the input value changes.

