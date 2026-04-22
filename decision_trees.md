# Red Cow Campaign - Decision Trees & Story Flows

Comprehensive Mermaid diagrams tracking all story branches and decision points in the campaign.

## Character Selection Flow

```mermaid
flowchart TD
    Start(["Start Campaign"]) --> Choose["Choose Your Hero"]
    
    Choose --> T[Thorvald<br/>Storm-Speaker]
    Choose --> E[Erlana<br/>Earth-Keeper]
    Choose --> R[Rok<br/>Thunder-Mouth]
    Choose --> A[Asvith<br/>Silver-Step]
    Choose --> K[Kara<br/>Silent-Blade]
    
    T --> Desc1["Housecarl<br/>Liege: Broddi<br/>Enemy: Lunars<br/>Flaw: Oath-Breaker Hunt"]
    E --> Desc2["Priestess<br/>Father: Lunar convert<br/>Shame: Bloodline<br/>Flaw: Forbidden Knowledge"]
    R --> Desc3["Berserker<br/>Family: Slain by Telmori<br/>Enemy: Jogar Sog<br/>Flaw: Red Rage"]
    A --> Desc4["Scout<br/>True Loyalty: Kallyr<br/>Secret: Rebel spy<br/>Flaw: Blood Debt"]
    K --> Desc5["Sword Maiden<br/>Husband: Murdered<br/>Investigation: Truth<br/>Flaw: Cannot Lie"]
    
    Desc1 --> Begin[Begin Campaign]
    Desc2 --> Begin
    Desc3 --> Begin
    Desc4 --> Begin
    Desc5 --> Begin
```

## 1618 - Year One Decision Tree

```mermaid
flowchart TD
    Start1618["1618 Opening"] --> Moot[Moot<br/>Political] & Patrol[Border Patrol<br/>Action] & Temple[Temple Visit<br/>Story]
    
    Moot --> Roll1{Oratory Roll}
    Roll1 -->|"Great"| InfluenceG[Conquering Storm<br/>Gains Influence]
    Roll1 -->|"Success"| MootWords[Words considered]
    Roll1 -->|"Fail"| MootFail[Council divided]
    
    Patrol --> Roll2{Awareness Roll}
    Roll2 -->|"Great"| Spot[Spot Telmori patrol]
    Roll2 -->|"Success"| Peaceful[Ride peaceful]
    Roll2 -->|"Fail"| Ambush[Nearly ambushed]
    
    Temple --> Roll3{Faith Roll}
    Roll3 -->|"Great"| Bless[Divine blessing]
    Roll3 -->|"Success"| Rest[Temple peace]
    Roll3 -->|"Fail"| Empty[Temple emptying]
    
    InfluenceG --> Crisis[First Crisis]
    MootWords --> Crisis
    MootFail --> Crisis
    Spot --> Crisis
    Peaceful --> Crisis
    Ambush --> Crisis
    Bless --> Crisis
    Rest --> Crisis
    Empty --> Crisis
    
    Crisis --> Runner["Children taken!<br/>Wolves in night"]
    
    Runner --> Chase[Pursue kidnappers<br/>Combat] & Heal[Tend wounded<br/>Healing] & Trail[Investigate<br/>Scouting]
    
    Chase --> RollC{Combat Roll}
    RollC -->|"Victory"| Rescue[Children rescued]
    RollC -->|"Mixed"| Gone[Taken to Stagland]
    RollC -->|"Defeat"| EmptyReturn[Return empty]
    
    Heal --> RollH{Healing Roll}
    RollH -->|"Great"| Saves[Lives saved]
    RollH -->|"Success"| SomeLive[Some survive]
    RollH -->|"Fail"| TwoDie[Two die]
    
    Trail --> RollT{Tracking Roll}
    RollT -->|"Great"| LearnLoc[Learn hiding place]
    RollT -->|"Success"| TrailEast[Trail leads east]
    RollT -->|"Fail"| Confused[Signs confuse]
    
    Rescue --> 1619[1619 Season]
    Gone --> 1619
    EmptyReturn --> 1619
    Saves --> 1619
    SomeLive --> 1619
    TwoDie --> 1619
    LearnLoc --> 1619
    TrailEast --> 1619
    Confused --> 1619
```

