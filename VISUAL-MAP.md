graph TD
    %% Styles
    classDef governance fill:#f9f,stroke:#333,stroke-width:4px,color:black;
    classDef defense fill:#f00,stroke:#333,stroke-width:2px,color:white;
    classDef creative fill:#0ff,stroke:#333,stroke-width:2px,color:black;
    classDef education fill:#ff9,stroke:#333,stroke-width:2px,color:black;
    classDef commerce fill:#0f0,stroke:#333,stroke-width:4px,color:black;
    classDef archive fill:#ccc,stroke:#333,stroke-width:1px,color:#666;

    %% CLUSTER 1: CORE GOVERNANCE
    subgraph GOVERNANCE [1. CORE GOVERNANCE]
        OMEGA(OMEGA / Root Ontology)
        STARSHIP(Starship / Operations)
        FED(Federation / Protocols)
        LIB(Academy Hub / Library Index)
        MEM(Psi-Omega Memory)
    end
    class OMEGA,STARSHIP,FED,LIB,MEM governance;

    %% CLUSTER 2: DEFENSE
    subgraph DEFENSE [2. SECURITY & DEFENSE]
        HWF(HackerWatch-Fortress)
        SOCKS(Socks / Stock Watcher)
    end
    class HWF,SOCKS defense;

    %% CLUSTER 3: MUSIC
    subgraph MUSIC [3. MUSIC PRODUCTION]
        KOZMIC(Kozmic Master Console)
        PORT(Portable Studio)
    end
    class KOZMIC,PORT creative;

    %% CLUSTER 4: ENTERTAINMENT
    subgraph ENT [4. KOZMIC ENTERTAINMENT]
        COMEDY(AI Comedy Lounge)
        JOKE(Jokebox)
        KASINO(Kozmic Kasino / NFT)
        PLAY(Kozmic Playland)
    end
    class COMEDY,JOKE,KASINO,PLAY creative;

    %% CLUSTER 5: BOOKS
    subgraph BOOKS [5. BOOKS & LIT]
        LITTLEX(Little X Series Books 1-7)
    end
    class LITTLEX education;

    %% CLUSTER 6: KIDS MUSIC
    subgraph KIDS_MUSIC [6. KIDS MUSIC ED]
        MAGIC(Magic Chalkboard / Composer)
    end
    class MAGIC education;

    %% CLUSTER 7: COMMERCE
    subgraph STORE [7. COMMERCE]
        GMSRFC(GMSRFC / Main Storefront)
    end
    class GMSRFC commerce;

    %% ARCHIVE
    subgraph ARCHIVE_BIN [ARCHIVE]
        OLD_HW(Old HackerWatch)
        OLD_STUDIO(Old Master Studio)
        CORDA(Corda Fork)
    end
    class OLD_HW,OLD_STUDIO,CORDA archive;

    %% RELATIONS
    OMEGA -->|Governs| DEFENSE
    OMEGA -->|Governs| MUSIC
    OMEGA -->|Governs| ENT
    OMEGA -->|Governs| BOOKS
    OMEGA -->|Governs| STORE

    %% Product Flows
    MUSIC -->|Products| GMSRFC
    ENT -->|Tickets/NFTs| GMSRFC
    BOOKS -->|Book Bundles| GMSRFC
    KIDS_MUSIC -->|Apps| GMSRFC
    DEFENSE -->|Subscriptions| GMSRFC

    %% Internal Cluster Flows
    COMEDY --> JOKE
    JOKE --> KASINO
