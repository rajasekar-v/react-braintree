# React braintree implementaion


[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install
```
npm install react-braintree-impl --save
```

## Usage Example
```
Credit card add (braintree UI implementaion)
```
```js
import { CreditCardAdd } from 'react-braintree-impl'

const CreditCard = ({
    setLoader,
    loadingBraintree,
    saveCreditCardDetails,
    onBraintreeFails,
    nonceToken
}) => (
       <CreditCardAdd
        setLoader={setLoader}
        loadingBraintree={loadingBraintree}
        saveCreditCardDetails={saveCreditCardDetails}
        onBraintreeFails={onBraintreeFails}
        nonceToken={nonceToken}
        containerClassName="Triniti-creditcard"
      />
    )
```

## PROPTYPES
| Prop | Type | Default | Description |
| ---- | ---- | ------- | ----------- |
| setLoader | function | null | To set loader state on parent |
| loadingBraintree | Boolean | false | Loading state identifier |
| saveCreditCardDetails | function | null | Credit card details submit method |
| onBraintreeFails | function | null | Failure handler for braintree connection establishment |
| nonceToken | String | '' | Braintree authorization token |
| containerClassName | String | '' | Parent classname to override the styles of the list |

## Usage Example
```
Invoices listing
```
```js
import { InvoicesTable } from 'react-braintree-impl'

const Invoices = ({
    invoices,
    selectedStartDate,
    selectedEndDate,
    isLoading,
    onDateChange,
    minStartDate,
    onSelect,
    isRemarkEnabled,
}) => (
    <InvoicesTable
      invoices={invoices}
      selectedStartDate={selectedStartDate}
      selectedEndDate={selectedEndDate}
      isLoading={isLoading}
      onDateChange={this.handleDateChange}
      minStartDate={startDate}
      containerClassName="users-invoices"
      onSelect={this.selectInvoiceForRemark}
      isRemarkEnabled={true}
    />
);
```
## PROPTYPES
| Prop | Type | Default | Description | Sample |
| ---- | ---- | ------- | ----------- | ------ |
| invoices | Array | [] | list of invoices |
| selectedStartDate | Date | null | Start date of the filter |
| selectedEndDate | Date | null | End date of the filter |
| isLoading | Boolean | false | loading state identifier |
| onDateChange | function | null | To handle date change for filters |
| minStartDate | Date | null | Minimum date possible in the filter |
| onSelect | function | null | Select handler for each invoice (Row) |
| isRemarkEnabled | Boolean | false | To either show or hide remarks |
| containerClassName | String | '' | Parent classname to override the styles of the list |


## Usage Example
```
Plan charrges form
```
```js
import { PlanCharges } from 'react-braintree-impl'

const PlanCharges = ({
    selectedDiscountType,
    selectedChargeType,
    handleChargeTypeSelect,
    handleDiscountTypeSelect,
    model,
    onChange,
    handleSubmit,
    schema,
    isEdited,
    slabsError,
    slabValidation,
    Input,
    Form,
    FieldArray,
    chargeTypeList,
    discountTypeList,
    Prompt
}) => (
    <PlanCharges
      selectedDiscountType={selectedDiscountType}
      selectedChargeType={selectedChargeType}
      handleChargeTypeSelect={handleChargeTypeSelect}
      handleDiscountTypeSelect={handleDiscountTypeSelect}
      model={model}
      onChange={this.onChange}
      handleSubmit={handleSubmit}
      schema={schema}
      isEdited={isEdited}
      slabsError={slabsError}
      slabValidation={this.slabValidation}
      Input={Input}
      Form={Form}
      FieldArray={FieldArray}
      chargeTypeList={chargeTypeList}
      discountTypeList={discountTypeList}
      Prompt={Prompt}
      containerClassName="plan-charges-container"
    />
);
```
## PROPTYPES
| Prop | Type | Default | Description | Sample |
| ---- | ---- | ------- | ----------- | ------ |
| selectedDiscountType | Object | {} | |
| selectedChargeType | Object | {} | |
| handleChargeTypeSelect | function | null | Charge type selection handler |
| handleDiscountTypeSelect | function | null | Discount type selection handler |
| model | Object | null | Plancharges object to be modified or written into  |
| onChange | function | null | Form onChange handler |
| handleSubmit | function | null | Submit handler |
| schema | object | null | yup schema object for the form Validation |
| isEdited | Boolean | false | Whether the form is touched (any value has been changed) |
| slabsError | Object | {} | Validated errors for slabs |
| slabValidation | function | null | validation method for slab |
| Input | Component | null | Input Component for form |
| Form | Component | null | Form Component to house the input components |
| FieldArray | Component | null | FieldArray component (Component capable of having array of fields) |
| chargeTypeList | Array | [] | List of charge types |
| discountTypeList | Array | [] | List of discount types |
| Prompt | Component | null | Prompt component to prompt on errors |
| containerClassName | String | '' | Parent classname to override the styles of the list |