## Faction Influence Tree

```mermaid
flowchart LR
    subgraph Factions
        FS[Free Sartar] -->|"wants"| LR[Lunar Resistance]
        FS -->|"opposes"| EC[Lunar Empire]
        
        EH[Eye of Hurricane] -->|"wants"| PP[Peace & Prosperity]
        EH -->|"opposes"| FS
        
        CS[Conquering Storm] -->|"wants"| OW[Old Wars]
        CS -->|"hates"| ES[Emerald Sword]
        CS -->|"hates"| TB[Two-Pine]
        
        WS[Wolfskinners] -->|"supports"| JG[Jomes Hostralos]
        WS -->|"hates"| TM[Telmori]
        
        MW[Moon Winds] -->|"supports"| EC
        MW -->|"wants"| CL[Conversion]
    end
    
    FS == "competes" ==> EH
    EH == "competes" ==> CS
    WS == "allies" ==> JG
    MW == "allies" ==> EC
```

## Campaign Timeline Decision Points

```mermaid
timeline
    title Red Cow Campaign - Key Decision Years
    1618 Sea Season
      : Character Selection
      : Moot vs Patrol vs Temple
      : Missing begins
      : Chase vs Heal vs Trail
    1619 Fire Season
      : Cattle raids escalate
      : Emerald Sword conflict
      : The Crimson Bat arrives
    1619-1620
      : Demon attacks Sartar
      : Chaos spreads
    1620
      : Lunar tightening grip
      : Tensions rise
    1621 Storm Season
      : Orlanth is Dead declared
      : Great Winter begins
    1622
      : Star collapse
      : Tribe nearly destroyed
    1623 Spring
      : Culbrea Rising
      : Two-Pine attacks
      : Tribal council decisions
    1623 Summer
      : Black Arrow sent
      : Faction alignment critical
    1624
      : The Eleven Lights
      : Heroquest begins
      : Underworld journey
    1625
      : Liberation of Jonstown
      : Battle of Dangerford
      : Freedom or defeat
```

## NPC Relationship Web

```mermaid
graph TD
    subgraph Red_Cow_Inner
        BC[Broddi Strong-Kin<br/>Chieftain] -->|"leads"| EH[Eye of Hurricane]
        DL[Darna Longcoat<br/>Ring Member] -->|"leads"| CS[Conquering Storm]
        KB[Kangharl Black-Brow<br/>Warrior] -->|"member"| CS
        EK[Erlana Earth-Keeper<br/>Healer] -->|"member"| EH
    end
    
    subgraph Enemies
        JS[Jogar Sog<br/>Telmori Chief] -->|"commands"| TM[Telmori Wolves]
        BR[Brangbane<br/>Ghoul King] -->|"commands"| GH[Ghoul Army]
        LE[Lunar Empire] -->|"rules"| JH[Jomes Hostralos<br/>General]
    end
    
    subgraph Allies
        QI[Queen Ivartha<br/>Cinsina Queen] -->|"commands"| WS[Wolfskinners]
        KS[Kallyr Starbrow<br/>Rebel Leader] -->|"leads"| FS[Free Sartar]
    end
    
    subgraph PCs
        TS[Thorvald Storm-Speaker] -->|"member"| CS
        RT[Rok Thunder-Mouth] -->|"member"| WS
        AS[Asvith Silver-Step] -->|"member"| WS
        AS -.-|"secretly"| FS
        KB2[Kara Silent-Blade] -->|"member"| EH
    end
    
    TS -.->|"oath"| DL
    RT -.->|"hate"| JS
    AS -.->|"hides"| BT[Boldk Red-Turner]
    KB2 -.->|"investigates"| HusbandDeath
    
    JH -->|"fights"| TM
    QI -->|"allies"| JH
    WS -.->|"allies"| JH
    QI -.->|"distrusts"| KS
```

