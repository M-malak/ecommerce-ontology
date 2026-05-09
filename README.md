---

# E-Commerce Product Ontology (OWL 2 DL)

A production-quality OWL 2 DL ontology modelling an online shopping platform domain.

## Overview

| Metric | Value |
|---|---|
| OWL Profile | OWL 2 DL |
| Serialisation | RDF/XML |
| Reasoner tested | HermiT 1.4 |
| Named classes | 25 |
| Object properties | 9 |
| Data properties | 13 |
| Named individuals | 28 |
| Restrictions | 8 |
| Property chains | 1 |

## OWL 2 DL Features Demonstrated

**Class axioms:** equivalentClass, subClassOf, intersectionOf, unionOf, AllDisjointClasses

**Restrictions:** someValuesFrom, hasValue, minQualifiedCardinality, qualifiedCardinality

**Property characteristics:** Functional, Transitive, Asymmetric, Irreflexive, inverseOf, propertyChainAxiom

**OWL 2 only:** AllDifferent, datatype facets (minInclusive, maxExclusive)

## Domain Coverage

Product taxonomy: Electronics (Laptop, Smartphone, Headphones, SmartWatch) + Accessories (Charger, Case, Cable)

Defined classes (auto-classified by reasoner): PremiumProduct, BudgetProduct, DiscountedProduct, HighRatedProduct, GamingLaptop, GamerCustomer, FrequentBuyer, LoyalCustomer, VerifiedReview

Entities: 5 brands, 6 products, 4 customers, 4 orders, 2 reviews, 4 payment methods

## Property Chain

purchases o manufacturedBy → prefersBrand — Customer brand preference inferred from purchase history

## Loading in Protege

1. Open Protege 5.6 Desktop
2. File → Open → select ecommerce_simple.owl
3. Reasoner → HermiT 1.4 → Start Reasoner
4. DL Query examples:
   - LoyalCustomer → Ali Hassan, Riya Sharma
   - PremiumProduct → MacBookPro, iPhone15Pro, ROGZephyrus
   - FrequentBuyer → Ali Hassan, Lena Mueller, Riya Sharma
   - DiscountedProduct → GalaxyS24Ultra, SonyHeadphones, AnkerCharger
   - VerifiedReview → Review001, Review002

## License

MIT
