---
description: Win32 \_ PORTCONNECTOR WMI 類別代表實體連線埠，例如，資料庫-25 針腳男性、Centronics 或 PS/2。
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Win32_PortConnector 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187618"
---
# <a name="win32_portconnector-class"></a><span data-ttu-id="4c2b2-103">Win32 \_ PortConnector 類別</span><span class="sxs-lookup"><span data-stu-id="4c2b2-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="4c2b2-104">**Win32 \_ PortConnector** [WMI 類別](../wmisdk/retrieving-a-class.md)代表實體連線埠，例如，資料庫-25 針腳男性、Centronics 或 PS/2。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="4c2b2-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4c2b2-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c2b2-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c2b2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="4c2b2-108">成員</span><span class="sxs-lookup"><span data-stu-id="4c2b2-108">Members</span></span>

<span data-ttu-id="4c2b2-109">**Win32 \_ PortConnector** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4c2b2-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="4c2b2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4c2b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c2b2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4c2b2-111">Properties</span></span>

<span data-ttu-id="4c2b2-112">**Win32 \_ PortConnector** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c2b2-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-117">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="4c2b2-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-119">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-122">固定設定和使用實體連接器的信號。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="4c2b2-123">這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-124">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-125">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4c2b2-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-127">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "ConnectorType" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 8 \| Internal/External Connector Type" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-128">此埠所使用之連接器的實體屬性陣列。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="4c2b2-129">這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="4c2b2-130">下列清單列出這些值。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c2b2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4c2b2-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="4c2b2-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**男性** (2) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="4c2b2-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**女性** (3) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="4c2b2-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**受防護** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="4c2b2-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>非 **遮罩** (5) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="4c2b2-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI () High-Density (50 針腳)** (6) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="4c2b2-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI () Low-Density (50 針腳)** (7) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="4c2b2-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 針腳)** (8) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="4c2b2-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 針腳)** (9) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="4c2b2-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 針腳)** (10) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="4c2b2-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI 光纖通道 (DB-9、銅)** (11) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="4c2b2-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI 光纖通道 (光纖)** (12) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="4c2b2-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI 光纖通道 SCA-II (40 針腳)** (13) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="4c2b2-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI 光纖通道 SCA-II (20 部 pin)** (14) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="4c2b2-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI 光纖通道 BNC** (15) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="4c2b2-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 英寸 (40 針腳)** (16) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="4c2b2-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 英寸 (44 針腳)** (17) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="4c2b2-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="4c2b2-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="4c2b2-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="4c2b2-152"><span id="DB-9"></span><span id="db-9"></span>**Db-library** (21) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="4c2b2-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="4c2b2-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="4c2b2-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="4c2b2-156"><span id="RS-232C"></span><span id="rs-232c"></span>**Rs-232c** (25) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="4c2b2-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="4c2b2-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="4c2b2-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="4c2b2-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="4c2b2-161"><span id="v.35"></span>**V. 35** (30) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="4c2b2-162"><span id="x.21"></span>**X. 21** (31) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="4c2b2-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="4c2b2-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="4c2b2-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP 類別 3** (34) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="4c2b2-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP 類別 4** (35) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="4c2b2-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP 類別 5** (36) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="4c2b2-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="4c2b2-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="4c2b2-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="4c2b2-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**光纖 MIC** (40) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="4c2b2-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**APPLE AUI** (41) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="4c2b2-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="4c2b2-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="4c2b2-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="4c2b2-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="4c2b2-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="4c2b2-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="4c2b2-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA 類型 I** (48) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="4c2b2-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA 類型 II** (49) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="4c2b2-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA 類型 III** (50) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="4c2b2-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV 埠** (51) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="4c2b2-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="4c2b2-184"><span id="USB"></span><span id="usb"></span>**USB** (53) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="4c2b2-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="4c2b2-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="4c2b2-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 針腳)** (56) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="4c2b2-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="4c2b2-189"><span id="DIN"></span><span id="din"></span>**(58**) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="4c2b2-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**迷你** 等 (59) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="4c2b2-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**微型** (60) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="4c2b2-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="4c2b2-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**紅外線** (62) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="4c2b2-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP HIL** (63) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="4c2b2-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**存取. bus** (64) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="4c2b2-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="4c2b2-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="4c2b2-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**迷你 Centronics** (67) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="4c2b2-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**迷你 Centronics 類型-14** (68) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="4c2b2-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**迷你 Centronics 類型-20** (69) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="4c2b2-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**迷你 Centronics 類型-26** (70) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="4c2b2-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**匯流排滑鼠** (71) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="4c2b2-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="4c2b2-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="4c2b2-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Vm 匯流排** (74) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="4c2b2-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="4c2b2-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**專屬** (76) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="4c2b2-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**專屬處理器卡插槽** (77) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="4c2b2-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**專屬記憶卡插槽** (78) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="4c2b2-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**專屬 I/o Riser 卡插槽** (79) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="4c2b2-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="4c2b2-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="4c2b2-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="4c2b2-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="4c2b2-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-216">電腦-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="4c2b2-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="4c2b2-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="4c2b2-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="4c2b2-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="4c2b2-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**迷你插座** (88) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-221">SSA SCSI</span><span class="sxs-lookup"><span data-stu-id="4c2b2-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="4c2b2-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**在面板上** (89) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-223">圓形</span><span class="sxs-lookup"><span data-stu-id="4c2b2-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="4c2b2-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 釘選雙重內嵌 (pin 10 剪下)** (90) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-225">面板 IDE 連接器</span><span class="sxs-lookup"><span data-stu-id="4c2b2-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="4c2b2-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 個 Pin 雙內嵌 (針腳26剪下)** (91) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-227">在面板上的軟碟連接器</span><span class="sxs-lookup"><span data-stu-id="4c2b2-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="4c2b2-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 釘選雙重內嵌** (92) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-229">9個雙線插換行</span><span class="sxs-lookup"><span data-stu-id="4c2b2-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="4c2b2-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 釘選雙重內嵌** (93) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-231">25個雙內嵌的 Pin</span><span class="sxs-lookup"><span data-stu-id="4c2b2-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="4c2b2-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**從 Cd-rom 輸入的面板音效** (94) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="4c2b2-233">50釘選雙重內嵌</span><span class="sxs-lookup"><span data-stu-id="4c2b2-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-234">95</span><span class="sxs-lookup"><span data-stu-id="4c2b2-234">95</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-235">68釘選雙重內嵌</span><span class="sxs-lookup"><span data-stu-id="4c2b2-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-236">96</span><span class="sxs-lookup"><span data-stu-id="4c2b2-236">96</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-237">面板音效連接器</span><span class="sxs-lookup"><span data-stu-id="4c2b2-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-238">97</span><span class="sxs-lookup"><span data-stu-id="4c2b2-238">97</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="4c2b2-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-240">98</span><span class="sxs-lookup"><span data-stu-id="4c2b2-240">98</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-241">PCI X</span><span class="sxs-lookup"><span data-stu-id="4c2b2-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-242">99</span><span class="sxs-lookup"><span data-stu-id="4c2b2-242">99</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-243">S 匯流排 IEEE 1396-1993 32 位</span><span class="sxs-lookup"><span data-stu-id="4c2b2-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-244">100</span><span class="sxs-lookup"><span data-stu-id="4c2b2-244">100</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-245">S 匯流排 IEEE 1396-1993 64 位</span><span class="sxs-lookup"><span data-stu-id="4c2b2-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-246">101</span><span class="sxs-lookup"><span data-stu-id="4c2b2-246">101</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-247">MCA</span><span class="sxs-lookup"><span data-stu-id="4c2b2-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-248">102</span><span class="sxs-lookup"><span data-stu-id="4c2b2-248">102</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-249">喬</span><span class="sxs-lookup"><span data-stu-id="4c2b2-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-250">103</span><span class="sxs-lookup"><span data-stu-id="4c2b2-250">103</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-251">XIO</span><span class="sxs-lookup"><span data-stu-id="4c2b2-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-252">104</span><span class="sxs-lookup"><span data-stu-id="4c2b2-252">104</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-253">HIO</span><span class="sxs-lookup"><span data-stu-id="4c2b2-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-254">105</span><span class="sxs-lookup"><span data-stu-id="4c2b2-254">105</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-255">NGIO</span><span class="sxs-lookup"><span data-stu-id="4c2b2-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-256">106</span><span class="sxs-lookup"><span data-stu-id="4c2b2-256">106</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-257">PMC</span><span class="sxs-lookup"><span data-stu-id="4c2b2-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-258">107</span><span class="sxs-lookup"><span data-stu-id="4c2b2-258">107</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-259">MTRJ</span><span class="sxs-lookup"><span data-stu-id="4c2b2-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-260">108</span><span class="sxs-lookup"><span data-stu-id="4c2b2-260">108</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-261">VF-45</span><span class="sxs-lookup"><span data-stu-id="4c2b2-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-262">109</span><span class="sxs-lookup"><span data-stu-id="4c2b2-262">109</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-263">未來的 i/o</span><span class="sxs-lookup"><span data-stu-id="4c2b2-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-264">110</span><span class="sxs-lookup"><span data-stu-id="4c2b2-264">110</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-265">SC</span><span class="sxs-lookup"><span data-stu-id="4c2b2-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-266">111</span><span class="sxs-lookup"><span data-stu-id="4c2b2-266">111</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-267">SG</span><span class="sxs-lookup"><span data-stu-id="4c2b2-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-268">112</span><span class="sxs-lookup"><span data-stu-id="4c2b2-268">112</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-269">電子</span><span class="sxs-lookup"><span data-stu-id="4c2b2-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-270">113</span><span class="sxs-lookup"><span data-stu-id="4c2b2-270">113</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-271">光學</span><span class="sxs-lookup"><span data-stu-id="4c2b2-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-272">114</span><span class="sxs-lookup"><span data-stu-id="4c2b2-272">114</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-273">功能區</span><span class="sxs-lookup"><span data-stu-id="4c2b2-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-274">115</span><span class="sxs-lookup"><span data-stu-id="4c2b2-274">115</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-275">GLM</span><span class="sxs-lookup"><span data-stu-id="4c2b2-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-276">116</span><span class="sxs-lookup"><span data-stu-id="4c2b2-276">116</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-277">1x9</span><span class="sxs-lookup"><span data-stu-id="4c2b2-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-278">117</span><span class="sxs-lookup"><span data-stu-id="4c2b2-278">117</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-279">小 SG</span><span class="sxs-lookup"><span data-stu-id="4c2b2-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-280">118</span><span class="sxs-lookup"><span data-stu-id="4c2b2-280">118</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-281">LC</span><span class="sxs-lookup"><span data-stu-id="4c2b2-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-282">119</span><span class="sxs-lookup"><span data-stu-id="4c2b2-282">119</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-283">HSSC</span><span class="sxs-lookup"><span data-stu-id="4c2b2-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-284">120</span><span class="sxs-lookup"><span data-stu-id="4c2b2-284">120</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-285">VHDCI 防護 (68 pin) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-286">121</span><span class="sxs-lookup"><span data-stu-id="4c2b2-286">121</span></span>
</dt> <dd>

