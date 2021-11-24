---
layout: page
title: HousingHelper (Capstone)
---
<h1>
HousingHelper 🏠 (Capstone Project)
</h1>
<hr>

I'm in the <a href="https://www.schoolofcities.utoronto.ca/multidisciplinary-urban-capstone-project" target="_blank">Multidisciplinary Urban Capstone Project</a> at UofT, working in a team of 6 students to design a new affordable housing development. 

<img src="{{ site.url }}/assets/oda.jpg">
*our development is 100% not looking like this*

To say this goes beyond the scope of my studies would be an understatement, but this is an opportunity for some product development - because anything is an opportunity for product development 😎

I decided to take the lead on building a tool that **produces design requirements and analyses the financial feasibility of alternatives.** I've documented my thinking below:

<h2>Context</h2>
Our capstone client is a collective of public and private stakeholders (e.g. the City, engineering design firms) with the mandated goal of creating long-lasting affordable housing in Toronto.

They have 3 operational pillars (which loosely translate into epics):
1. Does it pencil? (is it feasible)
2. Does it scale? (can they have practices that translate to other sites)
3. How can we accelerate delivery?

Our specific project tasks us with proposing a development on a specific site. We scoped this ask down into 2 deliverables:
1. Masterplan (the architectural design)
2. Business plan

<h2>Product Vision</h2>
I'll admit it - this isn't a small task for anyone, let alone 6 undergraduate students. **The motivation behind making HousingHelper is to simply make our lives easier + deliver long-term value to our client.** The following is some loose thinking to come up with the ideal state for the tool. 

I'm focusing on the *business plan* side of the 2 deliverables. I realised that this tackles *Pillar 1 (does it pencil)* by:
1. Guiding the physical design by explaining what is financially feasible i.e. optimise the layout/functions for profitability and social benefit
2. Quantifying that feasibility e.g. determining profitability, payback periods

*Pillar 2 (does it scale)* could then be achieved by a separate tool that identifies similar sites based on input parameters (e.g. clustering census tracts in Toronto based on construction costs, incomes, rents), but might be something for another day.

For good measure, I threw this into the Crossing the Chasm framework:

- **For** Client stakeholders and design teams (including us)
- **Who** want to determine key design requirements for potential developments
- **HousingHelper is** a calculator/optimiser 
- **That** produces multiple sets of financially feasible alternatives

<h2>Specifications</h2>

<h3>Product summary</h3>

There are several things to optimise and produce sets of: 

*Residential usage*
- Setaside percentage (% of housing that is affordable, >30% for us)
- Unit type split

*Non-residential usage*
- Commercial usage split (e.g. retail, office)
- Amount of commercial (residential is generally fixed e.g. at least x units)
- Number of parking spots

Parameters that are relevant for optimisation (and may require user input):

<table>
  <tr>
    <th></th>
    <th>Construction</th>
    <th>Permanent</th>
  </tr>
  <tr>
    <th>Revenues (variable)</th>
    <td>Investors, city funding, developer equity, loans</td>
    <td>Rental units, commercial rental</td>
  </tr>
  <tr>
    <th>Costs</th>
    <td>Hard costs (fixed), soft costs (fixed), land (nominal), subsidies (variable)</td>
    <td>Loan repayments, operating costs e.g. maintenance and taxes (all variable)</td>
  </tr>
</table>

<h3>Business case for HousingHelper</h3>
Our client retains accountants that can produce industry-standard pro formas and cash flow statements, so that’s not our job. 

What we intend to do is **provide preliminary estimates** of the variables outlined in the Optimise section, producing ballpark requirements that can serve as guidelines for further investigation.

Creating a dynamic tool allows this process to be repeated efficiently with new parameters and across different sites in the future, **bringing lasting value to the client beyond our capstone** and speeding up their workflow. 

In the immediate term, HousingHelper helps our design team evaluate more options and get things done quicker. 

<h3>User stories</h3>
These aren't based solely on client-side stakeholders, but also our own team members (since this is an internal tool that will be used by design teams in the future). These were created based off client meetings and internal team discussions.

**As an** architectural practice
- **We want to** know the firm requirements of the development e.g. number of floors available for retail
- **So that we can** actually design the thing

**As a** planning organisation
- **We want to** evaluate the financial feasibility of the development
- **So that we can** obtain funding, plan budgets, and start necessary conversations

**As a** community organisation
- **We want to** know what types of uses will be available
- **So that we can** make arrangements to relocate people or complement non-residential uses


<h2>Roadmapping and prioritisation</h2>

<h3>Epic 1: does it pencil</h3>
I'll undertake the development process in 3 stages, largely corresponding to these 3 stories. This roadmapping also isn't spec'd out to the max, because I still need to work out the nitty gritty of the calculation process 😬

**Story 1: physical details**

Output several scenarios with different
- Residential floors
- Commercial space
- Parking spots

Potential inputs 
- Expected occupancy rates for unit types
- Size restrictions (height, max num units, floor plate area)
- Demographics (income, diversity)

**Story 2: finances**

Calculate the following for each output scenario 
- Setaway percentage
- Projected revenues
- Projected costs mostly constant
- → Breakeven duration 

**Story 3: usage**
- Unit types
- Specific non-residential uses

With this breakdown, I have a clearer sense of the product:

- The functionality of stories 1 and 2 are complementary; changing the parameters/outputs of one will update the other 
- The usage of story 3 can be applied to whatever scenario has been selected

<h3>Epic 2: does it scale (later on)</h3>

There's room here to crack out some stats e.g. clustering areas in Toronto, identifing similar clusters to a user input

<h2>Actual design</h2>
In progress, stay tuned 😈


