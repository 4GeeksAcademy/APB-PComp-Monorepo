# TrackFlow Business Context

This document records shared company and domain context for the TrackFlow project. Business facts below come from `BRIEFING.md`; proposed solutions are not treated as approved scope.

## Company and Business

TrackFlow is a third-party logistics (3PL) company serving e-commerce brands. It stores client inventory, prepares and packs orders, coordinates delivery through carrier networks, and handles returns.

The detailed company briefing describes operations in the United States and Spain, with warehouses in Los Angeles and Zaragoza. It reports approximately 130 employees, annual revenue of about EUR 9 million, and eight carriers across both markets. These figures are approximate and come from the briefing.

TrackFlow serves two customer groups:

- **B2B:** e-commerce brands that contract TrackFlow's logistics services.
- **B2C:** consumers who receive shipments sent through TrackFlow.

## Operating Model

The business flow described in the briefing is: a brand submits an order; TrackFlow stores the inventory, picks and packs the order, hands it to a carrier, and manages delivery tracking and any return. Orders currently arrive by email in varying formats. The exact data contract and system interfaces are not documented here.

The company operates across these areas: warehouse operations, last-mile delivery and carrier management, reverse logistics, customer experience, commercial and client relations, people, technology, and executive management.

## Current Operating Landscape

- The Los Angeles and Zaragoza warehouses use different warehouse-management arrangements: one uses commercial software and the other an advanced spreadsheet. They do not share global inventory visibility.
- Order intake, carrier assignment and tracking, returns review, customer inquiries, and executive reporting involve substantial manual work.
- TrackFlow works with eight carriers. Carrier performance data is not maintained in a structured historical form, according to the briefing.
- Returns represent approximately 18-25% of volume, depending on client and country; decisions currently receive human review.
- Customer support serves both brands and end consumers through email, WhatsApp, and phone. The briefing describes agents consulting a Word document in Google Drive; it does not identify a unified ticketing or knowledge system.
- The technical landscape includes a legacy ERP from the early 2010s, undocumented integrations, point-to-point Python scripts, and databases across two cloud providers. These are descriptions of existing systems, not chosen target architecture.
- Executive reporting is assembled manually and may contain data one or two days old.

## Domain Terms

- **Warehouse / WMS:** a physical warehouse and the system or process used to manage its inventory and fulfillment.
- **SKU:** a stock-keeping unit used to identify a product or inventory item.
- **Carrier:** a company that transports a shipment to its destination.
- **Shipment tracking:** status information about a shipment while it moves through delivery.
- **Reverse logistics / return:** the process of handling a product after it is sent back.
- **B2B / B2C:** services for business clients / interactions with end consumers.

## Open Items and Source Caveats

- The detailed briefing describes the markets as the United States and Spain. The previous Spanish context placeholder said Mexico and Spain. This document follows the detailed briefing; confirm the correct markets before treating the discrepancy as resolved.
- Leadership names conflict across the source documents: the briefing names Thomas Harry in its company overview and Thomas Espinoza in its executive section; the previous `CONTEXT.md` also referred to Daniel Espinoza. The attribution for creating TrackFlow Tech also varies. Do not assume a canonical CEO or unit founder until confirmed.
- The briefing describes 24/7 availability as a desired property for some services, but provides no formal service-level agreement.
- Spanish and English support is described as optional or recommended for some departments. No default project language is established.
- No target technology stack, API contract, business-rule catalog, or project-specific implementation scope is established by this company context.
