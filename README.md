---

# E-Commerce Product Ontology (OWL 2 DL)

An OWL 2 DL ontology modelling an online shopping platform domain.

## Overview

| Metric | Value |
|---|---|
| OWL Profile | OWL 2 DL |
| Serialisation | RDF/XML |
| Reasoner tested | HermiT 1.4 |
| Named classes | 31 |
| Object properties | 12 |
| Data properties | 11 |
| Named individuals | 25 |
| Equivalent class axioms | 9 |
| Property chains | 1 |

## Classes (31)

**Core:** Brand, Category, Customer, Seller, Order, Product, Review, PaymentMethod

**Payment subclasses:** CreditCard, PayPal, BankTransfer, CryptoCurrency

**Product subclasses:** Electronics, Accessories, Laptop, Smartphone, Tablet, Headphones, SmartWatch, Cable, Charger, Case

**Defined classes (auto-classified by reasoner):** PremiumProduct, BudgetProduct, DiscountedProduct, HighRatedProduct, GamingLaptop, GamerCustomer, FrequentBuyer, LoyalCustomer, VerifiedReview

## Object Properties (12)

purchases, isPurchasedBy, manufacturedBy, manufactures, placesOrder, isOrderOf, containsProduct, usesPaymentMethod, reviewsProduct, hasReview, hasSubcategory, prefersBrand

## Data Properties (11)

hasPrice, hasDiscountPercentage, hasAggregateRating, hasRating, hasSKU, hasOrderID, hasTotalAmount, hasDeliveryStatus, hasOrderCount, isGamingLaptop, isVerifiedPurchase

## Individuals (25)

**Brands:** Apple, Samsung, Asus, Sony, Anker

**Products:** MacBookPro, iPhone15Pro, GalaxyS24Ultra, ROGZephyrus, SonyHeadphones, AnkerCharger

**Customers:** Customer_Ali, Customer_Sara, Customer_Riya, Customer_Lena

**Orders:** Order001, Order002, Order003, Order004

**Payment methods:** PM_Visa, PM_Mastercard, PM_PayPal, PM_Bitcoin

**Reviews:** Review001, Review002

## OWL 2 DL Features

- equivalentClass, intersectionOf, unionOf, subClassOf
- someValuesFrom, hasValue, minQualifiedCardinality, qualifiedCardinality
- FunctionalProperty, AsymmetricProperty, TransitiveProperty, IrreflexiveProperty
- owl:inverseOf, owl:propertyChainAxiom, owl:AllDifferent
- Datatype facets: xsd:minInclusive, xsd:maxExclusive

## Property Chain

purchases o manufacturedBy → prefersBrand

If a Customer purchases a Product manufactured by a Brand, the reasoner infers the Customer prefersBrand that Brand.

## Reasoning Results (HermiT 1.4)

| DL Query | Result |
|---|---|
| LoyalCustomer | Customer_Ali, Customer_Riya |
| FrequentBuyer | Customer_Ali, Customer_Lena, Customer_Riya |
| PremiumProduct | MacBookPro, iPhone15Pro, ROGZephyrus |
| DiscountedProduct | GalaxyS24Ultra, SonyHeadphones, AnkerCharger |
| GamingLaptop | ROGZephyrus |
| VerifiedReview | Review001, Review002 |

## Loading in Protege

1. Open Protege 5.6 Desktop
2. File → Open → select ecommerce_simple.owl
3. Reasoner → HermiT 1.4 → Start Reasoner
4. Go to DL Query tab, tick Instances, run queries above

## License

MIT
