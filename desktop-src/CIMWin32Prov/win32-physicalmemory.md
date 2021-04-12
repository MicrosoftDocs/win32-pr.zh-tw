---
description: 代表位於電腦系統上且可供作業系統使用的實體記憶體裝置。
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Win32_PhysicalMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468565"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="ec82d-103">Win32 \_ PhysicalMemory 類別</span><span class="sxs-lookup"><span data-stu-id="ec82d-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="ec82d-104">**Win32 \_ PhysicalMemory** [WMI 類別](../wmisdk/retrieving-a-class.md)代表位於電腦系統上的實體記憶體裝置，並可供作業系統使用。</span><span class="sxs-lookup"><span data-stu-id="ec82d-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="ec82d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ec82d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ec82d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec82d-107">語法</span><span class="sxs-lookup"><span data-stu-id="ec82d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="ec82d-108">成員</span><span class="sxs-lookup"><span data-stu-id="ec82d-108">Members</span></span>

<span data-ttu-id="ec82d-109">**Win32 \_ PhysicalMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec82d-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="ec82d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ec82d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec82d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ec82d-111">Properties</span></span>

<span data-ttu-id="ec82d-112">**Win32 \_ PhysicalMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec82d-113">**屬性**</span><span class="sxs-lookup"><span data-stu-id="ec82d-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-116">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 17 \| Attributes" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-117">SMBIOS 類型 17-屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="ec82d-118">表示排名。</span><span class="sxs-lookup"><span data-stu-id="ec82d-118">Represents the RANK.</span></span>

<span data-ttu-id="ec82d-119">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **屬性** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-120">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-121">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="ec82d-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-124">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 記憶體裝置 \| 002.4」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-125">實際標示的 bank，記憶體所在位置。</span><span class="sxs-lookup"><span data-stu-id="ec82d-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="ec82d-126">範例： "Bank 0"、"Bank A"</span><span class="sxs-lookup"><span data-stu-id="ec82d-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="ec82d-127">此值來自 SMBIOS 資訊中 **記憶體裝置** 結構的 **Bank 定位器** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-128">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-129">**容量**</span><span class="sxs-lookup"><span data-stu-id="ec82d-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-130">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ec82d-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-132">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置 \| 002.5 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="ec82d-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-133">實體記憶體的總容量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ec82d-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="ec82d-134">此值來自 SMBIOS 版本資訊中的 **記憶體設備** 結構。</span><span class="sxs-lookup"><span data-stu-id="ec82d-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="ec82d-135">針對 SMBIOS 版本2.1 到2.6，此值來自 **大小** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="ec82d-136">針對 SMBIOS 2.7 版 +，此值來自于 **擴充的大小** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="ec82d-137">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="ec82d-138">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="ec82d-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-142">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-143">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="ec82d-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="ec82d-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-145">**ConfiguredClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="ec82d-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-148">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| Type 17 \| 設定的記憶體頻率速度」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-149">記憶體裝置的設定頻率速度（以 mhz 為單位），以 MHz (MHz) ，如果速度不明，則為0。</span><span class="sxs-lookup"><span data-stu-id="ec82d-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="ec82d-150">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **已設定記憶體頻率速度** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-151">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-152">**ConfiguredVoltage**</span><span class="sxs-lookup"><span data-stu-id="ec82d-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-155">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| 類型 17 \| 設定的電壓」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-156">此裝置設定的電壓（以毫伏為單位），如果電壓不明，則為0。</span><span class="sxs-lookup"><span data-stu-id="ec82d-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="ec82d-157">此值來自 SMBIOS 資訊中的 **記憶體設備** 結構 **設定的電壓** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-158">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-159">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ec82d-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-162">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="ec82d-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-163">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="ec82d-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ec82d-164">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="ec82d-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="ec82d-165">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="ec82d-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec82d-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-169">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置 \| 002.8 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="ec82d-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-170">實體記憶體的資料寬度，以位為單位。</span><span class="sxs-lookup"><span data-stu-id="ec82d-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="ec82d-171">資料寬度為 0 (零) ，總寬度為 8 (八) 表示記憶體僅供提供錯誤更正位。</span><span class="sxs-lookup"><span data-stu-id="ec82d-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="ec82d-172">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **資料寬度** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-173">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-174">**說明**</span><span class="sxs-lookup"><span data-stu-id="ec82d-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-177">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-178">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ec82d-178">Description of an object.</span></span>

