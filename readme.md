# rn-survey

rn-survey is a react-native library for dealing with survey form generation. using this library you can save forms offline (Asyncstorage).

## Installation

Use the package manager [npm](https:) to install rn-survey.

```bash
npm install rn-survey
```

## Usage

```javascript
import Survey from 'rn-survey';

......
//sample JSON
const metaData = [
    {
      type: 'text',
      question: 'What is your name?',
      isMandatory: true,
      qstnKey: 'test1',
    },
    {
      type: 'single',
      question: 'Are you vaccinated?',
      isMandatory: true,
      qstnKey: 'test2',
      options: [
        {
          key: 'Yes',
          value: 'Yes',
        },
        {
          key: 'No',
          value: 'No',
        },
      ],
    },
    {
      type: 'multiple',
      question: 'Please select your preferred locations?',
      isMandatory: true,
      qstnKey: 'test3',
      options: [
        {
          key: 'Trivandrum',
          value: 'Trivandrum',
        },
        {
          key: 'Kochi',
          value: 'Kochi',
        },
        {
          key: 'Bangalore',
          value: 'Bangalore',
        },
      ],
    },
    {
      type: 'text',
      question: 'Please enter your comments',
      isMandatory: false,
      qstnKey: 'test4',
      options: [
        {
          key: 'option 1',
          value: 'option1',
        },
        {
          key: 'option 2',
          value: 'option2',
        },
        {
          key: 'option 3',
          value: 'option3',
        },
      ],
    },
  ];
........
...........

 <Survey
        metaData={metaData}
        onSubmit={submit}
        formId={data.id + '_' + userName}
      />

```
## Props
1.metaData: survey data

2.onSubmit: calls when survey submitted and returns answers as an object

3:formId: unique Id for form

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https:\)