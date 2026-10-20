Farmers Trading Market Information System
README | PROG101 Assignment 1
A logical-design project with a tested Flowgorithm prototype for agricultural produce discovery in Sierra Leone.
Module	PROG101 — Principles of Programming Logic and Design
Assignment	Designing Logical Solutions for Sierra Leone Community Challenges
Deliverable	Logical design and tested Flowgorithm prototype
Repository URL	https://github.com/Dijaconteh/FARMER-TRADING-MARKET-INFORMATION-SYSTEM-.git
Student / ID	905005744
1. Project overview
The Farmers Trading Market Information System is a programming-logic prototype designed around a community problem in Sierra Leone: farmers need a clearer way to communicate produce availability, while buyers need a straightforward way to find relevant listings.
The academic submission combines problem analysis, algorithms, pseudocode, modular Flowgorithm flowcharts, and sample program outputs. It demonstrates the intended logic; it is not a deployed agricultural marketplace.
2. Community problem and purpose
Produce information can be scattered across informal channels, making it difficult for buyers to locate available products, quantities, asking prices and locations. Listing details also become outdated when stock or prices change.
The proposed solution structures this information and provides operations to publish, find, revise and retire produce listings. Expected community benefits are proposed rather than measured in a field study.
3. Users and permissions
•	Farmer — may create and manage listings belonging to the farmer's registration record.
•	Buyer — may search ACTIVE listings without being authorized to edit them.
•	Authorized market assistant — may manage a farmer's listing only when a recorded farmer–assistant relationship exists. Knowing the farmer's ID alone does not grant permission.
4. Core menu operations
•	1 — AddListing: checks registration and actor authorization, collects produce details, validates them, supports RETRY/CANCEL, assigns a listing ID and saves an ACTIVE record in shared arrays.
•	2 — SearchListings: searches saved ACTIVE listings by product and optional location; displays matching information or a no-results message.
•	3 — UpdateListing: finds the requested ID, checks ownership/delegation and ACTIVE status, validates new quantity and price, then updates the shared record.
•	4 — MarkListingSold: checks listing existence, authorization and ACTIVE status, then records SOLD and excludes the listing from future ACTIVE searches.
•	5 — IdentifyFarmer: confirms registration and checks farmer/assistant authorization; returns a Boolean outcome. Option 0 exits the program.
5. Reusable functions and design concepts
•	Main — menu control, shared arrays, counters, and procedure calls.
•	AddListing, SearchListings, UpdateListing, MarkListingSold and IdentifyFarmer — five operational modules.
•	farmerExists — verifies an ID against the demonstration registered-farmer array.
•	ISAuthorised — permits a farmer acting for themselves or an assistant whose actor–farmer pair appears in the authorization records.
•	The solution demonstrates input–process–output, sequence, Boolean conditions, selection (If), repetition (While/For), functions, arrays, validation and modular decomposition.
6. Prototype data and rules
Listings are represented by parallel arrays containing identifiers, farmer identifiers, products, quantities, units, prices, locations, permitted contact preferences and ACTIVE/SOLD statuses. Counters track the number of records. Demonstration farmer and assistant records are held in separate arrays.
Required text fields cannot be empty; quantity and price must be positive; only ACTIVE listings can be updated; SOLD listings are excluded from ACTIVE searches. Authorization applies to the specific farmer responsible for the listing.
Demonstration search uses exact text matching, so product/location capitalization matters. The current prototype stores records only during the running session; it does not create a persistent database or automatically store modification timestamps.
7. Running the Flowgorithm prototype
Open FarmersTradingMarket_Final_Reviewed.fprg in Flowgorithm and select Main. Run the chart and use the console to choose menu options 1–5 or 0 to exit.
Suggested test: add a valid Rice listing for registered farmer F001; search for it; update quantity and price; search again to verify updated values; mark the listing SOLD; search again to confirm it is no longer ACTIVE. Test RETRY/CANCEL and unauthorized actor denial as separate scenarios.
Sample farmer and assistant identifiers are demonstration data only. The program is not connected to a real farmer registry, public directory or authentication provider.
8. Project boundaries
Not included: online orders, payment processing, transport/delivery, real-time verified market prices, deployed web/mobile applications, live farmer onboarding, external identity verification, operational database hosting or production security testing.
This assignment's brief states that source code is not required; the executable Flowgorithm chart is additional supporting evidence for the logical design, not a claim of a production system.
9. SDG, open source and Digital Public Goods
The proposed information service relates primarily to SDG 2 (Zero Hunger) through the potential improvement of agricultural market-information access and may contribute to more inclusive local economic participation.
Future open-source development could support adaptation by schools, communities and public-interest organizations. However, this academic repository is not automatically a certified Digital Public Good, and the availability of files on GitHub does not by itself grant an open-source license. Any license should be selected and added explicitly.
10. Project files and repository submission
Recommended repository name: PROG101_Assignment1_StudentName_StudentID. Replace the placeholders with the actual student details before creating the GitHub repository.
Upload README.md, the final report, the eight exported functional flowcharts, the final tested .fprg file, and relevant genuine screenshot evidence. The report includes the revised algorithms and matching pseudocode; separate files may be supplied if the lecturer requests them.
Keep a genuine series of Git commits as you organize the deliverables. Insert the actual repository URL and screenshots of the repository page, README and commit history in the final report.
11. Verification and academic integrity
The Flowgorithm prototype was tested interactively for listing creation, search, update, SOLD-state behavior, registration and actor authorization, and invalid-input handling. Only genuine runs and screenshots should be used as evidence.
The system is an academic demonstration. Do not describe its illustrative data, planned benefits, or prototype tests as live deployment, field validation, permanent storage or professional security assessment.
