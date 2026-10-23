
Farmers Trading Market Information System


README  PROG101 Assignment 1

A logical-design project with a tested Flowgorithm prototype for agricultural produce discovery in Sierra Leone.



Key	Details
Module	PROG101  Principles of Programming Logic and Design
Assignment	Designing Logical Solutions for Sierra Leone Community Challenges
Deliverable	Logical design and tested Flowgorithm prototype
Repository URL	GitHub Repository:https://github.com/Dijaconteh/PROG101-ASSIGNMENT-1-KHADIJA-O-CONTECH_5744

Student ID	905005744
Student Name: KHADIJA O CONTEH



1. Project Overview

The Farmers Trading Market Information System is a programming-logic prototype designed around a community problem in Sierra Leone: farmers need a clearer way to communicate produce availability, while buyers need a straightforward way to find relevant listings.
The academic submission combines problem analysis, algorithms, pseudocode, modular Flowgorithm flowcharts, and sample program outputs. It demonstrates the intended logic; it is not a deployed agricultural marketplace.

2. Community Problem and Purpose

Produce information can be scattered across informal channels, making it difficult for buyers to locate available products, quantities, asking prices, and locations. Listing details also become outdated when stock or prices change.
The proposed solution structures this information and provides operations to publish, find, revise, and retire produce listings. Expected community benefits are proposed rather than measured in a field study.

3. Users and Permissions

• Farmer: May create and manage listings belonging to the farmer's registration record.
• Buyer: May search ACTIVE listings without being authorized to edit them.
• Authorized Market Assistant: May manage a farmer's listing only when a recorded farmer–assistant relationship exists. Knowing the farmer's ID alone does not grant permission.

4. Core Menu Operations

• 1. AddListing: Checks registration and actor authorization, collects produce details, validates them, supports RETRY/CANCEL, assigns a listing ID, and saves an ACTIVE record in shared arrays.
• 2. SearchListings: Searches saved ACTIVE listings by product and optional location; displays matching information or a no-results message.
• 3. UpdateListing: Finds the requested ID, checks ownership/delegation and ACTIVE status, validates new quantity and price, then updates the shared record.
• 4. MarkListingSold: Checks listing existence, authorization, and ACTIVE status, then records SOLD and excludes the listing from future ACTIVE searches.
• 5. IdentifyFarmer: Confirms registration and checks farmer/assistant authorization; returns a Boolean outcome.
Note: Option 0 exits the program.

5. Reusable Functions and Design Concepts

• Main: Menu control, shared arrays, counters, and procedure calls.
• Operational Modules: AddListing, SearchListings, UpdateListing, MarkListingSold, and IdentifyFarmer.
• farmerExists: Verifies an ID against the demonstration registered-farmer array.
• ISAuthorised: Permits a farmer acting for themselves or an assistant whose actor–farmer pair appears in the authorization records.
• Core Concepts: The solution demonstrates input–process–output, sequence, Boolean conditions, selection (If), repetition (While/For), functions, arrays, validation, and modular decomposition.

6. Prototype Data and Rules

• Data Structure: Listings are represented by parallel arrays containing identifiers, farmer identifiers, products, quantities, units, prices, locations, permitted contact preferences, and ACTIVE/SOLD statuses. Counters track the number of records. Demonstration farmer and assistant records are held in separate arrays.
• Validation Rules: Required text fields cannot be empty; quantity and price must be positive; only ACTIVE listings can be updated; SOLD listings are excluded from ACTIVE searches. Authorization applies to the specific farmer responsible for the listing.
• Limitations: Demonstration search uses exact text matching, so product/location capitalization matters. The current prototype stores records only during the running session; it does not create a persistent database or automatically store modification timestamps.

7. Running the Flowgorithm Prototype

1. Open FarmersTradingMarket_Final_Reviewed.fprg in Flowgorithm.
2. Select the Main module.
3. Run the chart and use the console to choose menu options 1–5 or 0 to exit.
🧪 Suggested Test Scenario: Add a valid Rice listing for registered farmer F001 ➔ search for it ➔ update quantity and price ➔ search again to verify updated values ➔ mark the listing SOLD ➔ search again to confirm it is no longer ACTIVE. Test RETRY/CANCEL and unauthorized actor denial as separate scenarios.
Sample farmer and assistant identifiers are demonstration data only. The program is not connected to a real farmer registry, public directory, or authentication provider.

8. Project Boundaries

• Out of Scope: Online orders, payment processing, transport/delivery, real-time verified market prices, deployed web/mobile applications, live farmer onboarding, external identity verification, operational database hosting, or production security testing.
• Academic Constraints: This assignment's brief states that source code is not required; the executable Flowgorithm chart is additional supporting evidence for the logical design, not a claim of a production system.

9. SDG, Open Source, and Digital Public Goods

• SDG Alignment: The proposed information service relates primarily to SDG 2 (Zero Hunger) through the potential improvement of agricultural market-information access and may contribute to more inclusive local economic participation.
• Licensing Note: Future open-source development could support adaptation by schools, communities, and public-interest organizations. However, this academic repository is not automatically a certified Digital Public Good, and the availability of files on GitHub does not by itself grant an open-source license. Any license should be selected and added explicitly.



