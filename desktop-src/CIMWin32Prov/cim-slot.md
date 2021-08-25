---
description: CIM 位置 \_ 類別代表要插入封裝的連接器。
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 910fb4a3dcd5d3d95ef524d838781bad8331d33d71fc0af8ebd358ac9dd9588e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919458"
---
# <a name="cim_slot-class"></a>CIM \_ 插槽類別

**CIM 位置 \_** 類別代表要插入封裝的連接器。 例如，您可以將磁片磁碟機的實體封裝插入到 SCA 插槽，或 ([CIM \_ PhysicalPackage](cim-physicalpackage.md) 的子類別，) 可以插入至裝載面板上的16、32或64位擴充位置。 PCI 或 PCMCIA 類型 III 插槽是後者的範例。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a>成員

**CIM \_ 插槽** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ 插槽** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述 pin 設定的自由格式字串，以及實體連接器的使用信號。

這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。

</dd> <dt>

**ConnectorType**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ConnectorType" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.2 ") 
</dt> </dl>

實體連接器的類型。 指定陣列以允許連接器資訊組合的描述。 例如，一個陣列專案可以指定 RS-232，另一個資料庫-25，第三個則可以將連接器定義為「男性」。

這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。

<dt>

0
</dt> <dd>

Unknown

</dd> <dt>

1
</dt> <dd>

其他

</dd> <dt>

2
</dt> <dd>

Male

</dd> <dt>

3
</dt> <dd>

Female

</dd> <dt>

4
</dt> <dd>

受防護

</dd> <dt>

5
</dt> <dd>

受防護

</dd> <dt>

6
</dt> <dd>

SCSI () 高密度 (50 針腳) 

</dd> <dt>

7
</dt> <dd>

SCSI () 低密度 (50 針腳) 

</dd> <dt>

8
</dt> <dd>

SCSI (P) 高密度 (68 針腳) 

</dd> <dt>

9
</dt> <dd>

SCSI SCA-I (80 釘選) 

</dd> <dt>

10
</dt> <dd>

SCSI SCA-II (80 針腳) 

</dd> <dt>

11
</dt> <dd>

SCSI 光纖通道 (DB-9、銅) 

</dd> <dt>

12
</dt> <dd>

 (光纖) 的 SCSI 光纖通道

</dd> <dt>

13
</dt> <dd>

SCSI 光纖通道 SCA-II (40 釘選) 

</dd> <dt>

14
</dt> <dd>

SCSI 光纖通道 SCA-II (20 個 pin) 

</dd> <dt>

15
</dt> <dd>

SCSI 光纖通道 BNC

</dd> <dt>

16
</dt> <dd>

ATA 3-1/2 英寸 (40 針腳) 

</dd> <dt>

17
</dt> <dd>

ATA 2-1/2 英寸 (44 針腳) 

</dd> <dt>

18
</dt> <dd>

ATA-2

</dd> <dt>

19
</dt> <dd>

ATA-3

</dd> <dt>

20
</dt> <dd>

ATA/66

</dd> <dt>

21
</dt> <dd>

DB-9

</dd> <dt>

22
</dt> <dd>

DB-15

</dd> <dt>

23
</dt> <dd>

DB-25

</dd> <dt>

24
</dt> <dd>

DB-36

</dd> <dt>

25
</dt> <dd>

RS-232C

</dd> <dt>

26
</dt> <dd>

RS-422

</dd> <dt>

27
</dt> <dd>

RS-423

</dd> <dt>

28
</dt> <dd>

RS-485

</dd> <dt>

29
</dt> <dd>

RS-449

</dd> <dt>

30
</dt> <dd>

V. 35

</dd> <dt>

31
</dt> <dd>

X. 21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

AUI

</dd> <dt>

34
</dt> <dd>

UTP 類別3

</dd> <dt>

35
</dt> <dd>

UTP 類別4

</dd> <dt>

36
</dt> <dd>

UTP 類別5

</dd> <dt>

37
</dt> <dd>

BNC