<span data-ttu-id="4c2b2-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="4c2b2-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4c2b2-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-291">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-292">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4c2b2-293">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="4c2b2-294">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-295">**說明**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-296">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-298">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-299">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-299">Description of the object.</span></span>

<span data-ttu-id="4c2b2-300">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-301">**ExternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-304">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 8 \| External Reference 指示項" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-305">埠的外部參考指示項。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-305">External reference designator of the port.</span></span> <span data-ttu-id="4c2b2-306">外部參考指示項是決定埠類型和使用的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="4c2b2-307">範例： "COM1"</span><span class="sxs-lookup"><span data-stu-id="4c2b2-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-309">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-311">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4c2b2-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-312">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-312">Date and time the object is installed.</span></span> <span data-ttu-id="4c2b2-313">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4c2b2-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-315">**InternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-318">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| 類型 8 \| 內部參考指示項」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-319">埠的內部參考指示項。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-319">Internal reference designator of the port.</span></span> <span data-ttu-id="4c2b2-320">內部參考指示項是製造商專屬的，而且會識別電路板位置或埠的使用。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="4c2b2-321">範例： "J101"</span><span class="sxs-lookup"><span data-stu-id="4c2b2-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-322">**製造商**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-325">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-326">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="4c2b2-327">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-328">**型號**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-331">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-332">實體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-332">Name for the physical element.</span></span>

