Literature\_Review
================
Erik Carlson
11/09/2020

## EPA Data

The data I am using is the EPA Enforcement and Compliance history
database (ECHO). It is a database constiting of the EPA’s inspection,
compliance and enforecement data. I am focusing on EPA formal
pentalties. Following this are a few papers I read to understand their
methodologies using the same dataset.

## Environmental Sentencing in the United States Pacific Northwest 2007–2011: A Story of Disparity

Joseph Kremer analyzed environmental enforcement risk and enforcement
disparity in minority and low-income neighborhoods. He looked only at
the years 2007-2011 for EPA region 10, which consists of Alaska, Idaho,
Oregon, and Washington State (Kremer, 2016).

  - First, the data was cleansed by removing financial penalties listed
    that were not actual penalties, but were instead tagged as unrelated
    repayments to the enforcement agency.  
  - Then in the rare instance where one enforcement case led to multiple
    facility fines, only the first facility was used for analysis
  - Since demographic data was the primary concern for the analysis,
    data with missing geographic data were not used

The dependent variable used was the same as my preliminary dependent
variable, total monetary penalty. In order control for issues such as
omitted variable bias, multiple independent variables were used. These
included:

**Violation Type**

The type of violation has an impact on the penalty received. The
violation type was controlled for by using a series of binary variables
that were 1 if it violated a particular environmental violation. These
violations included:

1.  The Resource and Recovery Act (RCRA) RCRA violations deal with
    hazardous waste, and example of an RCRA violation is a gas station
    storage tank leaking into the ground water.
2.  The Comprehensive Environmental Response, Compensation, and
    Liability Act (CERCLA) CERCLA violations involve failures in
    addressing the cleanup of contaminated sites. An example of a
    violation is not notifying the relevant authorities that chemical
    solvents were spilled in a nearby storm drain.
3.  Clean Air Act (CAA)
4.  Clean Water Act (CWA) 5.. Toxic Substances Control Act (TSCA)
5.  EPCRA and FIFRA were used as the omitted binary variables These
    stand for The Emergency Planning and Community Right to Know Act and
    the Federal Insecticide, Fungicide, and Rodenticid Act.

**Violation Severity**:

Two binary variables were used to control for severity of a violation

1.  Whether the issue was voluntarily disclosed, and the case was
    expedited EPA policy allows for voluntary disclosure of minor
    violations for a reduced penalty and are expedited through the
    enforcement process
2.  Whether violations occurred at multiple facility locations This was
    included because facilities with violating locations are overall
    more severe violators and can be controlled for.

**Facility Characteristics: Size and economic power of entity may affect
sentencing**

Small violators make up large part of dataset. Larger companies have
fewer number of fines are generally fines less. Kremer controlled with
binary variables for:

1.  Identify Fortune 500 companies.
2.  Identifying government agencies such as schools, firehouses, and
    water treatment plant as they receive different treatments
3.  Variable repeat offender, since repeat offenders get penalized more.
    It is a possibility that repeat offenders make up large portion of
    the dataset so it should be controlled for.
4.  Toxic release inventory (TRI) facilities that primarily deal with
    specific toxic chemicals in amounts greater than 25,000 pounds.
    These specific facilities should be controlled for.
5.  Some facilities have permits that allow the firms to pollute both
    the air and water. Having multiple permits may lead to greater
    non-compliance risk since they can pollute through multiple
    environmental mediums. Variable for facilities with multiple
    environmental permits may be needed.

**Year of Violation:**

A major point of interest was how time was used in the analysis. Rather
than using a year-demeaned OLS regression or a time series analysis, the
years were included with T-1 binary regressors. Thus, a regressor was
used for 2008,2009, 2010 and 2011. Since the main concern of the paper
was communities, variables for sociodemographic local communities were
also included as the main variables of interest. These variables may be
important to control for, but not at such a local level. Following the
selection of the variables the main methodology in order is as follows.

**Method:**

1.  Preliminary analysis of bivariate relationships of community
    demographic and fine severity
2.  Mean and median fine amounts as well as severity characteristics
    across differing community types with percentile ranking of
    different variables. For example the income and race variables were
    normalized so it ranged from 0 to 1.
3.  Do two tailed t-tests to compare mean fine amount for race,
    ethnicity, household income, and homeownership. Do the same tests
    for violation severity against same parameters.
4.  Do the entire OLS regression for a more robust assessment

Using this metholology Kremer showed that controlling for other factors,
fines and penalties were less severe in low-income neighborhoods in the
region studied.

## When threats become credible: A natural experiment of environmental enforcement from Florida

Blundell used a technique to measure time differences using a
Differences in Differences technique in his analysis on Florida’s
enforcement data. He was investigating the effects of possible increased
enforcement following 2012 state policy changes. Differences in
differences is used to emulate experimental design of a control and
treatment group, however in this case the control the dataset before
2012, and the treatment group was the dataset after 2012. Overall
difference in difference is both useable and applicable to analyzing
changes in enforcement in the year to date. However this was only usable
because their dependant variable was entity compliance based on lagged
enforcement actions in each time period. This allowed for both the
pre-2012 and post-2012 to have a compliance-rate, then after epa actions
having a second compliance rate. Then comparing the changes using
differences in differences between the two time periods. Using this
methodology would require accessing a more indepth and specific dataset
that has each entity’s compliance status in each quarter.

Using this methodology they were able to show that changes in enforement
post 2012, including actions such as increasing penalties for
high-priority facilities, did improve entity compliance.

## References

Blundell, W. (2020). When threats become credible: A natural experiment
of environmental enforcement from Florida. Journal of Environmental
Economics and Management, V101.

Kremer, J. (2016). Environmental Sentencing in the United States Pacific
Northwest 2007–2011: A Story of Disparity. Sociological Perspectives,
528-542.
