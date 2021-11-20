# Lucky-Markteplace

## Decentralized marketplace where with a bit of luck you can buy stuff for less or convert your old stuff in crypto at full price
A community composed of various roles:
Sellers - sell their items to a limited number of people at full of the listed price.
Buyers - buy items at a fraction of the listed price by risking their amounts.
Judges - help resolve various cases that might arise between sellers and buyers by earning a reward. 

## Happy path
1. Alice submits an item for sale (title, description, location, carrier, price, number of people that can participate, deadline to enter). Alice also needs to deposit some amount equal to the price she is willing to sell the item (prevents spam and malicious activities). After the sale she receives (price + deposited amount).

2. People start depositing fractions of the listed price (item price / available positions) until all available positions are filled.

3. Once all available positions are filled, a winner is selected at random.

4. Let's say Bob is selected as a winner, he pays only a fraction of the listed price, but he will receive the item after Alice ships it. Alice will receive the total price (Bob's amount + other participants amounts)

5. Once there is a prove (by tracking number) that Bob received the item, funds are released to Alice. (shipping by courier with mandatory inspection and test, to automatedly track the shipment to establish a successful delivery)

## Sad path:
 - Deadline is reached before all positions are filled. The sale is canceled and Alice covers any costs since it is her fault that the item listing is not attractive enough.

- Alice refuses to fulfill her obligation to ship the item. A penalty fee is deducted from her. Participants receive their deposited funds back.

- Alice does not provide the necessary proof of shipment within the pre-regulated period (it is a parameter for the conditions of the sale). The sale is canceled due to Alice's fault and a penalty fee is deducted from her. Participants receive their deposited funds back.

- Courier cannot deliver the product / Bob is not found and the package is returned to Alice. Participants receive their deposited funds back. (have to think about how the possible costs of are covered)

- Bob refuses the shipment and it is returned to Alice.
1. Alice's fault (non-working, broken, missing parts, different from the description). Participants receive their deposited funds back. The sale is canceled due to Alice's fault and the corresponding penalty fee is deducted. To prove the truth of the claim, Bob must provide photo/video material. Judges might need to step in and help resolve the case.

2. Bob's fault (doesn't want the product). Participants receive their deposited funds back. The sale is canceled due to Bob's fault and the respective penalty fee is deducted.

3. The shipment is lost by the courier. The sale is canceled and participants receive their deposited funds back. (have to think about how the possible costs of are covered)

Each of the described cases can be identified via the API of the respective courier. Have to think about the conditions to break the contract in case one of the parties does not cooperate.

## UI/UX
1. Landing page
- shows a navigation bar (logo, search bar, ...)
- shows a list of available sales for participation

2. New Item page - shows a form for new listing creation with all the different properties
- Category
- Title
- Description
- Images
- Shipping location (address1, address2, zip, state, city, country)
- Shipping carrier (DHL, ...)
- Price
- Manager collateral (from the person who listed the item)
- Max available slots (people to participate)
- Entrance deadline (max days for entrance)
- Shipping deadline
- Delivery deadline
- Approval deadline

3. Item page
- The manager
- The current balance
- The status (started, shipped, delivered, approved, finalized)
- All participants
- The winner

4. Search
- Filter by keywords in the title and description
- Filter by price
- Filter by location
- Filter by delivery method 
- Sort by price, remaining time, latest

5. Things to add
- Overall user rating aimed at showing the reliability of the seller
- Number of successfully created and completed sales
- Number of failed sales as seller
- Number of successfully won sales
- Number of failed sales as buyer
- Number and list of active sales created by the user