---
description: Win32 \_ PhysicalMemoryArray&\# 160;WMI 類別代表電腦系統實體記憶體的詳細資料。 這包括記憶體裝置數目、可用記憶體容量，以及記憶體類型&\# 郵件; 例如，系統或視訊記憶體。
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryArray 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936516"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="24b49-104">Win32 \_ PhysicalMemoryArray 類別</span><span class="sxs-lookup"><span data-stu-id="24b49-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="24b49-105">**Win32 \_ PhysicalMemoryArray** [WMI 類別](../wmisdk/retrieving-a-class.md)代表電腦系統實體記憶體的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="24b49-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="24b49-106">這包括記憶體裝置數目、可用的記憶體容量，以及記憶體類型，例如系統或視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="24b49-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="24b49-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="24b49-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="24b49-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="24b49-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b49-109">語法</span><span class="sxs-lookup"><span data-stu-id="24b49-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="24b49-110">成員</span><span class="sxs-lookup"><span data-stu-id="24b49-110">Members</span></span>

<span data-ttu-id="24b49-111">**Win32 \_ PhysicalMemoryArray** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24b49-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="24b49-112">方法</span><span class="sxs-lookup"><span data-stu-id="24b49-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="24b49-113">屬性</span><span class="sxs-lookup"><span data-stu-id="24b49-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24b49-114">方法</span><span class="sxs-lookup"><span data-stu-id="24b49-114">Methods</span></span>

<span data-ttu-id="24b49-115">**Win32 \_ PhysicalMemoryArray** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="24b49-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="24b49-116">方法</span><span class="sxs-lookup"><span data-stu-id="24b49-116">Method</span></span>           | <span data-ttu-id="24b49-117">描述</span><span class="sxs-lookup"><span data-stu-id="24b49-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="24b49-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="24b49-118">**IsCompatible**</span></span> | <span data-ttu-id="24b49-119">未實作。</span><span class="sxs-lookup"><span data-stu-id="24b49-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="24b49-120">屬性</span><span class="sxs-lookup"><span data-stu-id="24b49-120">Properties</span></span>

<span data-ttu-id="24b49-121">**Win32 \_ PhysicalMemoryArray** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="24b49-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24b49-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="24b49-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-125">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-126">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="24b49-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="24b49-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-128">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="24b49-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-131">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="24b49-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-132">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="24b49-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="24b49-133">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="24b49-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="24b49-134">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-135">**深度**</span><span class="sxs-lookup"><span data-stu-id="24b49-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-136">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="24b49-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-138">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-139">實體封裝的深度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="24b49-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="24b49-140">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-141">**說明**</span><span class="sxs-lookup"><span data-stu-id="24b49-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-144">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-145">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="24b49-145">Description of the object.</span></span>

<span data-ttu-id="24b49-146">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-147">**高度**</span><span class="sxs-lookup"><span data-stu-id="24b49-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-148">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="24b49-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-150">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-151">實體封裝的高度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="24b49-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="24b49-152">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-153">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="24b49-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-154">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24b49-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24b49-156">若為 **TRUE**，實體封裝可進行熱交換 (如果可以使用實體不同的元素來取代元素，但在包含套件已套用電源的情況下，則是「開啟」 ) 。</span><span class="sxs-lookup"><span data-stu-id="24b49-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="24b49-157">例如，使用 SCA 連接器插入的磁片磁碟機套件會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="24b49-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="24b49-158">所有可以熱交換的封裝，本質上都是卸載且可取代的。</span><span class="sxs-lookup"><span data-stu-id="24b49-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="24b49-159">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="24b49-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-161">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="24b49-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-163">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="24b49-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-164">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="24b49-164">Date and time the object was installed.</span></span> <span data-ttu-id="24b49-165">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="24b49-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="24b49-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-167">**位置**</span><span class="sxs-lookup"><span data-stu-id="24b49-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24b49-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-170">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 16 \| Location" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-171">記憶體陣列的實體位置。</span><span class="sxs-lookup"><span data-stu-id="24b49-171">Physical location of the memory array.</span></span>

