# Forecast Financial Ratios - An Alternative Approach

## Objective
Financial analyst and regulators often rely on the ratio analysis to investigate a company. For example, the current ratio has to be above a certain threshold to be considered liquid.

However, financial statements may not be available to invetors. This is not rare, especially among foreign companies and new comers. The end product of my project will be an app to predict financial ratios based on 

 <ul type="disc">
  <li>Company Name</li>
  
  <li>Address</li>
  
  <li>Industry</li>
</ul>

## Model
### Label
The ```Y``` variable is a set of financial ratios. 

Computed from over ```80 million``` SEC financial statement filing entries, including ```36,136``` SEC registered companies, ranging from 2009 to 2019.

### Categorical Features

I extrated registration information from SEC filing, including

  <ul type="disc">
  <li>Company Name</li>
  <li>Industry SIC code</li>
  <li>Business Address</li>
  <li>Mailing Address</li>
  <li>Registration Address</li>
  <li>Number of subordinate companies or associates</li>
  <li>Size of the company</li>  
  </ul>

### Sentiment Features

Search company name in twitter to scrap comments. Then apply sentiment analysis to generate a company specific score using NLP.

## SEC Filing Data

<a href="https://www.sec.gov/edgar/searchedgar/companysearch.html">```EDGAR```</a> is the major data source of this project. EDGAR is maintained by the Securities Exchange Committee, free to access to the public. According to SEC,<i> "All companies, foreign and domestic, are required to file registration statements, periodic reports, and other forms electronically through EDGAR."</i> Small business is not usually required to file with SEC electronicly. Banks file with FDIC and other banking industry regulators. 


Financial statement (<a href="https://www.sec.gov/Archives/edgar/data/1639920/000156459019002688/ck0001639920-20f_20181231.htm#ITEM_8_INFORMATION_FINANCIAL">Sample 20-F form</a>): quarterly financial statement filing data from 2009Q1 to 2018Q4 (<a href="https:https://www.sec.gov/dera/data/financial-statement-data-sets.html">link</a>). The size of all text form data is 40G.


Filing information example:<br>
adsh	tag	version	coreg	ddate	qtrs	uom	value	footnote<br>
0000107687-18-000026	EBITDA	0000107687-18-000026		20160831	4	USD	71943000.0000	<br>
0000107687-18-000026	EBITDA	0000107687-18-000026		20170831	4	USD	157411000.0000	<br>
0000107687-18-000026	EBITDA	0000107687-18-000026		20180831	4	USD	180063000.0000	<br>
0000081362-18-000012	DeferredRevenue	us-gaap/2018		20171231	0	USD	1500000.0000	<br>
0001564590-18-026237	DeferredRevenue	us-gaap/2018		20171231	0	USD	9374000.0000	<br>
0001564590-18-026237	DeferredRevenue	us-gaap/2018		20180930	0	USD	9128000.0000	<br>
... <br>

## Project Site Link
https://mythopoet18.github.io/foreign-company-in-us/ <br>

### Fun Plot