<span data-ttu-id="ec82d-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="ec82d-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-183">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 17 \| Device 定位器" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-184">存放記憶體之通訊端或電路板的標籤。</span><span class="sxs-lookup"><span data-stu-id="ec82d-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="ec82d-185">範例： "SIMM 3"</span><span class="sxs-lookup"><span data-stu-id="ec82d-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="ec82d-186">此值來自 SMBIOS 資訊中 **記憶體裝置** 結構的 **裝置定位器** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-187">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="ec82d-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec82d-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-190">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置 \| 002.6」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-191">晶片的實外型規格。</span><span class="sxs-lookup"><span data-stu-id="ec82d-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="ec82d-192">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **外型規格** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-193">這個屬性繼承自 [**CIM \_ 晶片**](cim-chip.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="ec82d-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="ec82d-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-195">Unknown</span><span class="sxs-lookup"><span data-stu-id="ec82d-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-196">(1)</span><span class="sxs-lookup"><span data-stu-id="ec82d-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-197">其他</span><span class="sxs-lookup"><span data-stu-id="ec82d-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-198">(2)</span><span class="sxs-lookup"><span data-stu-id="ec82d-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-199">Sip</span><span class="sxs-lookup"><span data-stu-id="ec82d-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-200">(3)</span><span class="sxs-lookup"><span data-stu-id="ec82d-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-201">DIP</span><span class="sxs-lookup"><span data-stu-id="ec82d-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-202">(4)</span><span class="sxs-lookup"><span data-stu-id="ec82d-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="ec82d-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-204">(5)</span><span class="sxs-lookup"><span data-stu-id="ec82d-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-205">SOJ</span><span class="sxs-lookup"><span data-stu-id="ec82d-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-206">(6)</span><span class="sxs-lookup"><span data-stu-id="ec82d-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-207">專屬</span><span class="sxs-lookup"><span data-stu-id="ec82d-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-208">(7)</span><span class="sxs-lookup"><span data-stu-id="ec82d-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-209">Simm</span><span class="sxs-lookup"><span data-stu-id="ec82d-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-210">(8)</span><span class="sxs-lookup"><span data-stu-id="ec82d-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-211">Dimm</span><span class="sxs-lookup"><span data-stu-id="ec82d-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-212">(9)</span><span class="sxs-lookup"><span data-stu-id="ec82d-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-213">TSOP</span><span class="sxs-lookup"><span data-stu-id="ec82d-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-214">(10)</span><span class="sxs-lookup"><span data-stu-id="ec82d-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-215">Pga</span><span class="sxs-lookup"><span data-stu-id="ec82d-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-216">(11)</span><span class="sxs-lookup"><span data-stu-id="ec82d-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-217">RIMM</span><span class="sxs-lookup"><span data-stu-id="ec82d-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-218"> (12) </span><span class="sxs-lookup"><span data-stu-id="ec82d-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-219">SODIMM</span><span class="sxs-lookup"><span data-stu-id="ec82d-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-220">(13)</span><span class="sxs-lookup"><span data-stu-id="ec82d-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-221">SRIMM</span><span class="sxs-lookup"><span data-stu-id="ec82d-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-222">(14)</span><span class="sxs-lookup"><span data-stu-id="ec82d-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-223">Smd</span><span class="sxs-lookup"><span data-stu-id="ec82d-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-224">(15)</span><span class="sxs-lookup"><span data-stu-id="ec82d-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-225">SSMP</span><span class="sxs-lookup"><span data-stu-id="ec82d-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-226">(16)</span><span class="sxs-lookup"><span data-stu-id="ec82d-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-227">QFP</span><span class="sxs-lookup"><span data-stu-id="ec82d-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-228">(17)</span><span class="sxs-lookup"><span data-stu-id="ec82d-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-229">TQFP</span><span class="sxs-lookup"><span data-stu-id="ec82d-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-230">(18)</span><span class="sxs-lookup"><span data-stu-id="ec82d-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-231">SOIC</span><span class="sxs-lookup"><span data-stu-id="ec82d-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-232">(19)</span><span class="sxs-lookup"><span data-stu-id="ec82d-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-233">Lcc</span><span class="sxs-lookup"><span data-stu-id="ec82d-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-234">(20)</span><span class="sxs-lookup"><span data-stu-id="ec82d-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-235">PLCC</span><span class="sxs-lookup"><span data-stu-id="ec82d-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-236">(21)</span><span class="sxs-lookup"><span data-stu-id="ec82d-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-237">Bga</span><span class="sxs-lookup"><span data-stu-id="ec82d-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-238">(22)</span><span class="sxs-lookup"><span data-stu-id="ec82d-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-239">FPBGA</span><span class="sxs-lookup"><span data-stu-id="ec82d-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="ec82d-240">(23)</span><span class="sxs-lookup"><span data-stu-id="ec82d-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-241">LGA</span><span class="sxs-lookup"><span data-stu-id="ec82d-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec82d-242">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="ec82d-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-243">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec82d-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-245">若 **為 TRUE**，則會將此實體媒體元件取代為實際不同，但在包含套件已套用電源的情況下，則會使用相同的元件。</span><span class="sxs-lookup"><span data-stu-id="ec82d-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="ec82d-246">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="ec82d-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="ec82d-247">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="ec82d-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="ec82d-248">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ec82d-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-250">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ec82d-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-252">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ec82d-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-253">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ec82d-253">Date and time the object is installed.</span></span> <span data-ttu-id="ec82d-254">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="ec82d-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ec82d-255">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-256">**InterleaveDataDepth**</span><span class="sxs-lookup"><span data-stu-id="ec82d-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec82d-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-259">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 20 \| 交錯資料深度" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-260">不帶正負號的16位整數最大資料列數，可從記憶體裝置以單一交錯傳送的方式存取。</span><span class="sxs-lookup"><span data-stu-id="ec82d-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="ec82d-261">如果此值為 0 (零) ，則不會交錯記憶體。</span><span class="sxs-lookup"><span data-stu-id="ec82d-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-262">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="ec82d-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-263">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-265">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置對應位址 \| 001.7」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-266">實體記憶體在交錯中的位置。</span><span class="sxs-lookup"><span data-stu-id="ec82d-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="ec82d-267">例如，在2:1 交錯時，值為 "1" 表示記憶體是在 "偶數" 位置。</span><span class="sxs-lookup"><span data-stu-id="ec82d-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="ec82d-268">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="ec82d-269">0</span><span class="sxs-lookup"><span data-stu-id="ec82d-269">0</span></span>
</dt> <dd>

