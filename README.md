# E-Commerce Product Ontology (OWL 2 DL)

A production-quality OWL 2 DL ontology modelling an online shopping platform domain.

## Overview

| Metric | Value |
|---|---|
| OWL Profile | OWL 2 DL |
| Serialisation | RDF/XML |
| Reasoner tested | HermiT 1.4, Pellet 2.x |
| Named classes | 40 |
| Object properties | 23 |
| Data properties | 26 |
| Named individuals | 53 |
| Restrictions | 23 |
| Property chains | 3 |

## OWL 2 DL Features Demonstrated

All 40 major OWL 2 DL constructs are present with domain-justified semantics:

**Class axioms:** `equivalentClass`, `subClassOf`, `intersectionOf`, `unionOf`, `complementOf`, `oneOf`, `disjointUnionOf`, `AllDisjointClasses`, `disjointWith`

**Restrictions:** `someValuesFrom`, `allValuesFrom`, `hasValue`, `minQualifiedCardinality`, `maxQualifiedCardinality`, `qualifiedCardinality`, `minCardinality`

**Property characteristics:** Functional, InverseFunctional, Transitive, Symmetric, Asymmetric, Reflexive, Irreflexive, `inverseOf`

**Property structure:** `subPropertyOf` (object + data), property chain axioms (3 chains)

**OWL 2 only:** `hasKey`, `NegativePropertyAssertion`, `disjointUnionOf`, DataOneOf, `AllDifferent`, `differentFrom`, `sameAs`

**Annotations:** Dublin Core, SKOS (definition, note, example), custom annotation properties, `owl:deprecated`, `rdfs:seeAlso`, `owl:versionIRI`

## Domain Coverage

- **Product taxonomy:** Electronics (Laptop, Smartphone, Tablet, Headphones, SmartWatch) + Accessories (Cable, Charger, Case)
- **Defined classes (auto-classified by reasoner):** PremiumProduct (≥$1000), BudgetProduct (<$300), MidRangeProduct ($300–999), GamingLaptop, GamerCustomer, FrequentBuyer, LoyalCustomer, HighRatedProduct, DiscountedProduct, VerifiedReview, NonPremiumProduct, UnverifiedReview, AppleExclusiveProduct, DigitalPaymentOrder, SingleProductOrder, MultiProductOrder, PlatformBrand, PlatformSeller
- **Entities:** 5 brands, 13 categories, 10 products, 5 customers, 2 sellers, 5 payment methods, 6 orders, 6 reviews

## Property Chains

| Chain | Semantics |
|---|---|
| `purchases ∘ manufacturedBy → prefersBrand` | Customer's brand preference inferred from purchase history |
| `placesOrder ∘ containsProduct → indirectlyPurchases` | Bridges order-level and product-level purchase records |
| `writesReview ∘ reviewsProduct → hasReviewedProduct` | Directly links customer to reviewed products |

## Loading in Protégé

1. Open Protégé 5.6 Desktop
2. File → Open → select `ecommerce.owl`
3. Reasoner → HermiT 1.4 → Start Reasoner
4. DL Query examples:
   - `ec:LoyalCustomer` → returns Customer_Ali, Customer_Riya
   - `ec:PremiumProduct` → returns MacBookPro, iPhone15Pro, ROGZephyrus, iPadPro
   - `ec:SingleProductOrder` → returns Order005
   - `ec:FrequentBuyer` → returns Customer_Ali, Customer_Lena, Customer_Riya

## Author

Mohd Khan  
University of Campania Luigi Vanvitelli  
MIRAMARE EU Project

## License

MIT
