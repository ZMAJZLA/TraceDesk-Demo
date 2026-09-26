# TraceDesk

**A dynamic, Omni-Industry operations and ticketing system engineered by The Karter Group Technologies.**

TraceDesk is a lightweight, high-performance Application designed to replace legacy, industry-specific management software. By utilising a Dynamic Dictionary Engine, the platform instantly re-wires its vocabulary, checklists, and workflows to adapt to any physical service business—from IT repair shops to bakeries and tattoo studios.

---

##  Core Architecture

*   **Frontend:** Pure HTML5, CSS3, and Vanilla JavaScript (No heavy frameworks, ensuring sub-second load times).
*   **State Management:** Client-side `localStorage` (V9 Prototype Phase) -> Migrating to PostgreSQL (Supabase) for production.
*   **Print Engine:** Custom `@media print` CSS API targeting both standard A4 (Invoices) and Thermal Printers (Asset Tags).
*   **Barcode Generation:** `JsBarcode` (Code128 Format).
*   **Hosting Deployment:** Cloudflare Pages (Global CDN).

---

##  Features

### 1. Dynamic Industry Dictionaries
TraceDesk is vertical-agnostic. Upon initialization, the system injects custom lexicons based on the selected industry:
*   **IT Repair:** "Asset", "Device PIN", "Pre-Repair Condition".
*   **Automotive:** "Vehicle Registration", "Mileage", "Locking Nut".
*   **Bakery:** "Cake Size", "Allergens", "Delivery Date".

### 2. Dual-Output Print Engine
Removes the need for third-party PDF generators. The UI leverages the browser's native print API to generate two distinct physical documents:
*   **The Workshop Tag:** A high-contrast, thermal-printer-ready label featuring a scannable Code128 barcode and the technician's pre-flight checklist.
*   **The Customer Invoice:** A cleanly formatted A4 receipt/invoice detailing the billing breakdown and legal terms.

### 3. Live Operations Board
A tactile, drag-and-drop Kanban interface allowing staff to move assets seamlessly from *Intake* to *In Progress* to *Ready for Collection*.

### 4. Automated Customer CRM
When a new ticket is generated, the system automatically parses the client's contact information and builds a persistent profile in the Customer Database, tracking total lifetime tickets.