<span data-ttu-id="4c2b2-333">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-334">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-335">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-337">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-338">物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-338">Label for the object.</span></span> <span data-ttu-id="4c2b2-339">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="4c2b2-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-344">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="4c2b2-345">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="4c2b2-346">如果只有條碼資料可用且唯一或可作為專案索引鍵，則此屬性為 **Null** ，而條碼資料會當做標記屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="4c2b2-347">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-348">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-351">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-352">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="4c2b2-353">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-354">**PortType**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-355">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-357">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 8 \| Port type" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-358">埠的函式。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-358">Function of the port.</span></span> <span data-ttu-id="4c2b2-359">下列清單列出這些值。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="4c2b2-360">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-361">**平行埠 XT/相容** (1) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="4c2b2-362">**平行埠 PS/2** (2) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="4c2b2-363">**平行埠 ECP** (3) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="4c2b2-364">**平行埠 EPP** (4) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="4c2b2-365">**平行埠 ECP/EPP** (5) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-366">**序列埠 XT/相容** (6) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-367">**序列埠16450相容** (7) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-368">**序列埠16550相容** (8) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-369">**序列埠16550A 相容** (9) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="4c2b2-370">**SCSI 埠** (10) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="4c2b2-371">**MIDI 埠** (11) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="4c2b2-372">**歡樂杆埠** (12) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="4c2b2-373">**鍵盤埠** (13) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="4c2b2-374">**滑鼠連接埠** (14) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="4c2b2-375">**SSA SCSI** (15) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="4c2b2-376">**USB** (16) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="4c2b2-377">**FireWire (IEEE P1394)** (17) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="4c2b2-378">**PCMCIA 類型 II** (18) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="4c2b2-379">**PCMCIA 類型 II** (19) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="4c2b2-380">**PCMCIA 類型 III** (20) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="4c2b2-381">**Cardbus** (21) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="4c2b2-382">**存取匯流排埠** (22) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="4c2b2-383">**SCSI II** (23) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="4c2b2-384">**SCSI Wide** (24) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="4c2b2-385">**電腦-98** (25) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="4c2b2-386">**PC-98-Hireso** (26) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="4c2b2-387">**PC-H98** (27) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="4c2b2-388">**影片埠** (28) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="4c2b2-389">**音訊埠** (29) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="4c2b2-390">**數據機埠** (30) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="4c2b2-391">**網路埠** (31) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-392">**8251 相容** (32) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="4c2b2-393">**8251 FIFO 相容** (33) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4c2b2-394">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-395">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-397">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="4c2b2-398">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-399">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-402">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-403">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="4c2b2-404">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-405">**SKU**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-406">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-408">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-409">實體元素的庫存單位數。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="4c2b2-410">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-411">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-414">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-415">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-415">Current status of the object.</span></span> <span data-ttu-id="4c2b2-416">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4c2b2-417">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4c2b2-418">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4c2b2-419">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4c2b2-420">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4c2b2-421">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4c2b2-422">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4c2b2-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4c2b2-423">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4c2b2-424">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4c2b2-425">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c2b2-426">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4c2b2-427">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4c2b2-428">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4c2b2-429">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4c2b2-430">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4c2b2-431">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4c2b2-432">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4c2b2-433">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4c2b2-434">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4c2b2-435">**Tag**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-438">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-439">電腦系統上端口連接的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="4c2b2-440">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="4c2b2-441">範例：「埠連接器1」</span><span class="sxs-lookup"><span data-stu-id="4c2b2-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="4c2b2-442">**版本**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c2b2-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c2b2-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c2b2-445">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="4c2b2-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c2b2-446">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-446">Version of the physical element.</span></span>

