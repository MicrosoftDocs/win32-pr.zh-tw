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
# <a name="win32_systemslot-class"></a><span data-ttu-id="5ca23-103">Win32 \_ SystemSlot 類別</span><span class="sxs-lookup"><span data-stu-id="5ca23-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="5ca23-104">**Win32 \_ SystemSlot** [WMI 類別](../wmisdk/retrieving-a-class.md)代表實體連接點，包括埠、主機板插槽和週邊設備，以及專屬的連接點。</span><span class="sxs-lookup"><span data-stu-id="5ca23-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="5ca23-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5ca23-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5ca23-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca23-107">語法</span><span class="sxs-lookup"><span data-stu-id="5ca23-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5ca23-108">成員</span><span class="sxs-lookup"><span data-stu-id="5ca23-108">Members</span></span>

<span data-ttu-id="5ca23-109">**Win32 \_ SystemSlot** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5ca23-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="5ca23-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5ca23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ca23-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5ca23-111">Properties</span></span>

<span data-ttu-id="5ca23-112">**Win32 \_ SystemSlot** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ca23-113">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="5ca23-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-116">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Bus Number" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-117">SMBIOS 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="5ca23-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="5ca23-118">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **匯流排編號** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-119">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-120">**標題**</span><span class="sxs-lookup"><span data-stu-id="5ca23-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-123">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-124">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="5ca23-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="5ca23-125">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-126">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="5ca23-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-129">描述 pin 設定的自由格式字串，以及實體連接器的信號使用方式。</span><span class="sxs-lookup"><span data-stu-id="5ca23-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="5ca23-130">這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-131">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="5ca23-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-132">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5ca23-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-134">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "ConnectorType" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| type 9 \| 插槽類型" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-135">此位置使用之連接器的實體屬性陣列。</span><span class="sxs-lookup"><span data-stu-id="5ca23-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="5ca23-136">此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-137">這個屬性繼承自 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="5ca23-138">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="5ca23-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ca23-139">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5ca23-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5ca23-140">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5ca23-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="5ca23-141">**男性** (2) </span><span class="sxs-lookup"><span data-stu-id="5ca23-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="5ca23-142">**女性** (3) </span><span class="sxs-lookup"><span data-stu-id="5ca23-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="5ca23-143">**受防護** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="5ca23-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="5ca23-144">非 **遮罩** (5) </span><span class="sxs-lookup"><span data-stu-id="5ca23-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="5ca23-145">**SCSI () High-Density (50 針腳)** (6) </span><span class="sxs-lookup"><span data-stu-id="5ca23-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="5ca23-146">**SCSI () Low-Density (50 針腳)** (7) </span><span class="sxs-lookup"><span data-stu-id="5ca23-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="5ca23-147">**SCSI (P) High-Density (68 針腳)** (8) </span><span class="sxs-lookup"><span data-stu-id="5ca23-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="5ca23-148">**SCSI SCA-I (80 針腳)** (9) </span><span class="sxs-lookup"><span data-stu-id="5ca23-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="5ca23-149">**SCSI SCA-II (80 針腳)** (10) </span><span class="sxs-lookup"><span data-stu-id="5ca23-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="5ca23-150">**SCSI 光纖通道 (DB-9、銅)** (11) </span><span class="sxs-lookup"><span data-stu-id="5ca23-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="5ca23-151">**SCSI 光纖通道 (光纖)** (12) </span><span class="sxs-lookup"><span data-stu-id="5ca23-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="5ca23-152">**SCSI 光纖通道 SCA-II (40 針腳)** (13) </span><span class="sxs-lookup"><span data-stu-id="5ca23-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="5ca23-153">**SCSI 光纖通道 SCA-II (20 部 pin)** (14) </span><span class="sxs-lookup"><span data-stu-id="5ca23-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="5ca23-154">**SCSI 光纖通道 BNC** (15) </span><span class="sxs-lookup"><span data-stu-id="5ca23-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="5ca23-155">**ATA 3-1/2 英寸 (40 針腳)** (16) </span><span class="sxs-lookup"><span data-stu-id="5ca23-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="5ca23-156">**ATA 2-1/2 英寸 (44 針腳)** (17) </span><span class="sxs-lookup"><span data-stu-id="5ca23-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="5ca23-157">**ATA-2** (18) </span><span class="sxs-lookup"><span data-stu-id="5ca23-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="5ca23-158">**ATA-3** (19) </span><span class="sxs-lookup"><span data-stu-id="5ca23-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="5ca23-159">**ATA/66** (20) </span><span class="sxs-lookup"><span data-stu-id="5ca23-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="5ca23-160">**Db-library** (21) </span><span class="sxs-lookup"><span data-stu-id="5ca23-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="5ca23-161">**DB-15** (22) </span><span class="sxs-lookup"><span data-stu-id="5ca23-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="5ca23-162">**DB-25** (23) </span><span class="sxs-lookup"><span data-stu-id="5ca23-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="5ca23-163">**DB-36** (24) </span><span class="sxs-lookup"><span data-stu-id="5ca23-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="5ca23-164">**Rs-232c** (25) </span><span class="sxs-lookup"><span data-stu-id="5ca23-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="5ca23-165">**RS-422** (26) </span><span class="sxs-lookup"><span data-stu-id="5ca23-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="5ca23-166">**RS-423** (27) </span><span class="sxs-lookup"><span data-stu-id="5ca23-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="5ca23-167">**RS-485** (28) </span><span class="sxs-lookup"><span data-stu-id="5ca23-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="5ca23-168">**RS-449** (29) </span><span class="sxs-lookup"><span data-stu-id="5ca23-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="5ca23-169">**V. 35** (30) </span><span class="sxs-lookup"><span data-stu-id="5ca23-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="5ca23-170">**X. 21** (31) </span><span class="sxs-lookup"><span data-stu-id="5ca23-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="5ca23-171">**IEEE-488** (32) </span><span class="sxs-lookup"><span data-stu-id="5ca23-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="5ca23-172">**AUI** (33) </span><span class="sxs-lookup"><span data-stu-id="5ca23-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="5ca23-173">**UTP 類別 3** (34) </span><span class="sxs-lookup"><span data-stu-id="5ca23-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="5ca23-174">**UTP 類別 4** (35) </span><span class="sxs-lookup"><span data-stu-id="5ca23-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="5ca23-175">**UTP 類別 5** (36) </span><span class="sxs-lookup"><span data-stu-id="5ca23-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="5ca23-176">**BNC** (37) </span><span class="sxs-lookup"><span data-stu-id="5ca23-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="5ca23-177">**RJ11** (38) </span><span class="sxs-lookup"><span data-stu-id="5ca23-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="5ca23-178">**RJ45** (39) </span><span class="sxs-lookup"><span data-stu-id="5ca23-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="5ca23-179">**光纖 MIC** (40) </span><span class="sxs-lookup"><span data-stu-id="5ca23-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="5ca23-180">**APPLE AUI** (41) </span><span class="sxs-lookup"><span data-stu-id="5ca23-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="5ca23-181">**Apple GeoPort** (42) </span><span class="sxs-lookup"><span data-stu-id="5ca23-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="5ca23-182">**PCI** (43) </span><span class="sxs-lookup"><span data-stu-id="5ca23-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="5ca23-183">**ISA** (44) </span><span class="sxs-lookup"><span data-stu-id="5ca23-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="5ca23-184">**EISA** (45) </span><span class="sxs-lookup"><span data-stu-id="5ca23-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="5ca23-185">**VESA** (46) </span><span class="sxs-lookup"><span data-stu-id="5ca23-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="5ca23-186">**PCMCIA** (47) </span><span class="sxs-lookup"><span data-stu-id="5ca23-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="5ca23-187">**PCMCIA 類型 I** (48) </span><span class="sxs-lookup"><span data-stu-id="5ca23-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="5ca23-188">**PCMCIA 類型 II** (49) </span><span class="sxs-lookup"><span data-stu-id="5ca23-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="5ca23-189">**PCMCIA 類型 III** (50) </span><span class="sxs-lookup"><span data-stu-id="5ca23-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="5ca23-190">**ZV 埠** (51) </span><span class="sxs-lookup"><span data-stu-id="5ca23-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="5ca23-191">**CardBus** (52) </span><span class="sxs-lookup"><span data-stu-id="5ca23-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="5ca23-192">**USB** (53) </span><span class="sxs-lookup"><span data-stu-id="5ca23-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="5ca23-193">**IEEE 1394** (54) </span><span class="sxs-lookup"><span data-stu-id="5ca23-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="5ca23-194">**HIPPI** (55) </span><span class="sxs-lookup"><span data-stu-id="5ca23-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="5ca23-195">**HSSDC (6 針腳)** (56) </span><span class="sxs-lookup"><span data-stu-id="5ca23-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="5ca23-196">**GBIC** (57) </span><span class="sxs-lookup"><span data-stu-id="5ca23-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="5ca23-197">**(58**) </span><span class="sxs-lookup"><span data-stu-id="5ca23-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="5ca23-198">**迷你** 等 (59) </span><span class="sxs-lookup"><span data-stu-id="5ca23-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="5ca23-199">**微型** (60) </span><span class="sxs-lookup"><span data-stu-id="5ca23-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="5ca23-200">**PS/2** (61) </span><span class="sxs-lookup"><span data-stu-id="5ca23-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="5ca23-201">**紅外線** (62) </span><span class="sxs-lookup"><span data-stu-id="5ca23-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="5ca23-202">**HP HIL** (63) </span><span class="sxs-lookup"><span data-stu-id="5ca23-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="5ca23-203">**存取. bus** (64) </span><span class="sxs-lookup"><span data-stu-id="5ca23-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="5ca23-204">**NuBus** (65) </span><span class="sxs-lookup"><span data-stu-id="5ca23-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="5ca23-205">**Centronics** (66) </span><span class="sxs-lookup"><span data-stu-id="5ca23-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="5ca23-206">**迷你 Centronics** (67) </span><span class="sxs-lookup"><span data-stu-id="5ca23-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="5ca23-207">**迷你 Centronics 類型-14** (68) </span><span class="sxs-lookup"><span data-stu-id="5ca23-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="5ca23-208">**迷你 Centronics 類型-20** (69) </span><span class="sxs-lookup"><span data-stu-id="5ca23-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="5ca23-209">**迷你 Centronics 類型-26** (70) </span><span class="sxs-lookup"><span data-stu-id="5ca23-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="5ca23-210">**匯流排滑鼠** (71) </span><span class="sxs-lookup"><span data-stu-id="5ca23-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="5ca23-211">**ADB** (72) </span><span class="sxs-lookup"><span data-stu-id="5ca23-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="5ca23-212">**AGP** (73) </span><span class="sxs-lookup"><span data-stu-id="5ca23-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="5ca23-213">**Vm 匯流排** (74) </span><span class="sxs-lookup"><span data-stu-id="5ca23-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="5ca23-214">**VME64** (75) </span><span class="sxs-lookup"><span data-stu-id="5ca23-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="5ca23-215">**專屬** (76) </span><span class="sxs-lookup"><span data-stu-id="5ca23-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="5ca23-216">**專屬處理器卡插槽** (77) </span><span class="sxs-lookup"><span data-stu-id="5ca23-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="5ca23-217">**專屬記憶卡插槽** (78) </span><span class="sxs-lookup"><span data-stu-id="5ca23-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="5ca23-218">**專屬 I/o Riser 卡插槽** (79) </span><span class="sxs-lookup"><span data-stu-id="5ca23-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="5ca23-219">**PCI-66MHZ** (80) </span><span class="sxs-lookup"><span data-stu-id="5ca23-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="5ca23-220">**AGP2X** (81) </span><span class="sxs-lookup"><span data-stu-id="5ca23-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="5ca23-221">**AGP4X** (82) </span><span class="sxs-lookup"><span data-stu-id="5ca23-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="5ca23-222">**PC-98** (83) </span><span class="sxs-lookup"><span data-stu-id="5ca23-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="5ca23-223">**PC-98-Hireso** (84) </span><span class="sxs-lookup"><span data-stu-id="5ca23-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="5ca23-224">**PC-H98** (85) </span><span class="sxs-lookup"><span data-stu-id="5ca23-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="5ca23-225">**PC-98Note** (86) </span><span class="sxs-lookup"><span data-stu-id="5ca23-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="5ca23-226">**PC-98Full** (87) </span><span class="sxs-lookup"><span data-stu-id="5ca23-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="5ca23-227">**PCI-X** (88) </span><span class="sxs-lookup"><span data-stu-id="5ca23-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="5ca23-228">**S 匯流排 IEEE 1396-1993 32 位** (89) </span><span class="sxs-lookup"><span data-stu-id="5ca23-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="5ca23-229">**S 匯流排 IEEE 1396-1993 64 位** (90) </span><span class="sxs-lookup"><span data-stu-id="5ca23-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="5ca23-230">**MCA** (91) </span><span class="sxs-lookup"><span data-stu-id="5ca23-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="5ca23-231">**GIO** (92) </span><span class="sxs-lookup"><span data-stu-id="5ca23-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="5ca23-232">**XIO** (93) </span><span class="sxs-lookup"><span data-stu-id="5ca23-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="5ca23-233">**HIO** (94) </span><span class="sxs-lookup"><span data-stu-id="5ca23-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="5ca23-234">**NGIO** (95) </span><span class="sxs-lookup"><span data-stu-id="5ca23-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="5ca23-235">**PMC** (96) </span><span class="sxs-lookup"><span data-stu-id="5ca23-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="5ca23-236">**未來的 i/o** (97) </span><span class="sxs-lookup"><span data-stu-id="5ca23-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="5ca23-237">**(98**) 的不限</span><span class="sxs-lookup"><span data-stu-id="5ca23-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="5ca23-238">**AGP8X** (99) </span><span class="sxs-lookup"><span data-stu-id="5ca23-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="5ca23-239">**PCI-E** (100) </span><span class="sxs-lookup"><span data-stu-id="5ca23-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ca23-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ca23-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-243">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="5ca23-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-244">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="5ca23-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5ca23-245">搭配類別的其他索引鍵屬性使用時，此屬性可讓您以唯一的方式識別此類別和其子類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="5ca23-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="5ca23-246">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-247">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="5ca23-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-248">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5ca23-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-250">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Current Usage" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-251">系統位置使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="5ca23-251">Status of system slot use.</span></span>

