[![Build Status](https://travis-ci.org/biztek/hipaa-dea-number-input.svg?branch=master)](https://travis-ci.org/biztek/hipaa-dea-number-input)

_[Demo ↗](https://biztek.github.io/hipaa-dea-number-input/components/hipaa-dea-number-input/demo/)_

_[API docs ↗](https://biztek.github.io/hipaa-dea-number-input/components/hipaa-dea-number-input)_

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

The DEA number validation rules are based on the following wikipedia article (https://en.wikipedia.org/wiki/DEA_number)
A valid DEA number consists of:
- 2 letters, 6 numbers, and 1 check digit
- The first letter is a code identifying the type of registrant (see below)
- The second letter is the first letter of the registrant's last name, or "9" for registrants using a business address instead of name.

Of the seven digits that follow, the seventh digit is a "checksum" that is calculated similarly to the Luhn algorithm, with the following steps:
- Add together the first, third and fifth digits call this CALC1,3,5
- Add together the second, fourth and sixth digits and multiply the sum by 2, call this CALC2,4,6
- Add CALC1,3,5 + CALC2,4,6 call this CHECK

The rightmost digit of CHECK (the digit in the ones place) is used as the check digit in the DEA number

Registrant type (first letter of DEA Number):[dubious – discuss]

- A – Deprecated (used by some older entities)
- B – Hospital/Clinic
- C – Practitioner
- D – Teaching Institution
- E – Manufacturer
- F – Distributor
- G – Researcher
- H – Analytical Lab
- J – Importer
- K – Exporter
- L – Reverse Distributor
- M – Mid Level Practitioner
- P – Narcotic Treatment Program
- R – Narcotic Treatment Program
- S – Narcotic Treatment Program
- T – Narcotic Treatment Program
- U – Narcotic Treatment Program
- X – Suboxone/Subutex Prescribing Program

Right Format DEA Numbers example: BJ6125341 , FN5623740, AS5623740.

Wrong Format DEA Numbers : B23456789, 73636373D.

### Listening for input changes

By default, it listens for changes on the `bind-value` attribute on its children nodes and perform
tasks such as auto-validating and label styling when the `bind-value` changes.

### Validation

If the `auto-validate` attribute is set, element validates the input whether it is Hipaa compliant DEA number and update
the label styling when the input value changes.

### License

Licensed under [Apache License 2.0](LICENSE).