## Location Navigation Map

```mermaid
flowchart TD
    subgraph Territory
        RCF[Red Cow Fort] -->|"along Heort Creek"| EC[Eastern Steads]
        RCF -->|"along Danda Creek"| WC[Western Steads]
    end
    
    subgraph Neighbors
        EC -->|"across Heort"| ST[Stagrance]
        ST -->|"east"| TW[Telmori Wilds]
        WC -->|"north"| ES[Emerald Sword<br/>Dinacoli]
        WC -->|"west"| DOL[Dolutha]
        RCF -->|"south"| TB[Two-Pine<br/>Culbrea]
    end
    
    subgraph Quest_Locations
        RCF -->|"center"| JF[Jonstown<br/>Tribal City]
        TW -->|"deep in"| WO[Woods of Dead]
        JF -->|"road"| PR[Pavis Way]
        JF -->|"north"| JH[Jomes Lands]
        WO -->|"contains"| BH[Brangbane's Hall]
    end
    
    style RCF fill:#8b0000,color:#fff
    style TW fill:#333,color:#fff
    style WO fill:#444,color:#fff
    style JF fill:#006400,color:#fff
```

## PC Secret Missions

```mermaid
flowchart TD
    subgraph Thorvald_Arc
        T1[Broddi Strong-Kin<br/>Liege Lord] -->|"oath"| TD[Debt of Honor]
        T2[Jomes Hostralos<br/>Bitter Enemy] -->|"swore"| TV[Oath of Vengeance]
    end
    
    subgraph Erlana_Arc
        E1[Broddi Strong-Kin<br/>Wary Patron] -->|"seeks"| EP[Prove Loyalty]
        E2[Bolik Red-Turner<br/>Half-Brother] -->|"hidden"| EB[Bloodline Secret]
        E3[Father's Legacy] -->|"carries"| EF[Shame/Burden]
    end
    
    subgraph Rok_Arc
        R1[Jogar Sog<br/>Mortal Enemy] -->|"hunts"| RR[Red Revenge]
        R2[Frekor Deep-Woods<br/>War-Brother] -->|"sworn"| RW[Wolf Bond]
    end
    
    subgraph Asvith_Arc
        A1[Jomes Hostralos<br/>表面 Liege] -->|"serves"| AL[表面 Loyalty]
        A2[Kallyr Starbrow<br/>True Loyalty] -->|"secret"| AT[True Allegiance]
        A3[Bolik Red-Turner<br/>Father's Killer] -->|"hides"| AB[Blood Debt]
    end
    
    subgraph Kara_Arc
        K1[Broddi Strong-Kin<br/>Wary Patron]
        K2[Kangharl Black-Brow<br/>Suspicious]
        K3[Humakt Priests<br/>Seek Truth]
        K4[Husband's Killer] -->|"investigate"| KI[Find Killer]
    end
```

## QuestWorlds Combat System Flow

```mermaid
flowchart TD
    Start[Combat Begins] --> Declare[Declare Combatants]
    Declare --> Roll[Roll Both Dice]
    Roll --> Compare[Compare Results]
    
    Compare -->|"Char = 20"| CV[Critical Victory]
    Compare -->|"Char 11-19 & Resist < 11"| V[Victory]
    Compare -->|"Char 11-19 & Resist 11+"| M[Mixed]
    Compare -->|"Char 1-10 & Resist 11+"| D[Defeat]
    Compare -->|"Char = 1"| CD[Complete Defeat]
    
    CV --> FullDmg[Full Damage to Enemy]
    V --> HalfDmg[Half Damage to Enemy]
    M --> Exch[Exchange Position]
    D --> Half2[Take Half Damage]
    CD --> Full2[Full Damage to You]
    
    FullDmg --> VictoryEnd[Enemy Defeated]
    HalfDmg --> Continue[Combat Continues]
    Exch --> Continue
    Half2 --> Continue
    Full2 --> YouDied[You Fall]
```

