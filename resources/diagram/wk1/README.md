## Lịch sử phát triển máy tính
```mermaid
flowchart TB
    A[1642: Pascaline] --> B[1837: Analytical Engine]
    B --> C[1890: Hollerith Tabulator]
    C --> D[1946: ENIAC – đèn điện tử]
    D --> E[1951: UNIVAC I – thương mại]
    E --> F[1956–1963: Thế hệ 2 – Transistor]
    F --> G[1964–1971: Thế hệ 3 – IC]
    G --> H[1971: Intel 4004 – Vi xử lý]
    H --> I[1981: IBM PC]
    I --> J[1990s: Internet phổ biến]
    J --> K[2007: iPhone – Smartphone]
    K --> L[2016: TPU – AI Accelerator]
    L --> M[2020s: Generative AI, GPU/TPU mới]
    style A fill:#f9f,stroke:#333,stroke-width:2px
```
***
### Tổng quan hệ thống máy tính
```mermaid
graph LR
  subgraph System["Hệ thống máy tính"]
    CPU["CPU"]
    MEM["Bộ nhớ (RAM/ROM)"]
    IO["Thiết bị Vào/Ra (I/O)"]
    BUS["Bus hệ thống"]
  end

  CPU --- BUS
  MEM --- BUS
  IO  --- BUS

  subgraph CPU_Breakdown["Bên trong CPU"]
    ALU["ALU"]
    CU["CU"]
    REG["Thanh ghi"]
  end

  CPU --- ALU
  CPU --- CU
  CPU --- REG
```

### Cấu trúc bên trong CPU (ALU, CU, Thanh ghi, Cache)
```mermaid
graph TD
  subgraph CPU["CPU"]
    subgraph FrontEnd["Front-End"]
      IF["Instruction Fetch"]
      ID["Instruction Decode"]
    end
    subgraph Core["Core"]
      REG["Register File"]
      ALU["ALU (Arithmetic Logic Unit)"]
      CU["Control Unit"]
    end
    subgraph MemorySide["Bộ nhớ đệm (Cache)"]
      L1["L1 Cache"]
      L2["L2 Cache"]
      L3["L3 Cache (chia sẻ)"]
    end
  end

  IF --> ID --> REG --> ALU
  CU -. điều khiển .-> IF
  CU -. điều khiển .-> ID
  CU -. điều khiển .-> REG
  CU -. điều khiển .-> ALU

  L1 --> L2 --> L3
  L1 -- nạp/ghi --> REG

```

### Phân cấp bộ nhớ (tốc độ nhanh → chậm)
```mermaid
graph TB
  REG["Thanh ghi (ns, nhỏ, nhanh nhất)"]
  L1["L1 Cache (rất nhanh, rất nhỏ)"]
  L2["L2 Cache (nhanh, nhỏ)"]
  L3["L3 Cache (nhanh vừa, lớn hơn)"]
  RAM["RAM (truy cập chính, lớn)"]
  SSD["SSD (lưu trữ lâu dài)"]
  HDD["HDD (lưu trữ dài hạn, rẻ/GB)"]

  REG --> L1 --> L2 --> L3 --> RAM --> SSD --> HDD
  click REG "https://en.wikipedia.org/wiki/Processor_register" "Thanh ghi"

```

### Thiết bị vào/ra và Bộ điều khiển I/O
```mermaid
graph LR
  subgraph Host["Máy tính"]
    CPU["CPU"]
    MEM["RAM"]
    BUS["System Bus"]
    IOC["Bộ điều khiển I/O"]
  end

  CPU --- BUS
  MEM --- BUS
  IOC --- BUS

  subgraph Inputs["Thiết bị Vào"]
    KB["Bàn phím"]
    MS["Chuột"]
    MIC["Microphone"]
    SC["Máy quét"]
  end

  subgraph Outputs["Thiết bị Ra"]
    MON["Màn hình"]
    SPK["Loa"]
    PRN["Máy in"]
  end

  KB --- IOC
  MS --- IOC
  MIC --- IOC
  SC --- IOC

  IOC --- MON
  IOC --- SPK
  IOC --- PRN

```

### Bus hệ thống (Data/Address/Control)
```mermaid
graph TB
  CPU["CPU"] --- DBUS["Data Bus (truyền dữ liệu)"]
  CPU --- ABUS["Address Bus (địa chỉ ô nhớ/I/O)"]
  CPU --- CBUS["Control Bus (tín hiệu điều khiển)"]

  DBUS --- MEM["Bộ nhớ"]
  DBUS --- IO["Thiết bị I/O"]
  ABUS --- MEM
  ABUS --- IO
  CBUS --- MEM
  CBUS --- IO

```

### Chu trình nhập phím → hiển thị (Sequence Diagram)
```mermaid
sequenceDiagram
  participant User as Người dùng
  participant KB as Bàn phím
  participant IOC as Bộ điều khiển I/O
  participant CPU as CPU
  participant RAM as RAM
  participant GPU as GPU/Display Adapter
  participant MON as Màn hình

  User->>KB: Nhấn phím
  KB->>IOC: Tín hiệu phím (scan code)
  IOC->>CPU: Ngắt (interrupt) + dữ liệu phím
  CPU->>RAM: Cập nhật buffer nhập
  CPU->>GPU: Gửi khung văn bản cần vẽ
  GPU->>MON: Tín hiệu hình ảnh
  MON-->>User: Ký tự xuất hiện trên màn hình

```
