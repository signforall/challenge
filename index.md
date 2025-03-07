---
layout: default
---


# The SignforAll 2025 Challenge

Welcome to The SignforAll 2025 Challenge, showcasing the Saudi Sign Language (SSL). This competition is dedicated to advancing SSL sign language recognition by addressing key challenges, including the recognition of signs from unseen signers, unseen sentence, and conditions involving face coverings from the SSL dataset.
## Task Description
Participants will develop models to translate SSL signs into text. There are three tracks:

- **Track 1 - Model Generalization on Unseen Signers**: Recognize SSL signs performed by unseen signers, but with seen sentences.
- **Track 2 - Model Generalization on Unseen Sentences**: Recognize SSL signs performed by seen signers, but with unseen sentences.
- **Track 3 - Model Generalization on Unseen Signers and Sentences**: Recognize SSL signs performed by fully unseen signers and sentences.

**BLEU score is the accepted evaluation metric, using the SacreBLEU library.**

## Base Line Results:
The results from training the model on T5 variant models on the pose features are shown in the table below:  


<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Styled Table</title>
  <style>
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 20px 0;
      font-family: Arial, sans-serif;
    }
    th, td {
      border: 1px solid #ddd;
      padding: 8px 12px;
      text-align: center;
    }
    th {
      background-color: #4CAF50;
      color: white;
    }
    tr:nth-child(even) {
      background-color: #f2f2f2;
    }
    tr:hover {
      background-color: #ddd;
    }
    td {
      font-size: 14px;
    }
    th {
      font-size: 16px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <table>
    <thead>
      <tr>
        <th></th>
        <th colspan="4"><strong>Test-1</strong></th>
        <th colspan="4"><strong>Test-2</strong></th>
        <th colspan="4"><strong>Test-3</strong></th>
      </tr>
      <tr>
        <th><strong>Models</strong></th>
        <th colspan="4"><strong>Unseen Signers - Unseen Sentences</strong></th>
        <th colspan="4"><strong>Seen Signers - Unseen Sentences</strong></th>
        <th colspan="4"><strong>Unseen Signers - Seen Sentences</strong></th>
      </tr>
      <tr>
        <th></th>
        <th><strong>BLEU-1</strong></th>
        <th><strong>BLEU-2</strong></th>
        <th><strong>BLEU-3</strong></th>
        <th><strong>BLEU-4</strong></th>
        <th><strong>BLEU-1</strong></th>
        <th><strong>BLEU-2</strong></th>
        <th><strong>BLEU-3</strong></th>
        <th><strong>BLEU-4</strong></th>
        <th><strong>BLEU-1</strong></th>
        <th><strong>BLEU-2</strong></th>
        <th><strong>BLEU-3</strong></th>
        <th><strong>BLEU-4</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>T5-Base</strong></td>
        <td>24.05</td>
        <td><strong>9.59</strong></td>
        <td><strong>4.96</strong></td>
        <td><strong>2.73</strong></td>
        <td>24.46</td>
        <td>9.14</td>
        <td>4.53</td>
        <td>2.01</td>
        <td>84.07</td>
        <td>81.09</td>
        <td>80.59</td>
        <td>80.37</td>
      </tr>
      <tr>
        <td><strong>T5v1.1-Base</strong></td>
        <td><strong>26.16</strong></td>
        <td>9.25</td>
        <td>4.39</td>
        <td>1.59</td>
        <td><strong>26.87</strong></td>
        <td><strong>11.25</strong></td>
        <td><strong>6.05</strong></td>
        <td>2.78</td>
        <td><strong>88.46</strong></td>
        <td><strong>86.27</strong></td>
        <td><strong>85.84</strong></td>
        <td><strong>85.75</strong></td>
      </tr>
      <tr>
        <td><strong>mT5-Base (English)</strong></td>
        <td>23.63</td>
        <td>8.32</td>
        <td>3.98</td>
        <td>1.46</td>
        <td>26.72</td>
        <td>10.53</td>
        <td>5.42</td>
        <td><strong>2.79</strong></td>
        <td>87.76</td>
        <td>85.62</td>
        <td>85.22</td>
        <td>85.16</td>
      </tr>
      <tr>
        <td><strong>mT5-Base (Arabic)</strong></td>
        <td>10.84</td>
        <td>2.99</td>
        <td>1.28</td>
        <td>0.72</td>
        <td>13.3</td>
        <td>4.28</td>
        <td>1.64</td>
        <td>0.66</td>
        <td>85.54</td>
        <td>84.27</td>
        <td>83.99</td>
        <td>83.87</td>
      </tr>
    </tbody>
  </table>

The results show that fine-tuning on pretrained checkpoints significantly improves model performance, as indicated by higher BLEU scores across all test sets. 
The improvement suggests that incorporating domain-specific data during pre-training helps enhance the model's generalization ability. Models fine-tuned on pretrained checkpoints perform better, especially on unseen data, highlighting the benefits of such an approach. For a more detailed comparison, please refer to the baseline paper.


  <table>
    <thead>
      <tr>
        <th></th>
        <th colspan="4"><strong>Test-1</strong></th>
        <th colspan="4"><strong>Test-2</strong></th>
        <th colspan="4"><strong>Test-3</strong></th>
      </tr>
      <tr>
        <th><strong>Models</strong></th>
        <th colspan="4"><strong>Unseen Signers - Unseen Sentences</strong></th>
        <th colspan="4"><strong>Seen Signers - Unseen Sentences</strong></th>
        <th colspan="4"><strong>Unseen Signers - Seen Sentences</strong></th>
      </tr>
      <tr>
        <th></th>
        <th><strong>BLEU-1</strong></th>
        <th><strong>BLEU-2</strong></th>
        <th><strong>BLEU-3</strong></th>
        <th><strong>BLEU-4</strong></th>
        <th><strong>BLEU-1</strong></th>
        <th><strong>BLEU-2</strong></th>
        <th><strong>BLEU-3</strong></th>
        <th><strong>BLEU-4</strong></th>
        <th><strong>BLEU-1</strong></th>
        <th><strong>BLEU-2</strong></th>
        <th><strong>BLEU-3</strong></th>
        <th><strong>BLEU-4</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>T5-Base</strong></td>
        <td><strong>35.89</strong></td>
        <td><strong>17.33</strong></td>
        <td><strong>11.14</strong></td>
        <td><strong>7.48</strong></td>
        <td><strong>35.78</strong></td>
        <td><strong>17.53</strong></td>
        <td><strong>10.34</strong></td>
        <td><strong>5.72</strong></td>
        <td><strong>95.17</strong></td>
        <td><strong>94.02</strong></td>
        <td><strong>93.78</strong></td>
        <td><strong>93.67</strong></td>
      </tr>
      <tr>
        <td><strong>T5v1.1-Base</strong></td>
        <td>34.76</td>
        <td>16.79</td>
        <td>10.05</td>
        <td>5.56</td>
        <td>35.59</td>
        <td>16.96</td>
        <td>9.92</td>
        <td>5.23</td>
        <td>94.5</td>
        <td>93.16</td>
        <td>92.83</td>
        <td>92.58</td>
      </tr>
      <tr>
        <td><strong>mT5-Base (English)</strong></td>
        <td>33.5</td>
        <td>16.07</td>
        <td>9.77</td>
        <td>5.66</td>
        <td>32.92</td>
        <td>14.85</td>
        <td>8.52</td>
        <td>4.74</td>
        <td>94.64</td>
        <td>93.44</td>
        <td>93.19</td>
        <td>93.04</td>
      </tr>
      <tr>
        <td><strong>mT5-Base (Arabic)</strong></td>
        <td>16.75</td>
        <td>5.4</td>
        <td>1.86</td>
        <td>0.81</td>
        <td>18.16</td>
        <td>6.37</td>
        <td>2.66</td>
        <td>1.47</td>
        <td>92.97</td>
        <td>92.37</td>
        <td>92.42</td>
        <td>92.48</td>
      </tr>
    </tbody>
  </table>
</body>
</html>


## Baseline 

To replicate our results, please follow the steps outlined in our GitHub repository.

You can access the repository via the following link:

[GitHub Repository](https://github.com/signforall/t5-training-scripts)

## Important Dates

- ** 📅 Release train data: March 10, 2025 **
- ** 📅 Release test data: April 28, 2025 **
- ** 📅 Release eval results: May 1, 2025 ** 
- ** 📅 Paper Submission Deadline: May 10, 2025 **
- ** 📅 Notification of Acceptance: June 24, 2025 **
- ** 📅 Camera-Ready Submission: July 15, 2025 **


## Licence
Creative Commons Attribution-NonCommercial (CC BY-NC)

## Contact
For questions use the following contact email:  
Email: [signforall@googlegroups.com](signforall@googlegroups.com)

## Organizers 

- **Ali Alhejab - SDAIA, Riyadh, Saudi Arabia **
- **Lamya Alkanhal - SDAIA, Riyadh, Saudi Arabia **
- **Tomas Zelezny - University of West Bohemia, Pilsen **
- **Jakub Straka - University of West Bohemia, Pilsen **
- **Badria Almutaani- SDAIA, Riyadh, Saudi Arabia **
- **Yazeed Alharbi - SDAIA, Riyadh, Saudi Arabia **
- **Ahmed Ali - SDAIA, Riyadh, Saudi Arabia **


<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Styled List</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    .list-container {
      background-color: #f9f9f9;
      border: 1px solid #ddd;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
    h2 {
      color: #4CAF50;
      font-size: 24px;
      margin-bottom: 10px;
    }
    ul {
      list-style-type: none;
      padding-left: 20px;
    }
    li {
      font-size: 16px;
      line-height: 1.6;
    }
    li::before {
      content: "• ";
      color: #4CAF50;
    }
    .sub-list {
      margin-left: 20px;
      font-size: 14px;
      color: #555;
    }
  </style>
</head>
<body>