<span data-ttu-id="ec82d-270">Noninterleaved</span><span class="sxs-lookup"><span data-stu-id="ec82d-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-271">1</span><span class="sxs-lookup"><span data-stu-id="ec82d-271">1</span></span>
</dt> <dd>

<span data-ttu-id="ec82d-272">第一個位置</span><span class="sxs-lookup"><span data-stu-id="ec82d-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-273">2</span><span class="sxs-lookup"><span data-stu-id="ec82d-273">2</span></span>
</dt> <dd>

<span data-ttu-id="ec82d-274">第二個位置</span><span class="sxs-lookup"><span data-stu-id="ec82d-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec82d-275">**製造商**</span><span class="sxs-lookup"><span data-stu-id="ec82d-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-278">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="ec82d-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-279">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="ec82d-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="ec82d-280">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **製造商** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-281">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-282">**MaxVoltage**</span><span class="sxs-lookup"><span data-stu-id="ec82d-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-285">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 17 \| Maximum 電壓" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-286">此裝置的最大操作電壓（以毫伏為單位）或0（如果電壓不明）。</span><span class="sxs-lookup"><span data-stu-id="ec82d-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="ec82d-287">此值來自 SMBIOS 資訊中 **記憶體裝置** 結構的 **最大電壓** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-288">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-289">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="ec82d-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-290">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec82d-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-292">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置 \| 002.9」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-293">實體記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="ec82d-293">Type of physical memory.</span></span> <span data-ttu-id="ec82d-294">這是對應至 SMBIOS 值的 CIM 值。</span><span class="sxs-lookup"><span data-stu-id="ec82d-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="ec82d-295">**SMBIOSMemoryType** 屬性包含原始的 SMBIOS 記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="ec82d-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="ec82d-296">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **記憶體類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-297">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec82d-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ec82d-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ec82d-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ec82d-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="ec82d-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2) </span><span class="sxs-lookup"><span data-stu-id="ec82d-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="ec82d-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**同步 DRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="ec82d-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="ec82d-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**CACHE DRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="ec82d-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="ec82d-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5) </span><span class="sxs-lookup"><span data-stu-id="ec82d-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="ec82d-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6) </span><span class="sxs-lookup"><span data-stu-id="ec82d-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="ec82d-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7) </span><span class="sxs-lookup"><span data-stu-id="ec82d-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="ec82d-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8) </span><span class="sxs-lookup"><span data-stu-id="ec82d-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="ec82d-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9) </span><span class="sxs-lookup"><span data-stu-id="ec82d-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="ec82d-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10) </span><span class="sxs-lookup"><span data-stu-id="ec82d-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="ec82d-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11) </span><span class="sxs-lookup"><span data-stu-id="ec82d-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="ec82d-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12) </span><span class="sxs-lookup"><span data-stu-id="ec82d-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="ec82d-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13) </span><span class="sxs-lookup"><span data-stu-id="ec82d-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="ec82d-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14) </span><span class="sxs-lookup"><span data-stu-id="ec82d-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="ec82d-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15) </span><span class="sxs-lookup"><span data-stu-id="ec82d-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="ec82d-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16) </span><span class="sxs-lookup"><span data-stu-id="ec82d-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="ec82d-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17) </span><span class="sxs-lookup"><span data-stu-id="ec82d-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="ec82d-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18) </span><span class="sxs-lookup"><span data-stu-id="ec82d-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="ec82d-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19) </span><span class="sxs-lookup"><span data-stu-id="ec82d-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="ec82d-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20) </span><span class="sxs-lookup"><span data-stu-id="ec82d-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="ec82d-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21) </span><span class="sxs-lookup"><span data-stu-id="ec82d-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-320">DDR2 —可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="ec82d-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="ec82d-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22) </span><span class="sxs-lookup"><span data-stu-id="ec82d-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-322">DDR2 —可能無法使用 FB （FB）。</span><span class="sxs-lookup"><span data-stu-id="ec82d-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-323">24</span><span class="sxs-lookup"><span data-stu-id="ec82d-323">24</span></span>
</dt> <dd>

