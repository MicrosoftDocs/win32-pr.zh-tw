---
description: CIM \_ PhysicalConnector 類別代表用來連接到其他元素的任何實體元素。 任何可以連接及傳輸兩個或多個實體元素之間的信號或電源的物件，都是此類別的子系 (或成員) 。
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: CIM_PhysicalConnector 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972779"
---
# <a name="cim_physicalconnector-class"></a>CIM \_ PhysicalConnector 類別

**CIM \_ PhysicalConnector** 類別代表用來連接到其他元素的任何實體元素。 任何可以連接及傳輸兩個或多個實體元素之間的信號或電源的物件，都是此類別的子系 (或成員) 。 例如，插槽和 D shell 連接器是實體連接器的類型。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a>成員

**CIM \_ PhysicalConnector** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ PhysicalConnector** 類別具有這些屬性。

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

</dd> <dt>

**ConnectorType**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

實體連接器的類型。 指定陣列以允許連接器資訊組合的描述。 例如，一個陣列專案可以指定 RS-232、另一個資料庫-25 和第三個專案可以將連接器定義為「男性」。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

**男性** (2) 


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

**女性** (3) 


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

**受防護** 的 (4) 


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

非 **遮罩** (5) 


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

**SCSI () High-Density (50 針腳)** (6) 


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

**SCSI () Low-Density (50 針腳)** (7) 


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

**SCSI (P) High-Density (68 針腳)** (8) 


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

**SCSI SCA-I (80 針腳)** (9) 


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

**SCSI SCA-II (80 針腳)** (10) 


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

**SCSI 光纖通道 (DB-9、銅)** (11) 


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

**SCSI 光纖通道 (光纖)** (12) 


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

**SCSI 光纖通道 SCA-II (40 針腳)** (13) 


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

**SCSI 光纖通道 SCA-II (20 部 pin)** (14) 


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

**SCSI 光纖通道 BNC** (15) 


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

**ATA 3-1/2 英寸 (40 針腳)** (16) 


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

**ATA 2-1/2 英寸 (44 針腳)** (17) 


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

**ATA-2** (18) 


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

**ATA-3** (19) 


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

**ATA/66** (20) 


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

**Db-library** (21) 


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

**DB-15** (22) 


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

**DB-25** (23) 


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

**DB-36** (24) 


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

**Rs-232c** (25) 


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

**RS-422** (26) 


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

**RS-423** (27) 


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

**RS-485** (28) 


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

**RS-449** (29) 


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

**V. 35** (30) 


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

**X. 21** (31) 


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

**IEEE-488** (32) 


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

**AUI** (33) 


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

**UTP 類別 3** (34) 


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

**UTP 類別 4** (35) 


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

**UTP 類別 5** (36) 


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

**BNC** (37) 


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

**RJ11** (38) 


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

**RJ45** (39) 


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

**光纖 MIC** (40) 


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

**APPLE AUI** (41) 


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

**Apple GeoPort** (42) 


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

**PCI** (43) 


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

**ISA** (44) 


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

**EISA** (45) 


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

**VESA** (46) 


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

**PCMCIA** (47) 


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

**PCMCIA 類型 I** (48) 


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

**PCMCIA 類型 II** (49) 


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

**PCMCIA 類型 III** (50) 


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

**ZV 埠** (51) 


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

**CardBus** (52) 


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

**USB** (53) 


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

**IEEE 1394** (54) 


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

**HIPPI** (55) 


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

**HSSDC (6 針腳)** (56) 


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

**GBIC** (57) 


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

**(58**) 


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

**迷你** 等 (59) 


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

**微型** (60) 


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

**PS/2** (61) 


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**紅外線** (62) 


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

**HP HIL** (63) 


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

**存取. bus** (64) 


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

**NuBus** (65) 


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

**Centronics** (66) 


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

**迷你 Centronics** (67) 


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

**迷你 Centronics 類型-14** (68) 


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

**迷你 Centronics 類型-20** (69) 


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

**迷你 Centronics 類型-26** (70) 


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

**匯流排滑鼠** (71) 


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

**ADB** (72) 


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

**AGP** (73) 


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

**Vm 匯流排** (74) 


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

**VME64** (75) 


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

**專屬** (76) 


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

**專屬處理器卡插槽** (77) 


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

**專屬記憶卡插槽** (78) 


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

**專屬 I/o Riser 卡插槽** (79) 


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

**PCI-66MHZ** (80) 


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

**AGP2X** (81) 


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

**AGP4X** (82) 


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (83) 


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

**PC-98-Hireso** (84) 


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

**PC-H98** (85) 


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

**PC-98Note** (86) 


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

**PC-98Full** (87) 


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

**SSA SCSI** (88) 


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

**迴圈** (89) 


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

**On 面板 IDE 連接器** (90) 


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

**在主機板軟盤機上** (91) 


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

**9 釘選雙重內嵌** (92) 


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

**25 個 Pin 雙內嵌** (93) 


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

**50 釘選雙重內嵌** (94) 


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

**68 釘選雙重內嵌** (95) 


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

**面板音效連接器** (96) 


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

**迷你插座** (97) 


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

**PCI-X** (98) 


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

**S 匯流排 IEEE 1396-1993 32 位** (99) 


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

**S 匯流排 IEEE 1396-1993 64 位** (100) 


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

**MCA** (101) 


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

**GIO** (102) 


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

**XIO** (103) 


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

**HIO** (104) 


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

**NGIO** (105) 


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

**PMC** (106) 


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

**MTRJ** (107) 


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

**VF-45** (108) 


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

**未來的 i/o** (109) 


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

**SC** (110) 


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

**SG** (111) 


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

**電** (112) 


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

**光學** (113) 


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

**功能區** (114) 


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

**GLM** (115) 


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

**1x9** (116) 


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

 (117) 的 **最小 SG**


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

**LC** (118) 


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

**HSSC** (119) 


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

**VHDCI 防護 (68 pin)** (120) 


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**(121**) 的不限


</dt> <dd></dd> </dl>

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

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

負責產生實體元素的組織名稱。 如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

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

負責產生或製造實體元素的組織所指派的元件編號。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示實體元素已開啟電源。 否則，它目前為關閉狀態。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

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

此實體元素的庫存單位號碼。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

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

**Tag**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

可唯一識別實體元素，並作為專案的索引鍵。 這個屬性可包含資產標記或序號資料等資訊。 在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。 例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。 物件仍會持續存在，甚至可以插入至不同的範圍容器。 實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

指出實體元素的版本。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ PhysicalConnector** 類別衍生自 [**cim \_ PhysicalElement**](cim-physicalelement.md)。

WMI 不會執行這個類別。 針對衍生自 **CIM \_ PHYSICALCONNECTOR** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。

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

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> </dl>

 