<span data-ttu-id="24b49-172">此值來自 SMBIOS 資訊中 **實體記憶體陣列** 結構的 **位置** 成員。</span><span class="sxs-lookup"><span data-stu-id="24b49-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="24b49-173">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="24b49-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24b49-174">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="24b49-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24b49-175">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="24b49-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="24b49-176">**System 電路板或主機板** (3) </span><span class="sxs-lookup"><span data-stu-id="24b49-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-177">**ISA 附加元件卡** (4) </span><span class="sxs-lookup"><span data-stu-id="24b49-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-178">**EISA 附加元件卡** (5) </span><span class="sxs-lookup"><span data-stu-id="24b49-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-179">**PCI 附加元件卡** (6) </span><span class="sxs-lookup"><span data-stu-id="24b49-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-180">**MCA 附加元件卡片** (7) </span><span class="sxs-lookup"><span data-stu-id="24b49-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-181"> (8) **的 PCMCIA 附加元件卡片**</span><span class="sxs-lookup"><span data-stu-id="24b49-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-182">**專屬附加元件卡片** (9) </span><span class="sxs-lookup"><span data-stu-id="24b49-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="24b49-183">**NuBus** (10) </span><span class="sxs-lookup"><span data-stu-id="24b49-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-184">**電腦-98/C20 附加元件卡** (11) </span><span class="sxs-lookup"><span data-stu-id="24b49-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-185">**電腦-98/C24 附加元件卡** (12) </span><span class="sxs-lookup"><span data-stu-id="24b49-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-186">**電腦-98/E 附加元件卡片** (13) </span><span class="sxs-lookup"><span data-stu-id="24b49-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="24b49-187">**電腦-98/本機匯流排附加元件卡** (14) </span><span class="sxs-lookup"><span data-stu-id="24b49-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24b49-188">**製造商**</span><span class="sxs-lookup"><span data-stu-id="24b49-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-191">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="24b49-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-192">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="24b49-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="24b49-193">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="24b49-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-195">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="24b49-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-197">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 16 \| 容量上限" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-198">請改用 **MaxCapacityEx** 屬性。</span><span class="sxs-lookup"><span data-stu-id="24b49-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="24b49-199">此值來自 SMBIOS 資訊中 **實體記憶體陣列** 結構的 **最大容量** 成員。</span><span class="sxs-lookup"><span data-stu-id="24b49-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="24b49-200">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 記憶體大小上限 (以位元組為單位）) 可安裝此特定記憶體陣列。</span><span class="sxs-lookup"><span data-stu-id="24b49-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="24b49-201">如果大小未知，就會將屬性的值指定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="24b49-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-202">**MaxCapacityEx**</span><span class="sxs-lookup"><span data-stu-id="24b49-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-203">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24b49-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-205">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| 類型 16 \| 擴充的最大容量」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-206">記憶體大小上限 (（以 kb 為單位）) 可安裝此特定記憶體陣列。</span><span class="sxs-lookup"><span data-stu-id="24b49-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="24b49-207">如果大小未知，就會將屬性的值指定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="24b49-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="24b49-208">此值來自 SMBIOS 資訊中 **實體記憶體陣列** 結構的 **延伸最大容量** 成員。</span><span class="sxs-lookup"><span data-stu-id="24b49-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="24b49-209">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="24b49-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="24b49-210">**MemoryDevices**</span><span class="sxs-lookup"><span data-stu-id="24b49-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24b49-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-213">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 16 \| Number of Memory Devices" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-214">此記憶體陣列中可用的實體插槽或通訊端數目。</span><span class="sxs-lookup"><span data-stu-id="24b49-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="24b49-215">此值來自 SMBIOS 資訊中 **實體記憶體陣列** 結構的 **記憶體裝置成員數目**。</span><span class="sxs-lookup"><span data-stu-id="24b49-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="24b49-216">**MemoryErrorCorrection**</span><span class="sxs-lookup"><span data-stu-id="24b49-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-217">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24b49-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-219">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 16 \| Memory Error 矯正" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-220">記憶體陣列所使用的錯誤更正類型。</span><span class="sxs-lookup"><span data-stu-id="24b49-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="24b49-221">此值來自 SMBIOS 資訊中 **實體記憶體陣列** 結構的 **記憶體錯誤更正** 成員。</span><span class="sxs-lookup"><span data-stu-id="24b49-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="24b49-222">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="24b49-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24b49-223">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="24b49-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24b49-224">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="24b49-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="24b49-225">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="24b49-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="24b49-226">同 **位 (4**) </span><span class="sxs-lookup"><span data-stu-id="24b49-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="24b49-227">**單一位 ECC** (5) </span><span class="sxs-lookup"><span data-stu-id="24b49-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="24b49-228">**多位 ECC** (6) </span><span class="sxs-lookup"><span data-stu-id="24b49-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="24b49-229">**CRC** (7) </span><span class="sxs-lookup"><span data-stu-id="24b49-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24b49-230">**型號**</span><span class="sxs-lookup"><span data-stu-id="24b49-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-233">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="24b49-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-234">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b49-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="24b49-235">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-236">**名稱**</span><span class="sxs-lookup"><span data-stu-id="24b49-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-239">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-240">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="24b49-240">Label by which the object is known.</span></span> <span data-ttu-id="24b49-241">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="24b49-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="24b49-242">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="24b49-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24b49-246">其他資料，除了資產標記資訊之外，還可以用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="24b49-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="24b49-247">其中一個範例是與也有資產標記的專案相關聯的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="24b49-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="24b49-248">請注意，如果只有條碼資料可供使用，而且是唯一的或可作為專案索引鍵，則在 tag 屬性中，此屬性會是 **Null** 和用來當做類別索引鍵的條碼資料。</span><span class="sxs-lookup"><span data-stu-id="24b49-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="24b49-249">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-250">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="24b49-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-253">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="24b49-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-254">負責產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="24b49-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="24b49-255">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-256">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="24b49-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-257">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24b49-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24b49-259">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="24b49-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="24b49-260">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-261">**移動**</span><span class="sxs-lookup"><span data-stu-id="24b49-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-262">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24b49-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24b49-264">若 **為 TRUE**，就會卸載實體封裝 (如果它是設計成要在通常找到它的實體容器中取出，則不會因而影響整體封裝) 的功能。</span><span class="sxs-lookup"><span data-stu-id="24b49-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="24b49-265">如果電源必須是「關閉」以執行移除，則套件仍可以卸載。</span><span class="sxs-lookup"><span data-stu-id="24b49-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="24b49-266">如果可以「開啟」電源，並移除該封裝，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="24b49-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="24b49-267">例如，膝上型電腦中的額外電池會卸載，也就是使用 SCA 連接器插入的磁片磁碟機套件。</span><span class="sxs-lookup"><span data-stu-id="24b49-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="24b49-268">不過，後者可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="24b49-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="24b49-269">膝上型電腦的顯示器不是可移動的，也不是 nonredundant 電源供應器。</span><span class="sxs-lookup"><span data-stu-id="24b49-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="24b49-270">移除這些元件會影響整體封裝的功能，或由於封裝的緊密整合而無法進行。</span><span class="sxs-lookup"><span data-stu-id="24b49-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="24b49-271">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-272">**更換**</span><span class="sxs-lookup"><span data-stu-id="24b49-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-273">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24b49-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24b49-275">若 **為 TRUE**，則可將此實體媒體元件取代為實際不同的元件。</span><span class="sxs-lookup"><span data-stu-id="24b49-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="24b49-276">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="24b49-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="24b49-277">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="24b49-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="24b49-278">另一個範例是掛接在滑動滑軌上的電源供應器套件。</span><span class="sxs-lookup"><span data-stu-id="24b49-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="24b49-279">所有卸載式套件本質上都是可取代的。</span><span class="sxs-lookup"><span data-stu-id="24b49-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="24b49-280">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-281">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="24b49-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-284">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="24b49-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-285">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="24b49-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="24b49-286">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-287">**SKU**</span><span class="sxs-lookup"><span data-stu-id="24b49-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-290">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="24b49-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-291">實體元素的 Stockkeeping 單位編號。</span><span class="sxs-lookup"><span data-stu-id="24b49-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="24b49-292">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-293">**狀態**</span><span class="sxs-lookup"><span data-stu-id="24b49-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-296">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-297">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="24b49-297">Current status of the object.</span></span> <span data-ttu-id="24b49-298">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="24b49-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="24b49-299">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="24b49-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="24b49-300">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="24b49-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="24b49-301">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="24b49-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="24b49-302">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="24b49-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="24b49-303">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="24b49-304">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="24b49-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="24b49-305">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="24b49-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="24b49-306">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="24b49-307">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24b49-308">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="24b49-309">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="24b49-310">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="24b49-311">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="24b49-312">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="24b49-313">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="24b49-314">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="24b49-315">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="24b49-316">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24b49-317">**Tag**</span><span class="sxs-lookup"><span data-stu-id="24b49-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-320">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Tag" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-321">實體記憶體陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="24b49-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="24b49-322">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="24b49-323">範例：「實體記憶體陣列1」</span><span class="sxs-lookup"><span data-stu-id="24b49-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="24b49-324">**使用**</span><span class="sxs-lookup"><span data-stu-id="24b49-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-325">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24b49-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-327">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 16 \| Use" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-328">電腦系統中使用記憶體的方式。</span><span class="sxs-lookup"><span data-stu-id="24b49-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="24b49-329">此值來自 SMBIOS 資訊中 **實體記憶體陣列** 結構的 **使用** 成員。</span><span class="sxs-lookup"><span data-stu-id="24b49-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="24b49-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="24b49-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24b49-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="24b49-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24b49-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="24b49-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="24b49-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**系統記憶體** (3) </span><span class="sxs-lookup"><span data-stu-id="24b49-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="24b49-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**視訊記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="24b49-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="24b49-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5) </span><span class="sxs-lookup"><span data-stu-id="24b49-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="24b49-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**非暫時性 RAM** (6) </span><span class="sxs-lookup"><span data-stu-id="24b49-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="24b49-337">非靜態 RAM</span><span class="sxs-lookup"><span data-stu-id="24b49-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="24b49-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7) </span><span class="sxs-lookup"><span data-stu-id="24b49-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24b49-339">**版本**</span><span class="sxs-lookup"><span data-stu-id="24b49-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24b49-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-342">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="24b49-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="24b49-343">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="24b49-343">Version of the physical element.</span></span>