<span data-ttu-id="ec82d-324">DDR3，可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="ec82d-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-325">25</span><span class="sxs-lookup"><span data-stu-id="ec82d-325">25</span></span>
</dt> <dd>

<span data-ttu-id="ec82d-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="ec82d-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="ec82d-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26) </span><span class="sxs-lookup"><span data-stu-id="ec82d-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec82d-328">**MinVoltage**</span><span class="sxs-lookup"><span data-stu-id="ec82d-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-329">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-331">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 20 \| 最小電壓" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-332">此裝置的最小操作電壓（以毫伏為單位）或0（如果電壓不明）。</span><span class="sxs-lookup"><span data-stu-id="ec82d-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="ec82d-333">此值來自 SMBIOS 資訊中 **記憶體裝置** 結構的 **最小電壓** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-334">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-335">**型號**</span><span class="sxs-lookup"><span data-stu-id="ec82d-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-338">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="ec82d-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-339">實體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec82d-339">Name for the physical element.</span></span>

<span data-ttu-id="ec82d-340">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-341">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ec82d-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-344">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-345">物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="ec82d-345">Label for the object.</span></span> <span data-ttu-id="ec82d-346">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="ec82d-347">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ec82d-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-351">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="ec82d-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="ec82d-352">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="ec82d-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="ec82d-353">如果只有條碼資料可用且唯一或可作為專案索引鍵，這個屬性會是 **Null** ，而條碼資料會當做標記屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="ec82d-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="ec82d-354">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-355">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="ec82d-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-358">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="ec82d-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-359">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="ec82d-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="ec82d-360">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **元件編號** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-361">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-362">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="ec82d-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-363">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-365">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置對應位址 \| 001.6」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-366">實體記憶體在資料列中的位置。</span><span class="sxs-lookup"><span data-stu-id="ec82d-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="ec82d-367">例如，如果採用 2 8 位的記憶體裝置來形成16位的資料列，則值為 2 (兩個) 表示這個記憶體是第二個裝置： 0 (零) 是此屬性的無效值。</span><span class="sxs-lookup"><span data-stu-id="ec82d-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="ec82d-368">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-369">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="ec82d-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-370">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec82d-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-372">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="ec82d-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="ec82d-373">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-374">**移動**</span><span class="sxs-lookup"><span data-stu-id="ec82d-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-375">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec82d-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-377">若 **為 TRUE**，就會卸載實體元件 (如果其設計目的是要將它放入和移出通常找到它的實體容器，則不會因而影響整體封裝) 的功能。</span><span class="sxs-lookup"><span data-stu-id="ec82d-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="ec82d-378">如果電源必須是「關閉」以執行移除，則元件仍可卸載。</span><span class="sxs-lookup"><span data-stu-id="ec82d-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="ec82d-379">如果可以「開啟」電源，並移除元件，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="ec82d-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="ec82d-380">例如，可升級的處理器晶片會卸載。</span><span class="sxs-lookup"><span data-stu-id="ec82d-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="ec82d-381">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-382">**更換**</span><span class="sxs-lookup"><span data-stu-id="ec82d-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-383">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec82d-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-385">若 **為 TRUE**，則可將此實體媒體元件取代為實際不同的元件。</span><span class="sxs-lookup"><span data-stu-id="ec82d-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="ec82d-386">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="ec82d-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="ec82d-387">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="ec82d-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="ec82d-388">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="ec82d-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="ec82d-389">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-390">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ec82d-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-393">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="ec82d-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-394">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="ec82d-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="ec82d-395">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **序號** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-396">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-397">**SKU**</span><span class="sxs-lookup"><span data-stu-id="ec82d-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-398">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-400">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="ec82d-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-401">實體元素的庫存單位數。</span><span class="sxs-lookup"><span data-stu-id="ec82d-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="ec82d-402">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-403">**SMBIOSMemoryType**</span><span class="sxs-lookup"><span data-stu-id="ec82d-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-404">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-406">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| type 17 \| Memory \_ type" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-407">原始的 SMBIOS 記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="ec82d-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="ec82d-408">**MemoryType** 屬性的值是對應至 SMBIOS 值的 CIM 值。</span><span class="sxs-lookup"><span data-stu-id="ec82d-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="ec82d-409">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec82d-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-410">**速度**</span><span class="sxs-lookup"><span data-stu-id="ec82d-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-411">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec82d-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-413">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「毫微秒」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-414">實體記憶體的速度（以毫微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ec82d-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="ec82d-415">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **速度** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-416">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-417">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ec82d-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-420">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-421">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ec82d-421">Current status of the object.</span></span> <span data-ttu-id="ec82d-422">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="ec82d-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ec82d-423">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="ec82d-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ec82d-424">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ec82d-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ec82d-425">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="ec82d-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ec82d-426">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ec82d-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ec82d-427">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ec82d-428">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="ec82d-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ec82d-429">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ec82d-430">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ec82d-431">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec82d-432">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ec82d-433">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ec82d-434">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ec82d-435">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ec82d-436">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ec82d-437">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ec82d-438">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ec82d-439">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ec82d-440">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec82d-441">**Tag**</span><span class="sxs-lookup"><span data-stu-id="ec82d-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-444">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-445">**Win32 \_ PhysicalMemory** 實例所代表之實體記憶體裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec82d-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="ec82d-446">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="ec82d-447">範例：「實體記憶體1」</span><span class="sxs-lookup"><span data-stu-id="ec82d-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="ec82d-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-449">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec82d-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-451">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體裝置 \| 002.7 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="ec82d-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-452">實體記憶體的總寬度（以位為單位），包括檢查或錯誤修正位。</span><span class="sxs-lookup"><span data-stu-id="ec82d-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="ec82d-453">如果沒有錯誤更正位，這個屬性中的值應該符合針對 **DataWidth** 屬性所指定的值。</span><span class="sxs-lookup"><span data-stu-id="ec82d-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="ec82d-454">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **總寬度** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="ec82d-455">這個屬性繼承自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec82d-456">**TypeDetail**</span><span class="sxs-lookup"><span data-stu-id="ec82d-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-457">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec82d-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-459">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 17 \| type Detail" ) </span><span class="sxs-lookup"><span data-stu-id="ec82d-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-460">表示的實體記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="ec82d-460">Type of physical memory represented.</span></span>

