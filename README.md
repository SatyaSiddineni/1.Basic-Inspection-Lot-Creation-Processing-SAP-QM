**Basic Inspection Lot Creation & Processing – SAP QM**

This project demonstrates the complete end‑to‑end process of Inspection Lot Creation and Processing in SAP Quality Management (QM). It covers master data setup, procurement integration, inspection execution, results recording, and usage decision — forming the foundation of any QM implementation.


✅ 1. Project Overview
This repository provides a practical, step‑by‑step demonstration of how an organization performs incoming inspection (Inspection Type 01) for procured materials. It includes:

        Master data preparation
        Purchase order creation
        Goods receipt triggering inspection lot
        Inspection lot processing
        Results recording
        Usage decision and stock posting

This scenario is widely used in manufacturing, pharmaceuticals, automotive, FMCG, and other industries where material quality is critical.


✅ 2. Business Scenario
A company procures raw materials from a vendor. Upon receiving the material, the system must:

        Automatically create an Inspection Lot
        Allow the Quality team to perform results recording
        Enable the Quality Manager to take a Usage Decision (UD)
        Post the material to Unrestricted, Blocked, or Scrap based on quality results
        This ensures that only quality‑approved materials enter the production process.


✅ 3. Process Flow Diagram
Code
                ┌────────────────────────┐
                │   Material Master Set   │
                │   Up with QM View       │
                └───────────┬────────────┘
                            │
                            ▼
                ┌────────────────────────┐
                │   Create Purchase Order │
                │        (ME21N)          │
                └───────────┬────────────┘
                            │
                            ▼
                ┌────────────────────────┐
                │   Goods Receipt (MIGO)  │
                │  Inspection Lot Created │
                └───────────┬────────────┘
                            │
                            ▼
                ┌────────────────────────┐
                │   Inspection Lot Review │
                │        (QA32)           │
                └───────────┬────────────┘
                            │
                            ▼
                ┌────────────────────────┐
                │   Results Recording     │
                │        (QE51N)          │
                └───────────┬────────────┘
                            │
                            ▼
                ┌────────────────────────┐
                │     Usage Decision      │
                │        (QA11)           │
                └───────────┬────────────┘
                            │
                            ▼
                ┌────────────────────────┐
                │ Stock Posting (Unres/   │
                │ Blocked/Accepted Stock) │
                └────────────────────────┘


✅ 4. T‑Codes Used in This Project

✅ 5. Folder Structure
Code
        📁 Basic-Inspection-Lot-Creation-Processing-SAP-QM
        │
        ├── 📁 01_Master_Data
        ├── 📁 02_Process_Flow
        ├── 📁 03_Inspection_Lot_Creation
        ├── 📁 04_Results_Recording
        ├── 📁 05_Usage_Decision
        ├── 📁 06_Test_Data
        └── README.md


✅ 6. Key Learnings

        How SAP QM integrates with MM during procurement
        How inspection lots are automatically created during GR
        How to perform results recording for quantitative & qualitative MICs
        How to take a usage decision and post stock accordingly
        Understanding of master data dependencies (MICs, Sampling, Plans)
        Real‑world relevance of incoming inspection processes