<span data-ttu-id="4c2b2-447">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c2b2-448">備註</span><span class="sxs-lookup"><span data-stu-id="4c2b2-448">Remarks</span></span>

<span data-ttu-id="4c2b2-449">**Win32 \_ PortConnector** 類別衍生自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="4c2b2-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c2b2-450">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c2b2-450">Requirements</span></span>



| <span data-ttu-id="4c2b2-451">需求</span><span class="sxs-lookup"><span data-stu-id="4c2b2-451">Requirement</span></span> | <span data-ttu-id="4c2b2-452">值</span><span class="sxs-lookup"><span data-stu-id="4c2b2-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2b2-453">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c2b2-453">Minimum supported client</span></span><br/> | <span data-ttu-id="4c2b2-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c2b2-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c2b2-455">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c2b2-455">Minimum supported server</span></span><br/> | <span data-ttu-id="4c2b2-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c2b2-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c2b2-457">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c2b2-457">Namespace</span></span><br/>                | <span data-ttu-id="4c2b2-458">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4c2b2-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c2b2-459">MOF</span><span class="sxs-lookup"><span data-stu-id="4c2b2-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c2b2-460"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c2b2-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c2b2-461">DLL</span><span class="sxs-lookup"><span data-stu-id="4c2b2-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c2b2-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c2b2-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c2b2-463">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c2b2-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2b2-464">**CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="4c2b2-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="4c2b2-465">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4c2b2-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