<span data-ttu-id="5ca23-252">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **目前使用** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-253">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="5ca23-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="5ca23-254">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="5ca23-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5ca23-255">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5ca23-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ca23-256">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5ca23-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="5ca23-257">**可用** (3) </span><span class="sxs-lookup"><span data-stu-id="5ca23-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="5ca23-258">**使用** (4) </span><span class="sxs-lookup"><span data-stu-id="5ca23-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ca23-259">**說明**</span><span class="sxs-lookup"><span data-stu-id="5ca23-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-262">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-263">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5ca23-263">Description of the object.</span></span>

<span data-ttu-id="5ca23-264">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-265">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="5ca23-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-266">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-268">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Device Number" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-269">SMBIOS 裝置編號。</span><span class="sxs-lookup"><span data-stu-id="5ca23-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="5ca23-270">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **裝置/** 函式編號成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-271">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-272">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="5ca23-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-275">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Function Number" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-276">SMBIOS 功能編號。</span><span class="sxs-lookup"><span data-stu-id="5ca23-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="5ca23-277">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **裝置/** 函式編號成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-278">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-279">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="5ca23-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-280">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-282">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-283">可以插入至插槽的介面卡卡片最大高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ca23-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="5ca23-284">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5ca23-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-286">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5ca23-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-288">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="5ca23-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-289">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5ca23-289">Date and time the object is installed.</span></span> <span data-ttu-id="5ca23-290">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="5ca23-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5ca23-291">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-292">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="5ca23-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-293">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-295">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-296">可以插入插槽中的介面卡卡片最大長度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ca23-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="5ca23-297">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-298">**製造商**</span><span class="sxs-lookup"><span data-stu-id="5ca23-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-301">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="5ca23-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-302">產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="5ca23-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="5ca23-303">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-304">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="5ca23-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-305">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5ca23-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-307">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "MaxDataWidth" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.3 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 位 ") </span><span class="sxs-lookup"><span data-stu-id="5ca23-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-308">可插入此位置的介面卡最大匯流排寬度，以位為單位。</span><span class="sxs-lookup"><span data-stu-id="5ca23-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="5ca23-309">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5ca23-309">This can be one of the following values.</span></span>

<span data-ttu-id="5ca23-310">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽資料匯流排寬度** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-311">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="5ca23-312">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="5ca23-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="5ca23-313"><span id="8"></span>**8** (0) </span><span class="sxs-lookup"><span data-stu-id="5ca23-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5ca23-314">最大資料寬度 (位) ：8</span><span class="sxs-lookup"><span data-stu-id="5ca23-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="5ca23-315"><span id="16"></span>**16** (1) </span><span class="sxs-lookup"><span data-stu-id="5ca23-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5ca23-316">最大資料寬度 (位) ：16</span><span class="sxs-lookup"><span data-stu-id="5ca23-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="5ca23-317"><span id="32"></span>**32** (2) </span><span class="sxs-lookup"><span data-stu-id="5ca23-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5ca23-318">最大資料寬度 (位) ：32</span><span class="sxs-lookup"><span data-stu-id="5ca23-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="5ca23-319"><span id="64"></span>**64** (3) </span><span class="sxs-lookup"><span data-stu-id="5ca23-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5ca23-320">最大資料寬度 (位) ：64</span><span class="sxs-lookup"><span data-stu-id="5ca23-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="5ca23-321"><span id="128"></span>**128** (4) </span><span class="sxs-lookup"><span data-stu-id="5ca23-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5ca23-322">最大資料寬度 (位) ：128</span><span class="sxs-lookup"><span data-stu-id="5ca23-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ca23-323">**型號**</span><span class="sxs-lookup"><span data-stu-id="5ca23-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-326">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5ca23-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-327">實體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ca23-327">Name for the physical element.</span></span>

<span data-ttu-id="5ca23-328">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-329">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5ca23-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-332">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-333">物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="5ca23-333">Label for the object.</span></span> <span data-ttu-id="5ca23-334">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5ca23-335">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-336">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ca23-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-337">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5ca23-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-339">可以用來做為系統位置資料表之索引的實體位置編號（不論該位置是否實際是空的）。</span><span class="sxs-lookup"><span data-stu-id="5ca23-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="5ca23-340">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽識別碼** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-341">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5ca23-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-345">其他資料 (也就是可以用來識別實體元素的資產標記資訊) 。</span><span class="sxs-lookup"><span data-stu-id="5ca23-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="5ca23-346">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="5ca23-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="5ca23-347">請注意，如果只有條碼資料可供使用，而且它是唯一的或可作為專案索引鍵，則這個屬性會是 **Null**，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="5ca23-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="5ca23-348">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-349">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5ca23-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-352">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="5ca23-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-353">生產者或製造商指派給實體元素的元件編號。</span><span class="sxs-lookup"><span data-stu-id="5ca23-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="5ca23-354">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-355">**PMESignal**</span><span class="sxs-lookup"><span data-stu-id="5ca23-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-356">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ca23-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-358">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| 插槽特性 2" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-359">若 **為 TRUE**，表示已啟用 PCI 匯流排電源管理 (PME) 信號，此位置會支援此位置。</span><span class="sxs-lookup"><span data-stu-id="5ca23-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="5ca23-360">此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **特性 2** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-361">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="5ca23-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-362">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ca23-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-364">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="5ca23-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="5ca23-365">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-366">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="5ca23-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-369">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-slot.md)位置」。**SpecialPurpose**") </span><span class="sxs-lookup"><span data-stu-id="5ca23-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-370">描述此位置實際是唯一的，且可能保存特殊硬體類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="5ca23-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="5ca23-371">只有當對應的屬性 **SpecialPurpose** 為 **TRUE** 時，這個屬性才有意義。</span><span class="sxs-lookup"><span data-stu-id="5ca23-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="5ca23-372">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-373">**SegmentGroupNumber**</span><span class="sxs-lookup"><span data-stu-id="5ca23-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-374">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-376">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| Segment Group Number" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-377">SMBIOS 區段群組號碼。</span><span class="sxs-lookup"><span data-stu-id="5ca23-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="5ca23-378">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **區段群組編號** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-379">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 10 和 Windows Server 2016 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca23-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-380">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5ca23-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-383">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5ca23-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-384">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="5ca23-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5ca23-385">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-386">[共用]</span><span class="sxs-lookup"><span data-stu-id="5ca23-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-387">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ca23-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-389">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| 插槽特性 1" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-390">若 **為 TRUE**，則會有兩個以上的插槽共用基礎板上的位置，例如 PCI/EISA 共用位置。</span><span class="sxs-lookup"><span data-stu-id="5ca23-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="5ca23-391">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽特性 1** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-392">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5ca23-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-393">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-395">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5ca23-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-396">實體元素的 Stockkeeping 單位編號。</span><span class="sxs-lookup"><span data-stu-id="5ca23-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="5ca23-397">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-398">**SlotDesignation**</span><span class="sxs-lookup"><span data-stu-id="5ca23-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-401">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 9 \| 插槽指定" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-402">SMBIOS 字串，可識別主機板上插槽的系統位置指定。</span><span class="sxs-lookup"><span data-stu-id="5ca23-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="5ca23-403">範例： "PCI-1"</span><span class="sxs-lookup"><span data-stu-id="5ca23-403">Example: "PCI-1"</span></span>

<span data-ttu-id="5ca23-404">此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **指定** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-405">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="5ca23-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-406">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ca23-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-408">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-slot.md)位置」。**PurposeDescription**") </span><span class="sxs-lookup"><span data-stu-id="5ca23-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-409">若 **為 TRUE**，則此位置實際上是唯一的，而且可能會保存特殊類型的硬體，例如圖形處理器位置。</span><span class="sxs-lookup"><span data-stu-id="5ca23-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="5ca23-410">若 **為 TRUE**，則 **PurposeDescription** 應指定位置唯一性或用途的本質。</span><span class="sxs-lookup"><span data-stu-id="5ca23-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="5ca23-411">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-412">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5ca23-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-413">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-415">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-416">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5ca23-416">Current status of the object.</span></span> <span data-ttu-id="5ca23-417">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="5ca23-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5ca23-418">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="5ca23-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5ca23-419">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="5ca23-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5ca23-420">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="5ca23-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5ca23-421">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="5ca23-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5ca23-422">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5ca23-423">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="5ca23-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5ca23-424">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5ca23-425">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5ca23-426">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ca23-427">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5ca23-428">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5ca23-429">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5ca23-430">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5ca23-431">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5ca23-432">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5ca23-433">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5ca23-434">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5ca23-435">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ca23-436">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="5ca23-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-437">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ca23-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-439">若 **為 TRUE**，則位置支援介面卡的熱插即用。</span><span class="sxs-lookup"><span data-stu-id="5ca23-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="5ca23-440">此值來自 SMBIOS 資訊中 **系統** 位置結構的位置 **特性 2** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-441">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-442">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5ca23-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-445">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="5ca23-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-446">由這個類別的實例所表示的系統位置。</span><span class="sxs-lookup"><span data-stu-id="5ca23-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="5ca23-447">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="5ca23-448">範例：「系統插槽1」</span><span class="sxs-lookup"><span data-stu-id="5ca23-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-449">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="5ca23-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-450">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ca23-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-452">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.11 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" 毫瓦 ") </span><span class="sxs-lookup"><span data-stu-id="5ca23-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-453">毫瓦中插槽的最大熱量。</span><span class="sxs-lookup"><span data-stu-id="5ca23-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="5ca23-454">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-455">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="5ca23-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-456">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5ca23-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-458">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.9 ") </span><span class="sxs-lookup"><span data-stu-id="5ca23-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-459">列舉整數的陣列，表示此位置所支援的 Vcc 電壓。</span><span class="sxs-lookup"><span data-stu-id="5ca23-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="5ca23-460">此值來自 SMBIOS 資訊中 **系統** 位置結構的 **插槽特性 1** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca23-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5ca23-461">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="5ca23-462">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="5ca23-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ca23-463">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5ca23-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5ca23-464">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5ca23-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="5ca23-465">**3.3 v** (2) </span><span class="sxs-lookup"><span data-stu-id="5ca23-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="5ca23-466">**5v** (3) </span><span class="sxs-lookup"><span data-stu-id="5ca23-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ca23-467">**版本**</span><span class="sxs-lookup"><span data-stu-id="5ca23-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-468">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ca23-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-470">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="5ca23-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-471">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="5ca23-471">Version of the physical element.</span></span>

<span data-ttu-id="5ca23-472">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ca23-473">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="5ca23-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ca23-474">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5ca23-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ca23-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ca23-476">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統插槽 \| 004.10 ") </span><span class="sxs-lookup"><span data-stu-id="5ca23-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="5ca23-477">列舉整數的陣列，表示此位置所支援的 Vpp 電壓。</span><span class="sxs-lookup"><span data-stu-id="5ca23-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="5ca23-478">這個屬性繼承自 [**CIM 位置 \_**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="5ca23-479">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="5ca23-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ca23-480">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5ca23-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5ca23-481">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5ca23-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="5ca23-482">**3.3 v** (2) </span><span class="sxs-lookup"><span data-stu-id="5ca23-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="5ca23-483">**5v** (3) </span><span class="sxs-lookup"><span data-stu-id="5ca23-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="5ca23-484">**12v** (4) </span><span class="sxs-lookup"><span data-stu-id="5ca23-484">**12V** (4)</span></span>


<span data-ttu-id="5ca23-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5ca23-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5ca23-486">備註</span><span class="sxs-lookup"><span data-stu-id="5ca23-486">Remarks</span></span>

<span data-ttu-id="5ca23-487">**Win32 \_ SystemSlot** 類別衍生自 [**CIM \_ 插槽**](cim-slot.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca23-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca23-488">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ca23-488">Requirements</span></span>



| <span data-ttu-id="5ca23-489">需求</span><span class="sxs-lookup"><span data-stu-id="5ca23-489">Requirement</span></span> | <span data-ttu-id="5ca23-490">值</span><span class="sxs-lookup"><span data-stu-id="5ca23-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca23-491">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ca23-491">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca23-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ca23-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ca23-493">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ca23-493">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca23-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ca23-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ca23-495">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ca23-495">Namespace</span></span><br/>                | <span data-ttu-id="5ca23-496">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ca23-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ca23-497">MOF</span><span class="sxs-lookup"><span data-stu-id="5ca23-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ca23-498"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ca23-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ca23-499">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca23-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca23-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca23-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca23-501">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ca23-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca23-502">**CIM \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="5ca23-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="5ca23-503">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="5ca23-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
