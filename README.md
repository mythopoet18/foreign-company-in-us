# Foreign Companies In The US

## Fun Fact

<b> Are there many foreign companies doing business in the US? </b> <br>
  Yes. Among 36,136 companies register with SEC, there are 4,325 ([11.97%](https://placehold.it/15/c5f015/000000?text=+)) foreign companies.

<b> Who are they? </b>
<iframe width="800" height="400" frameborder="0" scrolling="no" src="//plot.ly/~mythopoet/6.embed"></iframe>


<b> What do foreign companies do in the US? </b>
<iframe width="800" height="360" frameborder="0" scrolling="no" src="//plot.ly/~mythopoet/8.embed"></iframe>
<iframe width="800" height="580" frameborder="0" scrolling="no" src="//plot.ly/~mythopoet/12.embed"></iframe>
<iframe width="800" height="580" frameborder="0" scrolling="no" src="//plot.ly/~mythopoet/10.embed"></iframe>

## The Question
Should capital market investors moving from US-owned business to foreign-owned business? 


Some people say:<br>
  <ul type="disc">
  <li>Foreign IPOs are significantly more underpriced..<a href="https://www.researchgate.net/publication/229521875_Underpricing_of_Foreign_and_Domestic_IPOs_in_the_US_Market_Empirical_Evidence">Francis, Hasan and Li(2001)</a></li>
  
  <li>U.S. Stocks Are Dangerously Overvalued<a href="https://www.forbes.com/sites/jamesberman/2018/10/04/time-to-buy-the-emerging-markets/#2371a35960c2">...read</a></li>
  
  <li>385 tax rules makes US-owned business more competitive than foreign-owned business<a href="https://www.brookings.edu/blog/up-front/2017/08/10/the-385-tax-rules-make-american-businesses-more-competitive-treasury-should-keep-them/">...read</a></li>
  </ul>
  

[My plan](https://placehold.it/15/c5f015/000000?text=+)<br>
  Step 1: A full spectrum financial statement analysis to evaluate business risk and financial risk over time. Build structured panel dataset with following features (X):<br>
  <ul type="disc">
  <li>Earning: EPS, diluted EPS, Net Income, EBITDA</li>
  <li>Leverage ratios: DOL,DFL,DTL</li>
  <li>Working Capital: Current Ratio, turnovers</li>
  <li>Risk: Credit risk, Liquidity risk</li>
  <li>P/E ratio, growth of P/E ratio</li>
  <li>Growth rates</li>
  </ul>
  
  Step 2: Compare portfolio with US-owned companies and portfolio with foreign-owned companies.
  <ul type="disc">
  <li>Compare the mean of X:</li>
     <ul type="bullet">
     <li>H<sub>0</sub>: &mu;<sub>foreign</sub>=&mu;<sub>US</sub></li>
     <li>H<sub>0</sub>: &mu;<sub>foreign</sub>>&mu;<sub>US</sub></li>
     <li>H<sub>0</sub>: &mu;<sub>foreign</sub><&mu;<sub>US</sub></li>
     </ul>   
  <li>Test cyclical property: </li>
     <ul type="bullet">
     <li>Both US-owned and foreign-owned companies are cyclical/non-cyclical</li>
     <li>US-owned companies are cyclical; foreign-owned companies are non-cyclical</li>
     <li>US-owned companies are non-cyclical; foreign-owned companies are cyclical</li>
     </ul>  
  <li>Estimate Stochastic Dominance between US-owned portfolio and foreign-owned portfolio.<br> 
    <i>Literature: Kopa and Post(2009,2013), Post,Fang and Kopa(2015) test US market portfolio efficiency.</i> </li>
  </ul>
  
## Data

<a href="https://www.sec.gov/edgar/searchedgar/companysearch.html">EDGAR</a> is the major data source of this project. EDGAR is maintained by the Securities Exchange Committee, free to access to the public. According to SEC,<i> "All companies, foreign and domestic, are required to file registration statements, periodic reports, and other forms electronically through EDGAR."</i> Small business is not usually required to file with SEC electronicly. Banks file with FDIC and other banking industry regulators. 


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

Project Site Link: https://mythopoet18.github.io/foreign-company-in-us/
