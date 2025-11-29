---
toc: false 
layout: post
title: Tools Journey 
description: Journey with development tools -- GitHub, Cloning, Virtual Environments, and Running a local website.
permalink: /tools/journey
---

## Visual Journey

   I use an Macbook air   

![Tux the Linux Mascot]({{site.baseurl}}/images/tux.png)

This visual help remind me of Tools and their relationship to my Development Journey. 

flowchart TD
    %% GitHub Sources
    subgraph GitHub_Pages[GitHub: Open-Coding-Society/pages]
        A[Repo: pages]:::repo
    end

    subgraph GitHub_Template[GitHub: Open-Coding-Society/student]
        T[Template Repo: student]:::repo
    end

    subgraph GitHub_Student[GitHub: Jas-Bop/student]
        B[Repo: student]:::repo
    end

    %% Local Computer
    subgraph Local[Local Computer]
        subgraph opencs_dir[opencs/ directory]
            C[pages/]:::local
            Ccmd[VSCode Prep<br/><br/>./scripts/venv.sh<br/>source venv/bin/activate<br/>code .]:::cmd
        end
        subgraph user_dir[Jas-Bop/ directory]
            D[student/]:::local
            Dcmd[VSCode Prep<br/><br/>./scripts/venv.sh<br/>source venv/bin/activate<br/>code .]:::cmd
        end
    end

    %% Arrows: cloning
    A -.->|clone/pull only| C
    B <--> |clone, pull & push| D

    %% Arrows: template relationship
    T -.->|template → created| B

    %% Arrows: commands
    C --> Ccmd
    D --> Dcmd

    %% Styling (optional)
    classDef repo fill:#d0e3ff,stroke:#4a78c8,stroke-width:1px
    classDef local fill:#e8ffe8,stroke:#4ac84a,stroke-width:1px
    classDef cmd fill:#fffecf,stroke:#c8b84a,stroke-width:1px