</dd> <dt>

38
</dt> <dd>

RJ11

</dd> <dt>

39
</dt> <dd>

根

</dd> <dt>

40
</dt> <dd>

光纖 MIC

</dd> <dt>

41
</dt> <dd>

Apple AUI

</dd> <dt>

42
</dt> <dd>

Apple GeoPort

</dd> <dt>

43
</dt> <dd>

PCI

</dd> <dt>

44
</dt> <dd>

ISA

</dd> <dt>

45
</dt> <dd>

EISA

</dd> <dt>

46
</dt> <dd>

VESA

</dd> <dt>

47
</dt> <dd>

PCMCIA

</dd> <dt>

48
</dt> <dd>

PCMCIA 類型 I

</dd> <dt>

49
</dt> <dd>

PCMCIA 類型 II

</dd> <dt>

50
</dt> <dd>

PCMCIA 類型 III

</dd> <dt>

51
</dt> <dd>

ZV 埠

</dd> <dt>

52
</dt> <dd>

CardBus

</dd> <dt>

53
</dt> <dd>

USB

</dd> <dt>

54
</dt> <dd>

IEEE 1394

</dd> <dt>

55
</dt> <dd>

HIPPI

</dd> <dt>

56
</dt> <dd>

HSSDC (6 個 pin) 

</dd> <dt>

57
</dt> <dd>

GBIC

</dd> <dt>

58
</dt> <dd>

DIN

</dd> <dt>

59
</dt> <dd>

迷你

</dd> <dt>

60
</dt> <dd>

微型

</dd> <dt>

61
</dt> <dd>

PS/2

</dd> <dt>

62
</dt> <dd>

紅外線

</dd> <dt>

63
</dt> <dd>

HP-HIL

</dd> <dt>

64
</dt> <dd>

存取。匯流排

</dd> <dt>

65
</dt> <dd>

NuBus

</dd> <dt>

66
</dt> <dd>

Centronics

</dd> <dt>

67
</dt> <dd>

Mini-Centronics

</dd> <dt>

68
</dt> <dd>

Mini-Centronics 類型-14

</dd> <dt>

69
</dt> <dd>

Mini-Centronics 類型-20

</dd> <dt>

70
</dt> <dd>

Mini-Centronics 類型-26

</dd> <dt>

71
</dt> <dd>

匯流排滑鼠

</dd> <dt>

72
</dt> <dd>

亞行

</dd> <dt>

73
</dt> <dd>

AGP

</dd> <dt>

74
</dt> <dd>

VM 匯流排

</dd> <dt>

75
</dt> <dd>

VME64

</dd> <dt>

76
</dt> <dd>

專屬

</dd> <dt>

77
</dt> <dd>

專屬處理器卡插槽

</dd> <dt>

78
</dt> <dd>

專屬記憶卡插槽

</dd> <dt>

79
</dt> <dd>

專屬的 i/o Riser 插槽

</dd> <dt>

80
</dt> <dd>

PCI-66MHZ

</dd> <dt>

81
</dt> <dd>

AGP2X

</dd> <dt>

82
</dt> <dd>

AGP4X

</dd> <dt>

83
</dt> <dd>

電腦-98

</dd> <dt>

84
</dt> <dd>

電腦-98-Hireso

</dd> <dt>

85
</dt> <dd>

電腦-H98

</dd> <dt>

86
</dt> <dd>

電腦-98Note

</dd> <dt>

87
</dt> <dd>

電腦-98Full

</dd> <dt>

88
</dt> <dd>

SSA SCSI

</dd> <dt>

89
</dt> <dd>

圓形

</dd> <dt>

90
</dt> <dd>

面板 IDE 連接器

</dd> <dt>

91
</dt> <dd>

在面板上的軟碟連接器

</dd> <dt>

92
</dt> <dd>

9個雙線插換行

</dd> <dt>

93
</dt> <dd>

25個雙內嵌的 Pin

</dd> <dt>

94
</dt> <dd>

50釘選雙重內嵌

