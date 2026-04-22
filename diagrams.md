# Red Cow Campaign - Mermaid Diagrams

> Reference diagrams for the complete campaign story and character connections.

## Campaign Timeline (1618-1625)

```mermaid
timeline
    title Hero Wars Timeline: Red Cow Clan
    1618 Sea Season: The Missing begins :: Telmori raid steads :: Kidnapped children
    1618 Fire Season: Cattle raids begin :: Emerald Sword conflict
    1619: The Crimson Bat comes :: Demon arrives Sartar
    1620: Tension rises :: Lunar tightening grip
    1621 Storm Season: Orlanth is Dead :: Great Winter begins
    1622: Star collapse :: Tribe nearly destroyed
    1623 Spring: The Rising of Culbrea :: Two-Pine attacks
    1623 Summer: Tribal council :: Black Arrow sent
    1624: The Eleven Lights :: Heroquest begins
    1625: Liberation of Jonstown :: Battle of Dangerford
```

## Character & Faction Relationships

```mermaid
graph TD
    subgraph Red Cow Faction
        BC[Broddi Strong-Kin<br/>Chieftain] -->|leads| EH[Eye of Hurricane]
        DL[Darna Longcoat<br/>Ring Member] -->|leads| CS[Conquering Storm]
        KB[Kangharl Black-Brow<br/>Warrior] -->|member| CS
        EK[Erlana Earth-Keeper<br/>Healer] -->|member| EH
    end

    subgraph Enemies
        JS[Jogar Sog<br/>Telmori Chief] -->|commands| TM[Telmori Wolves]
        BR[Brangbane<br/>Ghoul King] -->|commands| GH[Ghoul Army]
        EC[Lunar Empire] -->|rules| JG[Jomes Hostralos<br/>General]
    end

    subgraph Allies
        QI[Queen Ivartha<br/>Cinsina Queen] -->|commands| WS[Wolfskinners]
        KS[Kallyr Starbrow<br/>Rebel Leader] -->|leads| FS[Free Sartar]
    end

    subgraph PCs
        TS[Thorvald Storm-Speaker] -->|member| CS
        RT[Rok Thunder-Mouth] -->|member| WS
        AS[Asvith Silver-Step] -->|member| WS
        AS -->|secretly| FS
        KB2[Kara Silent-Blade] -->|member| EH
    end

    %% Relationships
    TS -.->|oath| DL[Dead brother]
    RT -.->|hate| JS[Telmori killed family]
    AS -.->|hides| BT[Boldk Red-Turner<br/>Father's killer]
    KB2 -.->|investigates| HusbandDeath

    %% Alliances
    JG -->|fights| TM
    QI -->|allies| JG
    WS -.->|allies| JG
    QI -.->|distrusts| KS
```

## PC Connections to Key NPCs

```mermaid
graph TD
    subgraph Thorvald Storm-Speaker
        T1["Broddi Strong-Kin<br/>Liege Lord"]
        T2["Darna Longcoat<br/>Political Ally"]
        T3["Jomes Hostralos<br/>Bitter Enemy"]
    end

    subgraph Erlana Earth-Keeper
        E1["Broddi Strong-Kin<br/>Wary Patron"]
        E2["Mother Griselda<br/>Temple Superior"]
        E3["Bolik Red-Turner<br/>Half-Brother"]
    end

    subgraph Rok Thunder-Mouth
        R1["Jomes Hostralos<br/>Grudging Ally"]
        R2["Frekor Deep-Woods<br/>War-Brother"]
        R3["Jogar Sog<br/>Mortal Enemy"]
    end

    subgraph Asvith Silver-Step
        A1["Jomes Hostralos<br/>表面 Liege"]
        A2["Kallyr Starbrow<br/>True Loyalty"]
        A3["Bolik Red-Turner<br/>Blood Enemy"]
    end

    subgraph Kara Silent-Blade
        K1["Broddi Strong-Kin<br/>Wary Patron"]
        K2["Kangharl Black-Brow<br/>Suspicious"]
        K3["Humakt Priests<br/>Teachers"]
```

## Story Flow - Year by Year

```mermaid
flowchart LR
    subgraph 1618
        A1[The Missing] --> A2[Telmori Raid]
        A2 --> A3[Kidnapped Children]
    end

    subgraph 1619
        B1[Bat Arrives] --> B2[Demon Attacks]
        B2 --> B3[Chaos Spreads]
    end

    subgraph 1620-1621
        C1[Orlanth Dead] --> C2[Great Winter]
        C2 --> C3[Star Collapse]
    end

    subgraph 1622
        D1[Winter Ends] --> D2[Crisis Aftermath]
    end

    subgraph 1623
        E1[Culbrea Rising] --> E2[Two-Pine War]
        E2 --> E3[Tribal Council]
    end

    subgraph 1624
        F1[Eleven Lights] --> F2[Heroquest]
        F2 --> F3[Quest Complete]
    end

    subgraph 1625
        G1[Liberation] --> G2[Dangerford Battle]
        G2 --> G3[Freedom]
    end

    A3 -->|sets up| B1
    B3 -->|leads to| C1
    C3 -->|causes| D1
    D2 -->|leads to| E1
    E3 -->|leads to| F1
    F3 -->|culminates| G1
```