## QuestWorlds Skill Resolution

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

## Clan Resources System

```mermaid
erDiagram
    RED_COW_CLAN ||--o{ WEALTH : has
    RED_COW_CLAN ||--o{ WARRIORS : trained
    RED_COW_CLAN ||--o{ MAGIC : temple
    RED_COW_CLAN ||--o{ REPUTATION : clan_standing
    RED_COW_CLAN ||--o{ ALLIES : friend_clans
    
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

## Story Progression - Seasonal Flow

```mermaid
flowchart LR
    subgraph Year_1618
        A1[The Missing] --> A2[Telmori Raid]
        A2 --> A3[Kidnapped Children]
    end
    
    subgraph Year_1619
        B1[Bat Arrives] --> B2[Demon Attacks]
        B2 --> B3[Chaos Spreads]
    end
    
    subgraph Year_1620_1621
        C1[Orlanth Dead] --> C2[Great Winter]
        C2 --> C3[Star Collapse]
    end
    
    subgraph Year_1622
        D1[Winter Ends] --> D2[Crisis Aftermath]
    end
    
    subgraph Year_1623
        E1[Culbrea Rising] --> E2[Two-Pine War]
        E2 --> E3[Tribal Council]
    end
    
    subgraph Year_1624
        F1[Eleven Lights] --> F2[Heroquest]
        F2 --> F3[Quest Complete]
    end
    
    subgraph Year_1625
        G1[Liberation] --> G2[Dangerford Battle]
        G2 --> G3[Freedom]
    end
    
    A3 -->|"sets up"| B1
    B3 -->|"leads to"| C1
    C3 -->|"causes"| D1
    D2 -->|"leads to"| E1
    E3 -->|"leads to"| F1
    F3 -->|"culminates"| G1
```

## Interactive Branch Summary

```mermaid
flowchart TB
    subgraph Year_1618_Branches
        B1[Character Select] --> B2[Opening Choice]
        B2 --> B3[Moot/Patrol/Temple]
        B3 --> B4[Crisis Response]
        B4 --> B5[Chase/Heal/Trail]
        B5 --> B6[Year End]
    end
    
    subgraph Player_Choices
        B2 == Political ==> M[Join Moot]
        B2 == Action ==> P[Border Patrol]
        B2 == Story ==> T[Temple Visit]
        
        B4 == Combat ==> C[Pursue Raiders]
        B4 == Healing ==> H[Tend Wounded]
        B4 == Scout ==> S[Track Trail]
    end
    
    subgraph Outcomes
        C --> CR[Rescue/Gone/Fail]
        H --> HS[Saves/Some/Die]
        S --> SL[Locate/East/Confused]
    end
    
    subgraph Impact
        CR -.->|"affects"| RI[Resource Impact]
        HS -.->|"affects"| HI[Healing Impact]
        SL -.->|"affects"| SI[Intel Impact]
    end
    
    RI --> Next[1619 Transition]
    HI --> Next
    SI --> Next
```

---

# Enhancement 1: Conditional Macro System

> Faction-aware macros that change outcomes based on PC choices and faction standing

## Faction-Aware Roll Macro

```mermaid
flowchart TD
    START[<<macro factionRoll>>] --> READY[Read parameters]
    READY --> WHO[Identify PC]
    WHO --> FACT[Determine PC faction]
    
    FACT -->|"Free Sartar"| FS_HIGH{FS Standing<br/>> 15}
    FACT -->|"Eye of Hurricane"| EH_HIGH{EH Standing<br/>> 15}
    FACT -->|"Conquering Storm"| CS_HIGH{CS Standing<br/>> 15}
    FACT -->|"Wolfskinners"| WS_HIGH{WS Standing<br/>> 15}
    FACT -->|"Moon Winds"| MW_HIGH{MW Standing<br/>> 15}
    
    FS_HIGH -->|"Yes"| FS_BONUS[+2 to roll]
    FS_HIGH -->|"No"| CHECK_MOD1
    EH_HIGH -->|"Yes"| EH_BONUS[+2 to roll]
    EH_HIGH -->|"No"| CHECK_MOD2
    CS_HIGH -->|"Yes"| CS_BONUS[+2 to roll]
    CS_HIGH -->|"No"| CHECK_MOD3
    WS_HIGH -->|"Yes"| WS_BONUS[+2 to roll]
    WS_HIGH -->|"No"| CHECK_MOD4
    MW_HIGH -->|"Yes"| MW_BONUS[+2 to roll]
    MW_HIGH -->|"No"| CHECK_MOD5
    
    FS_BONUS --> ROLL[Dice Roll]
    EH_BONUS --> ROLL
    CS_BONUS --> ROLL
    WS_BONUS --> ROLL
    MW_BONUS --> ROLL
    
    CHECK_MOD1 --> ROLL
    CHECK_MOD2 --> ROLL
    CHECK_MOD3 --> ROLL
    CHECK_MOD4 --> ROLL
    CHECK_MOD5 --> ROLL
    
    ROLL --> RESULT[Return result<br/>with modifiers]
