# Evolução dos Microprocessadores
### 3 principais fases
1. Pré microprocessadores
2. Microprocessadores
3. Futuro/SOTA

***
# 1. Pré-Microprocessadores
* Eniac
    * válvula e arquitetura
* Revolução do transistor
    * Bell Labs
* Circuitos Integrados
# 2. Microprocessadores
* Intel começo
    * Intel 4004
    * Bit evolution (8 -> 16bits) + x86 invention
    * -concorrentes (zilog / MOS)- 
* Risc arquitetura
    * Arm 1
    * Mips
    * SPARCI
* Integração no chip + Mudança na arquitetura
    * Cache e FPU no chip
    * Arquitetura Superscalar
    * -Out-of-order-
* Cpus Multi core e SoC
    * Amd Athlon x2 / Pentium Dual
    * Controladores de memórias / Gpu Integradas
* Mobile SoCs e computação heterôgenea
    * Avanço do ARM (mobile)
    * Cores híbridos (Big-  Little)
# 3. Futuro / SOTA
* Soc's avançados
    * Full SoC's (apple M1/AMD HALO) 
    * Npu's integradas
    * 3D empacotamento
    * Chiplets
* -Domínio de GPU's-
    * Nvidia Paralelism?
* -Photonics-

```mermaid
---
config:
  nodeSpacing: 80

---
flowchart LR
 subgraph Org[" "]
        Circ["Circuitos Integrados"]
        RevTran["Revolução dos transistores"]
        Eniac["Eniac"]
  end
 subgraph Pre["Pré-Microprocessadores"]
        Org
  end
 subgraph Intel["Intel"]
        Mb(["Concorrentes -Zilog/MOS-"])
        Bt["Bit evolution 8-16bits + x86"]
        Frst["Intel 4004"]
  end
 subgraph Risc["Risc"]
        SPARCI["SPARCI"]
        Mips["Mips"]
        Arm["Arm 1"]
  end
 subgraph thrd["Integração no chip + Mudança na arquitetura"]
        Out(["Out of order"])
        Arq["Arquitetura superscalar"]
        Cache["Cache + Fpu Integrados"]
  end
 subgraph frth["Cpus Multi core e SoC"]
        Integ["Controladores de memórias / Gpu Integradas"]
        Dual["Amd Athlon x2 / Pentium Dual"]
  end
 subgraph fifth["Mobile SoCs e computação heterôgenea"]
        Bl["Cores híbridos Big- Little"]
        Mbl["Avanço do ARM mobile"]
  end
 subgraph Mic["Microprocessadores"]
        Intel
        Risc
        thrd
        frth
        fifth
  end
 subgraph Adv["Soc's avançados"]
        Chiplets["Chiplets"]
        3d["3D empacotamento"]
        Npu@{ label: "Npu's integradas" }
        Flsoc@{ label: "Full SoC's apple M1/AMD HALO" }
  end
 subgraph Gpu["-Domínio de GPU's-"]
  end
 subgraph Phts["-Photonics-"]
  end
 subgraph Fut["Futuro/SOTA"]
        Adv
        Gpu
        Phts
  end
    Eniac --> RevTran
    RevTran --> Circ
    Frst --> Bt
    Bt --> Mb
    Arm --> Mips
    Mips --> SPARCI
    Cache --> Arq
    Arq --> Out
    Dual --> Integ
    Mbl --> Bl
    Flsoc --> Npu
    Npu --> 3d
    3d --> Chiplets
    Pre --> Mic
    Mic --> Fut
    Intel --> Risc
    Risc --> thrd
    thrd --> frth
    frth --> fifth
    Adv --> Gpu
    Gpu --> Phts
```
