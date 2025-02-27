---
layout: index
title: Saudi Sign Language Competetion
description: IEEE Competetion from SDAIA 
---



## Introduction

This dataset is the result of a collaborative effort between King Fahd University of Petroleum and Minerals (KFUPM) and the National Center for Artificial Intelligence (NCAI). It contains sign language data collected from a diverse group of signers, designed to support research and development in the field of sign language recognition and related AI applications.

## Data Summary

The dataset includes sign language sentences from a variety of signers, capturing different signing styles and contexts. Below is a brief overview of the dataset:

- **Number of Signers**: 18
- **Total Hours of Video**: 35 hours
- **Data Splits**: 
  - **Training Split**:
    - Includes three female signers and eleven male signers.
    - The total duration of the training split is 28 hours.

  - **Validation Split**:
    - The validation split contains two signers, one male and one female, with their sentences included but the signers are unseen.
    - The total duration of this split is 6 hours.

  - **Test Split**:
    - The test split is 7 hours in total, consisting of:
      - **Test 1**: Unseen signers and unseen sentences.
      - **Test 2**: Seen signers and unseen sentences.
      - **Test 3**: Seen sentences and unseen signers.

The table below summarizes the data for each split based on the sentences, minutes, seen sentences, seen signers, and other parameters.

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
        <th><strong>Sentences</strong></th>
        <th><strong>Minutes</strong></th>
        <th><strong>Seen Sentences</strong></th>
        <th><strong>Seen Signers</strong></th>
        <th><strong># Sentences</strong></th>
        <th><strong># Signers</strong></th>
        <th><strong>Gender</strong></th>
        <th><strong>Split</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>200</td>
        <td>16.65</td>
        <td>No</td>
        <td>No</td>
        <td>100</td>
        <td>2</td>
        <td>1F, 1M</td>
        <td>Test 1</td>
      </tr>
      <tr>
        <td>1100 (1097)</td>
        <td>90.10</td>
        <td>No</td>
        <td>Yes</td>
        <td>100</td>
        <td>11</td>
        <td>2F, 9M</td>
        <td>Test 2</td>
      </tr>
      <tr>
        <td>3800 (3783)</td>
        <td>337.33</td>
        <td>Yes</td>
        <td>No</td>
        <td>1900</td>
        <td>2</td>
        <td>1F, 1M</td>
        <td>Test 3</td>
      </tr>
      <tr>
        <td>4000</td>
        <td>374</td>
        <td>Yes</td>
        <td>Mix</td>
        <td>2000</td>
        <td>2</td>
        <td>1F, 1M</td>
        <td>valid</td>
      </tr>
      <tr>
        <td>20311</td>
        <td>1661</td>
        <td>Yes</td>
        <td>Yes</td>
        <td>-</td>
        <td>14</td>
        <td>3F, 11M</td>
        <td>Train</td>
      </tr>
    </tbody>
  </table>
</body>
</html>

## Size per Split
The dataset will be available in the following format:
  <div class="list-container">
    <ul>
      <li><strong>Training:</strong> 24.50 GB</li>
      <li><strong>Validation:</strong> 5.24 GB</li>
      <li><strong>Test Total:</strong> 7.66 GB
        <ul class="sub-list">
          <li><strong>Test 1:</strong> 0.39 GB</li>
          <li><strong>Test 2:</strong> 1.31 GB</li>
          <li><strong>Test 3:</strong> 5.96 GB</li>
        </ul>
      </li>
    </ul>
  </div>


## Data Access
- **Data Acess Requirement**: Access to the dataset will require prior registration. Please visit to sign up and gain access.


## License and Citation

Please adhere to the license guidelines provided [Insert license details here]. When using this dataset in your research, kindly cite the following paper:
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