</dd> <dt>

95
</dt> <dd>

68釘選雙重內嵌

</dd> <dt>

96
</dt> <dd>

面板音效連接器

</dd> <dt>

97
</dt> <dd>

迷你插口

</dd> <dt>

98
</dt> <dd>

PCI X

</dd> <dt>

99
</dt> <dd>

S 匯流排 IEEE 1396-1993 32 位

</dd> <dt>

100
</dt> <dd>

S 匯流排 IEEE 1396-1993 64 位

</dd> <dt>

101
</dt> <dd>

MCA

</dd> <dt>

102
</dt> <dd>

喬

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

HIO

</dd> <dt>

105
</dt> <dd>

NGIO

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

MTRJ

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

未來的 i/o

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

電子

</dd> <dt>

113
</dt> <dd>

光學

</dd> <dt>

114
</dt> <dd>

功能區

</dd> <dt>

115
</dt> <dd>

GLM

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

小 SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

HSSC

</dd> <dt>

120
</dt> <dd>

VHDCI 防護 (68 pin) 

</dd> <dt>

121
</dt> <dd>

Infiniband

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**HeightAllowed**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) 
</dt> </dl>

可插入至插槽的介面卡卡片最大高度（以英寸為單位）。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LengthAllowed**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) 
</dt> </dl>

可以插入至插槽的介面卡卡片最大長度（以英寸為單位）。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

產生實體元素的組織。 如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 位 ") 
</dt> </dl>

可以插入至插槽的介面卡的最大匯流排寬度（以位為單位）。

<dt>

<span id="8"></span>

**8** (0) 


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** (1) 


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** (2) 


</dt> <dd></dd> <dt>

<span id="64"></span>

**64** (3) 


</dt> <dd></dd> <dt>

<span id="128"></span>

**128** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**型號**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

實體元素一般已知的名稱。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**Number**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

實體位置編號，可用來做為系統位置資料表的索引，以判斷位置是否實際被佔用。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除了資產標記資訊以外的其他資料，可用來識別實體元素。 其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。 請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

由產生或製造實體元素的組織所指派的元件編號。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示實體元素已開啟電源。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_** 位置」。**SpecialPurpose**") 
</dt> </dl>

描述此位置實際是唯一的，且可能保存特殊硬體類型的自由格式字串。 只有當對應的布林 **SpecialPurpose** 屬性設定為 **TRUE** 時，這個屬性才有意義。

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

製造商配置的數位，用來識別實體元素。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

實體元素的庫存單位號碼。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**SpecialPurpose**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_** 位置」。**PurposeDescription**") 
</dt> </dl>

若 **為 TRUE**，則位置實際上是唯一的，而且可能保存特殊類型的硬體， (例如，圖形處理器插槽) 。 若 **為 TRUE**， **PurposeDescription** 屬性應該指定位置是唯一的，還是位置的用途。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsHotPlug**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則位置支援介面卡的熱插即用。

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

可唯一識別實體元素並作為專案索引鍵的任一字元串。 這個屬性可包含資產標記或序號資料等資訊。 在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中非常高的位置，以獨立識別硬體/實體，無論 (或) 的封包、介面卡等等。 例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。 物件仍會持續存在，甚至可以插入至不同的範圍容器。 實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**ThermalRating**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 毫瓦 ") 
</dt> </dl>

插槽的最高散熱量（以毫瓦）。

</dd> <dt>

**VccMixedVoltageSupport**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.9 ") 
</dt> </dl>

插槽所支援的 Vcc 電壓。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2) 


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5v** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

實體元素的版本。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**VppMixedVoltageSupport**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統插槽 \| 004.10 ") 
</dt> </dl>

插槽所支援的 Vpp 電壓。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2) 


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5v** (3) 


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12v** (4) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ 插槽** 類別衍生自 [**cim \_ PhysicalConnector**](cim-physicalconnector.md)。

WMI 不會執行這個類別。 針對衍生自 CIM 位置 **的 \_ WMI 類別**，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> </dl>

 