## Location Map - Red Cow Lands

```mermaid
flowchart TD
    subgraph Red Cow Territory
        RCF[Red Cow Fort] -->|along Heort Creek| EC[Eastern Steads]
        RCF -->|along Danda Creek| WC[Western Steads]
    end

    subgraph Neighbors
        EC -->|across Heort| ST[Stagrance]
        ST -->|east| TW[Telmori Wilds]
        WC -->|north| ES[Emerald Sword<br/>Dinacoli]
        WC -->|west| DOL[Dolutha]
        RCF -->|south| TB[Two-Pine<br/>Culbrea]
    end

    subgraph Important Places
        RCF -->|center| JF[Jonstown<br/>Tribal City]
        TW -->|deep in| WO[Woods of Dead]
        JF -->|road| PR[Pavis Way]
    end

    style RCF fill:#8b0000,color:#fff
    style TW fill:#333,color:#fff
    style WO fill:#444,color:#fff
    style JF fill:#006400,color:#fff
```

## Faction Influence Map

```mermaid
graph TD
    subgraph Power Dynamics
        FS[Free Sartar] -->|wants| LR[Lunar Resistance]
        FS -->|opposes| EC[Lunar Empire]

        EH[Eye of Hurricane] -->|wants| PP[Peace & Prosperity]
        EH -->|opposes| FS

        CS[Conquering Storm] -->|wants| OW[Old Wars]
        CS -->|hates| ES[Emerald Sword]
        CS -->|hates| TB[Two-Pine]

        WS[Wolfskinners] -->|supports| JG[Jomes]
        WS -->|hates| TM[Telmori]

        MW[Moon Winds] -->|supports| EC
        MW -->|wants| CL[Conversion]
    end

    FS ---|competes| EH
    EH ---|competes| CS
    WS ---|allies| JG
    MW ---|allies| EC
```

## Combat Resolution Flow

```mermaid
flowchart TD
    Start[Combat Begins] --> Declare[Declare Combatants]
    Declare --> Roll[Roll Both Dice]
    Roll --> Compare[Compare Results]

    Compare -->|Char 20| CV[Critical Victory]
    Compare -->|Char 11-19 & Resist < 11| V[Victory]
    Compare -->|Both 11-19| M[Mixed]
    Compare -->|Char 1-10 & Resist 11+| D[Defeat]
    Compare -->|Char 1| CD[Complete Defeat]

    CV --> FullDmg[Full Damage to Enemy]
    V --> HalfDmg[Half Damage]
    M --> Exch[Exchange Position]
    D --> Half2[Take Half Damage]
    CD --> Full2[Full Damage to You]

    FullDmg --> VictoryEnd[Enemy Defeated]
    HalfDmg --> Continue[Combat Continues]
    Exch --> Continue
    Half2 --> Continue
    Full2 --> YouDied[You Fall]
```

## QuestWorlds Dice Results

```mermaid
stateDiagram-v2
    [*] --> Rolling
    Rolling --> Critical: 20 on char die
    Rolling --> Success: 11-19
    Rolling --> Failure: 1-10
    Rolling --> Fumble: 1 on char die

    Critical --> [*]
    Success --> SuccessVsFail: R < 11
    Success --> SuccessVsSucc: R 11-19
    Failure --> FailVsSucc: R 11+
    Failure --> FailVsFail: R < 11

    state SuccessVsFail {
        [*] --> Victory
    }
    state SuccessVsSucc {
        [*] --> Mixed
    }
    state FailVsSucc {
        [*] --> Mixed
    }
    state FailVsFail {
        [*] --> Defeat
    }
```

## Resource Tracking

```mermaid
erDiagram
    RED_COW_CLAN ||--o{ WEALTH : has
    RED_COW_CLAN ||--o{ WARRIORS : TRAINED
    RED_COW_CLAN ||--o{ MAGIC : TEMPLE
    RED_COW_CLAN ||--o{ REPUTATION : CLAN_STANDING
    RED_COW_CLAN ||--o{ ALLIES : FRIEND_CLANS

    WEALTH {
        int cattle
        int grain
        int treasure
    }
    WARRIORS {
        int thanes
        int carls
        int housecarls
    }
    MAGIC {
        int priests
        int shrines
        int artifacts
    }
    REPUTATION {
        int honor
        int fear
    }
```

## Key Plot Points Summary

```mermaid
mindmap
  (The Coming Storm)
    1618
      The Missing
      Telmori Raids
      Faction Tensions
    1619
      Crimson Bat
      Demon Attack
      Chaos Spreads
    1620
      Lunar Tightens
      Tensions Rise
    1621-1622
      Orlanth Dead
      Great Winter
      Star Collapse
    1623
      Culbrea Rising
      Two-Pine War
      Tribal Council
    1624
      Eleven Lights
      Heroquest
      Underworld Quest
    1625
      Liberation
      Dangerford
      Freedom
```

## Notes for Implementation

- **Year tracking**: Global variable $year (1618-1625)
- **Season tracking**: Sea/Fire/Earth/Dark/Storm
- **Resource decay**: Background events each season
- **Faction influence**: Player actions affect faction standing
- **Character arcs**: Each PC has year-specific story beats
- **Multiple endings**: Based on PC choices and faction alignment