<span data-ttu-id="24b49-344">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-345">**Weight**</span><span class="sxs-lookup"><span data-stu-id="24b49-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-346">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="24b49-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-348">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「磅」 ) </span><span class="sxs-lookup"><span data-stu-id="24b49-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-349">實體套件的加權（以磅為單位）。</span><span class="sxs-lookup"><span data-stu-id="24b49-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="24b49-350">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="24b49-351">**寬度**</span><span class="sxs-lookup"><span data-stu-id="24b49-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24b49-352">資料類型： **real32**</span><span class="sxs-lookup"><span data-stu-id="24b49-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="24b49-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24b49-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24b49-354">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "英寸" ) </span><span class="sxs-lookup"><span data-stu-id="24b49-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="24b49-355">實體套件的寬度（以英寸為單位）。</span><span class="sxs-lookup"><span data-stu-id="24b49-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="24b49-356">這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24b49-357">備註</span><span class="sxs-lookup"><span data-stu-id="24b49-357">Remarks</span></span>

<span data-ttu-id="24b49-358">**Win32 \_ PhysicalMemoryArray** 類別衍生自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="24b49-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="24b49-359">範例</span><span class="sxs-lookup"><span data-stu-id="24b49-359">Examples</span></span>

<span data-ttu-id="24b49-360">下列 PowerShell 範例會抓取目的電腦上所安裝的記憶體插槽數目和記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="24b49-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="24b49-361">下列 VBScript 程式碼範例會傳回電腦上所安裝之實體記憶體的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24b49-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="24b49-362">規格需求</span><span class="sxs-lookup"><span data-stu-id="24b49-362">Requirements</span></span>



| <span data-ttu-id="24b49-363">需求</span><span class="sxs-lookup"><span data-stu-id="24b49-363">Requirement</span></span> | <span data-ttu-id="24b49-364">值</span><span class="sxs-lookup"><span data-stu-id="24b49-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24b49-365">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24b49-365">Minimum supported client</span></span><br/> | <span data-ttu-id="24b49-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24b49-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24b49-367">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24b49-367">Minimum supported server</span></span><br/> | <span data-ttu-id="24b49-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24b49-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24b49-369">命名空間</span><span class="sxs-lookup"><span data-stu-id="24b49-369">Namespace</span></span><br/>                | <span data-ttu-id="24b49-370">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24b49-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24b49-371">MOF</span><span class="sxs-lookup"><span data-stu-id="24b49-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24b49-372"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="24b49-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24b49-373">DLL</span><span class="sxs-lookup"><span data-stu-id="24b49-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24b49-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24b49-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b49-375">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24b49-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b49-376">**CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="24b49-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="24b49-377">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="24b49-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="24b49-378">**Win32 \_ MemoryArrayLocation**</span><span class="sxs-lookup"><span data-stu-id="24b49-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 
