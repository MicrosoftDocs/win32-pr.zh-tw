---
description: Win32 \_ SystemSlot &\# 32;WMI 類別代表實體連接點，包括埠、主機板插槽和週邊設備，以及專屬的連接點。
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Win32_SystemSlot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111477"
---
# <a name="win32_systemslot-class"></a>Win32 \_ SystemSlot 類別

**Win32 \_ SystemSlot** [WMI 類別](../wmisdk/retrieving-a-class.md)代表實體連接點，包括埠、主機板插槽和週邊設備，以及專屬的連接點。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
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
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
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

**Win32 \_ SystemSlot** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SystemSlot** 類別具有這些屬性。

<dl> <dt>

**BusNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Bus Number" ) 
</dt> </dl>

SMBIOS 匯流排號碼。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **匯流排編號** 成員。

**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短描述（單行字串）。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述 pin 設定的自由格式字串，以及實體連接器的信號使用方式。

這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。

</dd> <dt>

**ConnectorType**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "ConnectorType" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| type 9 \| 插槽類型" ) 
</dt> </dl>

此位置使用之連接器的實體屬性陣列。

此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **類型** 成員。

這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。

可能的值為。

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

<span id="PCI-X"></span><span id="pci-x"></span>

**PCI-X** (88) 


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

**S 匯流排 IEEE 1396-1993 32 位** (89) 


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

**S 匯流排 IEEE 1396-1993 64 位** (90) 


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

**MCA** (91) 


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

**GIO** (92) 


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

**XIO** (93) 


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

**HIO** (94) 


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

**NGIO** (95) 


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

**PMC** (96) 


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

**未來的 i/o** (97) 


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**(98**) 的不限


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

**AGP8X** (99) 


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

**PCI-E** (100) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓您以唯一的方式識別此類別和其子類別的所有實例。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**CurrentUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Current Usage" ) 
</dt> </dl>

系統位置使用的狀態。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **目前使用** 成員。

可能的值為。

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**保留** (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

**可用** (3) 


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

**使用** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Device Number" ) 
</dt> </dl>

SMBIOS 裝置編號。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **裝置/** 函式編號成員。

**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**FunctionNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Function Number" ) 
</dt> </dl>

SMBIOS 功能編號。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **裝置/** 函式編號成員。

**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**HeightAllowed**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) 
</dt> </dl>

可以插入至插槽的介面卡卡片最大高度（以英寸為單位）。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
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

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) 
</dt> </dl>

可以插入插槽中的介面卡卡片最大長度（以英寸為單位）。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

產生實體元素的組織名稱。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "MaxDataWidth" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.3 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 位 ") 
</dt> </dl>

可插入此位置的介面卡最大匯流排寬度，以位為單位。 這可以是下列其中一個值。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽資料匯流排寬度** 成員。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

可能的值為。

<dt>

<span id="8"></span>

<span id="8"></span>**8** (0) 


</dt> <dd>

最大資料寬度 (位) ：8

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (1) 


</dt> <dd>

最大資料寬度 (位) ：16

</dd> <dt>

<span id="32"></span>

<span id="32"></span>**32** (2) 


</dt> <dd>

最大資料寬度 (位) ：32

</dd> <dt>

<span id="64"></span>

<span id="64"></span>**64** (3) 


</dt> <dd>

最大資料寬度 (位) ：64

</dd> <dt>

<span id="128"></span>

<span id="128"></span>**128** (4) 


</dt> <dd>

最大資料寬度 (位) ：128

</dd> </dl>

</dd> <dt>

**型號**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

實體元素的名稱。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) 
</dt> </dl>

物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**Number**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可以用來做為系統位置資料表之索引的實體位置編號（不論該位置是否實際是空的）。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽識別碼** 成員。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

其他資料 (也就是可以用來識別實體元素的資產標記資訊) 。 其中一個範例是與也有資產標記的專案相關聯的條碼資料。 請注意，如果只有條碼資料可供使用，而且它是唯一的或可作為專案索引鍵，則這個屬性會是 **Null**，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

生產者或製造商指派給實體元素的元件編號。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PMESignal**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| 插槽特性 2" ) 
</dt> </dl>

若 **為 TRUE**，表示已啟用 PCI 匯流排電源管理 (PME) 信號，此位置會支援此位置。

此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **特性 2** 成員。

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

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-slot.md)位置」。**SpecialPurpose**") 
</dt> </dl>

描述此位置實際是唯一的，且可能保存特殊硬體類型的自由格式字串。 只有當對應的屬性 **SpecialPurpose** 為 **TRUE** 時，這個屬性才有意義。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**SegmentGroupNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Segment Group Number" ) 
</dt> </dl>

SMBIOS 區段群組號碼。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **區段群組編號** 成員。

**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

製造商配置的數位，用來識別實體元素。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

[共用]
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| 插槽特性 1" ) 
</dt> </dl>

若 **為 TRUE**，則會有兩個以上的插槽共用基礎板上的位置，例如 PCI/EISA 共用位置。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽特性 1** 成員。

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

實體元素的 Stockkeeping 單位編號。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**SlotDesignation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| 插槽指定" ) 
</dt> </dl>

SMBIOS 字串，可識別主機板上插槽的系統位置指定。

範例： "PCI-1"

此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **指定** 成員。

</dd> <dt>

**SpecialPurpose**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-slot.md)位置」。**PurposeDescription**") 
</dt> </dl>

若 **為 TRUE**，則此位置實際上是唯一的，而且可能會保存特殊類型的硬體，例如圖形處理器位置。 若 **為 TRUE**，則 **PurposeDescription** 應指定位置唯一性或用途的本質。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

可能的值為。

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

此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **特性 2** 成員。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

由這個類別的實例所表示的系統位置。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

範例：「系統插槽1」

</dd> <dt>

**ThermalRating**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.11 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫瓦 ") 
</dt> </dl>

毫瓦中插槽的最大熱量。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

</dd> <dt>

**VccMixedVoltageSupport**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.9 ") 
</dt> </dl>

列舉整數的陣列，表示此位置所支援的 Vcc 電壓。

此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽特性 1** 成員。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

可能的值為。

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

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
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

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.10 ") 
</dt> </dl>

列舉整數的陣列，表示此位置所支援的 Vpp 電壓。

這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。

可能的值為。

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

**Win32 \_ SystemSlot** 類別衍生自 [**CIM \_ 插槽**](cim-slot.md)。

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

[**CIM \_ 位置**](cim-slot.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