```

## Quest Unlock Macro

```mermaid
flowchart TD
    START[<<macro checkQuestUnlock>>] --> CHECK[Check prerequisites]
    
    CHECK --> Q1{Rumors of Jogar Sog<br/>FS >= 10}
    Q1 -->|"Yes"| Q1_UNLOCK[Unlock: Hunt the Wolf-Chief]
    Q1 -->|"No"| Q1_LOCK[Quest hidden]
    
    CHECK --> Q2{Boland Truth<br/>Kara arc >= 3}
    Q2 -->|"Yes"| Q2_UNLOCK[Unlock: Husband's Killer]
    Q2 -->|"No"| Q2_LOCK[Quest hidden]
    
    CHECK --> Q3{Eleven Lights<br/>Year >= 1624}
    Q3 -->|"Yes"| Q3_UNLOCK[Unlock: Heroquest]
    Q3 -->|"No"| Q3_LOCK[Quest hidden]
    
    CHECK --> Q4{ Rebel Alliance<br/>FS + KS >= 25}
    Q4 -->|"Yes"| Q4_UNLOCK[Unlock: Liberation Plot]
    Q4 -->|"No"| Q4_LOCK[Quest hidden]
    
    Q1_UNLOCK --> DONE
    Q2_UNLOCK --> DONE
    Q3_UNLOCK --> DONE
    Q4_UNLOCK --> DONE
```

---

# Enhancement 2: Character Arc Milestones

> Track PC-specific progression through secret revelations and personal goals

## Thorvald Storm-Speaker Arc

```mermaid
flowchart TD
    TS_START[Thorvald Arc] --> TS1[Year 1618: Oath sworn]
    TS1 --> TS2[Year 1619: Jogar Sog location revealed]
    TS2 --> TS3[Year 1622: Opportunity for vengeance]
    TS3 --> TS4[Year 1624: Final hunt]
    TS4 --> TS5{"Confront Jogar"}
    
    TS5 -->|"Victory"| TS_V[Oath fulfilled<br/>Honor restored]
    TS5 -->|"Defeat"| TS_D[Oath unfulfilled<br/>Shame]
    TS5 -->|"Avoid"| TS_A[Let live<br/>Mixed honor]
```

## Erlana Earth-Keeper Arc

```mermaid
flowchart TD
    EK_START[Erlana Arc] --> EK1[Year 1618: Prove loyalty]
    EK1 --> EK2[Year 1620: Father's secrets]
    EK2 --> EK3[Year 1622: Half-brother revealed]
    EK3 --> EK4[Year 1624: Confront truth]
    EK4 --> EK5{"Confront Bolik"}
    
    EK5 -->|"Expose"| EK_E[Exile half-brother<br/>Shame]
    EK5 -->|"Hide"| EK_H[Keep secret<br/>Burden]
    EK5 -->|"Forgive"| EK_F[Reconcile<br/>Healing]
```

## Rok Thunder-Mouth Arc

```mermaid
flowchart TD
    RT_START[Rok Arc] --> RT1[Year 1618: Family lost]
    RT1 --> RT2[Year 1619: Enemy named]
    RT2 --> RT3[Year 1622: Find Jogar]
    RT3 --> RT4[Year 1624: Final battle]
    RT4 --> RT5{"Face Telmori"}
    
    RT5 -->|"Kill"| RT_K[Mortal enemy dead<br/>Peace]
    RT5 -->|"Spare"| RT_S[Lose purpose<br/>Void]
    RT5 -->|"Die"| RT_D[Die in glory<br/>Sacrifice]
```

## Asvith Silver-Step Arc

```mermaid
flowchart TD
    AS_START[Asvith Arc] --> AS1[Year 1618: Serve Jomes]
    AS1 --> AS2[Year 1620: Kallyr contact]
    AS2 --> AS3[Year 1622: Father's killer found]
    AS3 --> AS4[Year 1624: Reckoning]
    AS4 --> AS5{"Face Boldk"}
    
    AS5 -->|"Kill"| AS_K[Avenged<br/>Turn rebel]
    AS5 -->|"Spare"| AS_S[Mercy<br/>Double agent]
    AS5 -->|"Turn"| AS_T[Reveal truth<br/>Allies shift]
```

## Kara Silent-Blade Arc

```mermaid
flowchart TD
    KB_START[Kara Arc] --> KB1[Year 1618: Husband dead]
    KB1 --> KB2[Year 1620: Investigate truth]
    KB2 --> KB3[Year 1622: Suspect named]
    KB3 --> KB4[Year 1624: Evidence gathered]
    KB4 --> KB5{"Reveal truth"}
    
    KB5 -->|"Kill"| KB_K[Execute killer<br/>Justice]
    KB5 -->|"Exile"| KB_E[Banish<br/>Mercy]
    KB5 -->|"Hide"| KB_H[Protect clan<br/>Secret]
```

## Combined Arc Progression

```mermaid
timeline
    title PC Arc Completion Tracking
    1618
      : Thorvald: Oath sworn
      : Erlana: Prove loyalty
      : Rok: Family lost
      : Asvith: Serve Jomes
      : Kara: Husband dead
    1620
      : Thorvald: Trace enemy
      : Erlana: Father's secrets
      : Asvith: Kallyr contact
    1622
      : Thorvald: Hunt opportunity
      : Erlana: Half-brother
      : Rok: Find Jogar
      : Asvith: Boldk found
      : Kara: Suspect named
    1624
      : Thorvald: Final hunt
      : Erlana: Reckoning
      : Rok: Final battle
      : Asvith: Reckoning
      : Kara: Truth revealed
```

---

# Enhancement 3: Faction Standing Tracker

> Dynamic influence tracking affecting available quests and NPC interactions

## Faction Variables

```mermaid
erDiagram
    PC ||--o{ FACTION_STANDING : affects
    FACTION_STANDING {
        string factionName
        int standing
        int maxStanding
        int minStanding
    }
    FACTION_STANDING ||--o{ QUEST_UNLOCK : enables
    
    QUEST {
        string questName
        int requiredStanding
        string availableFrom
    }
```

## Faction Standing Effects

```mermaid
flowchart LR
    subgraph Faction_Standing_Boosts
        Moot[Moot speech] -->|"+2"| FS_PLUS[Free Sartar +]
        PatrolGood[Good patrol] -->|"+1"| WS_PLUS[Wolfskinners +]
        HealGood[Heal wounded] -->|"+1"| EH_PLUS[Eye of Hurricane +]
        AttackLunar[Lunar attack] -->|"+2"| CS_PLUS[Conquering Storm +]
        LunarHelp[Help Lunar] -->|"+2"| MW_PLUS[Moon Winds +]
    end
    
    subgraph Faction_Standing_Penalties
        MootFail[Failed speech] -->|"-1"| FS_MINUS
        PatrolFail[Failed patrol] -->|"-1"| WS_MINUS
        IgnoreCrisis[Ignore crisis] -->|"-2"| EH_MINUS
        RefuseCombat[Refuse fight] -->|"-1"| CS_MINUS
        RebelHelp[Help rebels] -->|"-2"| MW_MINUS
    end
    
    subgraph Standing_Thresholds
        FS_PLUS -->|"Standing >= 15"| FS_HIGH[Unlock rebel quests<br/>Meet Kallyr]
        WS_PLUS -->|"Standing >= 15"| WS_HIGH[Join wolf hunt<br/>Jomes trust]
        CS_PLUS -->|"Standing >= 15"| CS_HIGH[Lead raid<br/>Darna favor]
        EH_PLUS -->|"Standing >= 15"| EH_HIGH[Peace missions<br/>Broddi trust]
        MW_PLUS -->|"Standing >= 15"| MW_HIGH[Imperial favor<br/>Unlock Lunar quests]
    end
```

## Faction NPC Access

```mermaid
flowchart TD
    subgraph Free_Sartar_Access
        FS_10[Standing >= 10] --> FS_RUM[Access: Rumors]
        FS_15[Standing >= 15] --> FS_MEET[Meet: Kallyr Starbrow]
        FS_20[Standing >= 20] --> FS_JOIN[Join: Rebel band]
        FS_20 --> FS_INTEL[Intel: Lunar plans]
    end
    
    subgraph Wolfskinners_Access
        WS_10[Standing >= 10] --> WS_RUM[Access: Wolf patrols]
        WS_15[Standing >= 15] --> WS_MEET[Quest: Hunt Jogar]
        WS_20[Standing >= 20] --> WS_JOIN[Quest: Jomes secret]
    end
    
    subgraph Conquering_Storm_Access
        CS_10[Standing >= 10] --> CS_RUM[Access: Raids]
        CS_15[Standing >= 15] --> CS_MEET[Quest: Darna mission]
        CS_20[Standing >= 20] --> CS_JOIN[Lead: War party]
    end
    
    subgraph Eye_of_Hurricane_Access
        EH_10[Standing >= 10] --> EH_RUM[Access: Peace talks]
        EH_15[Standing >= 15] --> EH_MEET[Quest: Mediate]
        EH_20[Standing >= 20] --> EH_JOIN[Counsel: Broddi]
    end
    
    subgraph Moon_Winds_Access
        MW_10[Standing >= 10] --> MW_RUM[Access: Lunar news]
        MW_15[Standing >= 15] --> MW_MEET[Quest: Temple help]
        MW_20[Standing >= 20] --> MW_JOIN[Convert: Secret]
        MW_20 --> MW_INTEL[Lunar secrets]
    end
```

---

# Enhancement 5: Multiple Ending Paths

> Distinct conclusions based on PC choices and faction alignment

## Ending Decision Tree

```mermaid
flowchart TD
    START[1625 Ending] --> CHECK_ALL[Check all conditions]
    
    CHECK_ALL --> COND1{FS >= 20<br/>WS >= 15}
    COND1 -->|"Yes"| LIB_SUCCESS[Liberation Success]
    COND1 -->|"No"| CHECK_2
    
    CHECK_2 --> COND2{MW >= 20<br/>Lunar favor high}
    COND2 -->|"Yes"| COMP_SUCCESS[Compromise Success]
    COND2 -->|"No"| CHECK_3
    
    CHECK_3 --> COND3{Resources <= 5<br/>No allies}
    COND3 -->|"Yes"| EXILE[Exile Ending]
    COND3 -->|"No"| FINAL_CHANCE[Final Battle]
    
    FINAL_CHANCE --> ROLL{Military roll}
    ROLL -->|"Victory"| LIB_SUCCESS
    ROLL -->|"Defeat"| EXILE
    ROLL -->|"Mixed"| COMP_SUCCESS
    
    LIB_SUCCESS --> END_L[Freedom Ending:<br/>Sartar liberated]
    COMP_SUCCESS --> END_C[Collab Ending:<br/>Survival with Lunars]
    EXILE --> END_E[Exile Ending:<br/>Clan scattered]
```

## Freedom Ending Branch

```mermaid
flowchart TD
    FREE[Freedom Ending] --> F1["Year 1625:<br/>Dangerford Battle"]
    F1 --> F2{Combat Victory}
    F2 -->|"Yes"| F3[Lunar defeated]
    F2 -->|"No"| F4[Peace treaty]
    
    F3 --> F5[Jonstown freed]
    F4 --> F5
    F5 --> F6["Kallyr assumes<br/>power]
    F6 --> F7{"Support Kallyr"}
    
    F7 -->|"Yes"| F8[Republic ending:<br/>New Sartar]
    F7 -->|"No"| F9[ monarchy ending:<br/>Queenship]
    
    F8 --> EPILOGUE_F[Epilogue:<br/>PCs as heroes]
    F9 --> EPILOGUE_F
```

## Collaboration Ending Branch

```mermaid
flowchart TD
    COLLAB[Collaboration Ending] --> C1["Year 1625:<br/>Negotiate]
    C1 --> C2{Terms accepted}
    C2 -->|"Yes"| C3[Lunar terms]
    C2 -->|"No"| C4[Exile instead]
    
    C3 --> C4["Clan survives<br/>Under Lunar rule]
    C4 --> C5["PCs granted<br/>positions]
    C5 --> C6{"Accept posts"}
    
    C6 -->|"Yes"| C7[Official career:<br/>Serve Empire]
    C6 -->|"No"| C8[Quiet life:<br/>Withdraw]
    
    C7 --> EPILOGUE_C[Epilogue:<br/>Mixed legacy]
    C8 --> EPILOGUE_C
```

## Exile Ending Branch

```mermaid
flowchart TD
    EXILE[Exile Ending] --> E1["Year 1625:<br/>Clan falls]
    E1 --> E2[Red Cow destroyed]
    E2 --> E3[Scattered survivors]
    E3 --> E4["PCs escape<br/>to wilderness]
    E4 --> E5["Form outlaw<br/>band]
    E5 --> E6{"Join rebels"}
    
    E6 -->|"Yes"| E7[Continue fight:<br/>Guerrilla war]
    E6 -->|"No"| E8[New life:<br/>Elsewhere]
    
    E7 --> EPILOGUE_E1[Epilogue:<br/>Ever fighting]
    E8 --> EPILOGUE_E2[Epilogue:<br/>New beginning]
```

## Ending Effects Summary

```mermaid
mindmap
  (Multiple Endings)
    Freedom Ending
      Kallyr liberated
      PCs as heroes
      New Sartar Republic
    Collaboration Ending
      Survive under Lunar
      Mixed legacy
      Quiet service
    Exile Ending
      Outlaw band
      New beginning
      Endless fight
```

## Epilogue NPCs by Ending

```mermaid
flowchart LR
    subgraph Freedom_Epilogue
        FE[Freedom Ending] --> FE1[Queen Ivartha]
        FE --> FE2[Kallyr Starbrow]
        FE --> FE3[Free Sartar]
        FE --> FE4[Rebel leaders]
    end
    
    subgraph Collab_Epilogue
        CE[Collab Ending] --> CE1[Jomes Hostralos]
        CE --> CE2[Lunar priests]
        CE --> CE3[Imperial officials]
        CE --> CE4[Moon Winds]
    end
    
    subgraph Exile_Epilogue
        EE[Exile Ending] --> EE1[Venharl Stormbrow]
        EE --> EE2[Orstalor Spearlord]
        EE --> EE3[Outlaw camps]
        EE --> EE4[Hidden rebels]
    end
```

---

## Notes

- **Year tracking**: Global variable `$year` (1618-1625)
- **Season tracking**: Sea/Fire/Earth/Dark/Storm
- **Resource decay**: Background events each season
- **Faction influence**: Player actions affect faction standing
- **Character arcs**: Each PC has year-specific story beats
- **Multiple endings**: Based on PC choices and faction alignment