<span data-ttu-id="ec82d-461">此值來自 SMBIOS 資訊中 **記憶體設備** 結構的 **型別詳細資料** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec82d-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="ec82d-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="ec82d-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ec82d-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (2) </span><span class="sxs-lookup"><span data-stu-id="ec82d-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec82d-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="ec82d-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="ec82d-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**快速分頁** (8) </span><span class="sxs-lookup"><span data-stu-id="ec82d-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="ec82d-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**靜態資料行** (16) </span><span class="sxs-lookup"><span data-stu-id="ec82d-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="ec82d-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**虛擬靜態** (32) </span><span class="sxs-lookup"><span data-stu-id="ec82d-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="ec82d-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64) </span><span class="sxs-lookup"><span data-stu-id="ec82d-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="ec82d-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**同步** (128) </span><span class="sxs-lookup"><span data-stu-id="ec82d-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="ec82d-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256) </span><span class="sxs-lookup"><span data-stu-id="ec82d-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="ec82d-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512) </span><span class="sxs-lookup"><span data-stu-id="ec82d-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="ec82d-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**WINDOWS DRAM** (1024) </span><span class="sxs-lookup"><span data-stu-id="ec82d-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="ec82d-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**CACHE DRAM** (2048) </span><span class="sxs-lookup"><span data-stu-id="ec82d-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="ec82d-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**非暫時性的** (4096) </span><span class="sxs-lookup"><span data-stu-id="ec82d-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="ec82d-475">靜態</span><span class="sxs-lookup"><span data-stu-id="ec82d-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec82d-476">**版本**</span><span class="sxs-lookup"><span data-stu-id="ec82d-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec82d-477">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec82d-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-478">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec82d-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec82d-479">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="ec82d-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec82d-480">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="ec82d-480">Version of the physical element.</span></span>

<span data-ttu-id="ec82d-481">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec82d-482">備註</span><span class="sxs-lookup"><span data-stu-id="ec82d-482">Remarks</span></span>

<span data-ttu-id="ec82d-483">**Win32 \_ PhysicalMemory** 類別衍生自 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="ec82d-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ec82d-484">範例</span><span class="sxs-lookup"><span data-stu-id="ec82d-484">Examples</span></span>

<span data-ttu-id="ec82d-485">[本機/遠端電腦上的 Get-computerinfo 查詢電腦資訊（ (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell 範例（英文）： TechNet 資源庫上的 PowerShell 範例會使用一些硬體和軟體的呼叫，包括 **Win32 \_ PhysicalMemory**，以顯示本機或遠端系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ec82d-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="ec82d-486">TechNet 資源庫上的 [伺服器報表](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell 範例會使用一些硬體和軟體的呼叫，包括 **Win32 \_ PhysicalMemory**，以收集伺服器資訊並在 Word 檔中發佈。</span><span class="sxs-lookup"><span data-stu-id="ec82d-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="ec82d-487">下列 PowerShell 程式碼範例會抓取本機電腦的實體記憶體相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ec82d-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="ec82d-488">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec82d-488">Requirements</span></span>



| <span data-ttu-id="ec82d-489">需求</span><span class="sxs-lookup"><span data-stu-id="ec82d-489">Requirement</span></span> | <span data-ttu-id="ec82d-490">值</span><span class="sxs-lookup"><span data-stu-id="ec82d-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec82d-491">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec82d-491">Minimum supported client</span></span><br/> | <span data-ttu-id="ec82d-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec82d-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec82d-493">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec82d-493">Minimum supported server</span></span><br/> | <span data-ttu-id="ec82d-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec82d-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec82d-495">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec82d-495">Namespace</span></span><br/>                | <span data-ttu-id="ec82d-496">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ec82d-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec82d-497">MOF</span><span class="sxs-lookup"><span data-stu-id="ec82d-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec82d-498"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec82d-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec82d-499">DLL</span><span class="sxs-lookup"><span data-stu-id="ec82d-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec82d-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec82d-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec82d-501">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec82d-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec82d-502">**CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="ec82d-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="ec82d-503">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="ec82d-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
