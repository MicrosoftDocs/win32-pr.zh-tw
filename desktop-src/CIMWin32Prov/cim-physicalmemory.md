---
description: CIM \_ PhysicalMemory 類別代表低層級的記憶體裝置，例如 simm、dimm、原始記憶體晶片等等。
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: CIM_PhysicalMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847499"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="4f085-103">CIM \_ PhysicalMemory 類別</span><span class="sxs-lookup"><span data-stu-id="4f085-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="4f085-104">**CIM \_ PhysicalMemory** 類別代表低層級的記憶體裝置，例如 simm、dimm、原始記憶體晶片等等。</span><span class="sxs-lookup"><span data-stu-id="4f085-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f085-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4f085-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4f085-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4f085-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4f085-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4f085-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4f085-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4f085-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f085-109">語法</span><span class="sxs-lookup"><span data-stu-id="4f085-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
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
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="4f085-110">成員</span><span class="sxs-lookup"><span data-stu-id="4f085-110">Members</span></span>

<span data-ttu-id="4f085-111">**CIM \_ PhysicalMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f085-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="4f085-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4f085-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f085-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4f085-113">Properties</span></span>

<span data-ttu-id="4f085-114">**CIM \_ PhysicalMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4f085-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f085-115">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="4f085-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 002.4」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-119">記憶體所在的標記 bank。</span><span class="sxs-lookup"><span data-stu-id="4f085-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="4f085-120">例如，"Bank 0" 或 "Bank A"。</span><span class="sxs-lookup"><span data-stu-id="4f085-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="4f085-121">**容量**</span><span class="sxs-lookup"><span data-stu-id="4f085-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-122">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4f085-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-124">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.5 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="4f085-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-125">實體記憶體的總容量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4f085-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="4f085-126">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4f085-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-127">**標題**</span><span class="sxs-lookup"><span data-stu-id="4f085-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-130">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4f085-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-131">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4f085-131">Short textual description of the object.</span></span>

<span data-ttu-id="4f085-132">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4f085-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-136">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="4f085-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-137">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f085-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4f085-138">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4f085-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4f085-139">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="4f085-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4f085-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.8 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="4f085-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-144">實體記憶體的資料寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="4f085-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="4f085-145">資料寬度 0 (零) ，總計寬度為8，表示記憶體僅用來提供錯誤更正位。</span><span class="sxs-lookup"><span data-stu-id="4f085-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="4f085-146">**說明**</span><span class="sxs-lookup"><span data-stu-id="4f085-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-149">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4f085-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-150">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4f085-150">Textual description of the object.</span></span>

<span data-ttu-id="4f085-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-152">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="4f085-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4f085-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-155">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "FormFactor" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.6」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-156">晶片的實外型規格。</span><span class="sxs-lookup"><span data-stu-id="4f085-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="4f085-157">例如，您可以指定 SIMM、TSOP 或 PGA 之類的值。</span><span class="sxs-lookup"><span data-stu-id="4f085-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="4f085-158">這個屬性繼承自 [**CIM \_ 晶片**](cim-chip.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="4f085-159">0</span><span class="sxs-lookup"><span data-stu-id="4f085-159">0</span></span>
</dt> <dd>

<span data-ttu-id="4f085-160">Unknown</span><span class="sxs-lookup"><span data-stu-id="4f085-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="4f085-161">1</span><span class="sxs-lookup"><span data-stu-id="4f085-161">1</span></span>
</dt> <dd>

<span data-ttu-id="4f085-162">其他</span><span class="sxs-lookup"><span data-stu-id="4f085-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="4f085-163">2</span><span class="sxs-lookup"><span data-stu-id="4f085-163">2</span></span>
</dt> <dd>

<span data-ttu-id="4f085-164">Sip</span><span class="sxs-lookup"><span data-stu-id="4f085-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-165">3</span><span class="sxs-lookup"><span data-stu-id="4f085-165">3</span></span>
</dt> <dd>

<span data-ttu-id="4f085-166">DIP</span><span class="sxs-lookup"><span data-stu-id="4f085-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-167">4</span><span class="sxs-lookup"><span data-stu-id="4f085-167">4</span></span>
</dt> <dd>

<span data-ttu-id="4f085-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="4f085-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-169">5</span><span class="sxs-lookup"><span data-stu-id="4f085-169">5</span></span>
</dt> <dd>

<span data-ttu-id="4f085-170">SOJ</span><span class="sxs-lookup"><span data-stu-id="4f085-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="4f085-171">6</span><span class="sxs-lookup"><span data-stu-id="4f085-171">6</span></span>
</dt> <dd>

<span data-ttu-id="4f085-172">專屬</span><span class="sxs-lookup"><span data-stu-id="4f085-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="4f085-173">7</span><span class="sxs-lookup"><span data-stu-id="4f085-173">7</span></span>
</dt> <dd>

<span data-ttu-id="4f085-174">Simm</span><span class="sxs-lookup"><span data-stu-id="4f085-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="4f085-175">8</span><span class="sxs-lookup"><span data-stu-id="4f085-175">8</span></span>
</dt> <dd>

<span data-ttu-id="4f085-176">Dimm</span><span class="sxs-lookup"><span data-stu-id="4f085-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="4f085-177">9</span><span class="sxs-lookup"><span data-stu-id="4f085-177">9</span></span>
</dt> <dd>

<span data-ttu-id="4f085-178">TSOP</span><span class="sxs-lookup"><span data-stu-id="4f085-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-179">10</span><span class="sxs-lookup"><span data-stu-id="4f085-179">10</span></span>
</dt> <dd>

<span data-ttu-id="4f085-180">Pga</span><span class="sxs-lookup"><span data-stu-id="4f085-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="4f085-181">11</span><span class="sxs-lookup"><span data-stu-id="4f085-181">11</span></span>
</dt> <dd>

<span data-ttu-id="4f085-182">RIMM</span><span class="sxs-lookup"><span data-stu-id="4f085-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="4f085-183">12</span><span class="sxs-lookup"><span data-stu-id="4f085-183">12</span></span>
</dt> <dd>

<span data-ttu-id="4f085-184">SODIMM</span><span class="sxs-lookup"><span data-stu-id="4f085-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="4f085-185">13</span><span class="sxs-lookup"><span data-stu-id="4f085-185">13</span></span>
</dt> <dd>

<span data-ttu-id="4f085-186">SRIMM</span><span class="sxs-lookup"><span data-stu-id="4f085-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="4f085-187">14</span><span class="sxs-lookup"><span data-stu-id="4f085-187">14</span></span>
</dt> <dd>

<span data-ttu-id="4f085-188">Smd</span><span class="sxs-lookup"><span data-stu-id="4f085-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="4f085-189">15</span><span class="sxs-lookup"><span data-stu-id="4f085-189">15</span></span>
</dt> <dd>

<span data-ttu-id="4f085-190">SSMP</span><span class="sxs-lookup"><span data-stu-id="4f085-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-191">16</span><span class="sxs-lookup"><span data-stu-id="4f085-191">16</span></span>
</dt> <dd>

<span data-ttu-id="4f085-192">QFP</span><span class="sxs-lookup"><span data-stu-id="4f085-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-193">17</span><span class="sxs-lookup"><span data-stu-id="4f085-193">17</span></span>
</dt> <dd>

<span data-ttu-id="4f085-194">TQFP</span><span class="sxs-lookup"><span data-stu-id="4f085-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="4f085-195">18</span><span class="sxs-lookup"><span data-stu-id="4f085-195">18</span></span>
</dt> <dd>

<span data-ttu-id="4f085-196">SOIC</span><span class="sxs-lookup"><span data-stu-id="4f085-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="4f085-197">19</span><span class="sxs-lookup"><span data-stu-id="4f085-197">19</span></span>
</dt> <dd>

<span data-ttu-id="4f085-198">Lcc</span><span class="sxs-lookup"><span data-stu-id="4f085-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="4f085-199">20</span><span class="sxs-lookup"><span data-stu-id="4f085-199">20</span></span>
</dt> <dd>

<span data-ttu-id="4f085-200">PLCC</span><span class="sxs-lookup"><span data-stu-id="4f085-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="4f085-201">21</span><span class="sxs-lookup"><span data-stu-id="4f085-201">21</span></span>
</dt> <dd>

<span data-ttu-id="4f085-202">Bga</span><span class="sxs-lookup"><span data-stu-id="4f085-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="4f085-203">22</span><span class="sxs-lookup"><span data-stu-id="4f085-203">22</span></span>
</dt> <dd>

<span data-ttu-id="4f085-204">FPBGA</span><span class="sxs-lookup"><span data-stu-id="4f085-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="4f085-205">23</span><span class="sxs-lookup"><span data-stu-id="4f085-205">23</span></span>
</dt> <dd>

<span data-ttu-id="4f085-206">LGA</span><span class="sxs-lookup"><span data-stu-id="4f085-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4f085-207">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="4f085-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-208">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f085-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f085-210">若 **為 TRUE**，則可以熱交換套件。</span><span class="sxs-lookup"><span data-stu-id="4f085-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="4f085-211">如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="4f085-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="4f085-212">例如，風扇元件可能會設計為熱交換。</span><span class="sxs-lookup"><span data-stu-id="4f085-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="4f085-213">所有可以熱交換的元件都是可卸載和取代的。</span><span class="sxs-lookup"><span data-stu-id="4f085-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="4f085-214">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4f085-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-216">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4f085-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-218">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4f085-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-219">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4f085-219">Date and time the object was installed.</span></span> <span data-ttu-id="4f085-220">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="4f085-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4f085-221">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-222">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="4f085-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-223">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f085-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-225">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置對應位址 \| 001.7」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-226">實體記憶體在交錯中的位置。</span><span class="sxs-lookup"><span data-stu-id="4f085-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="4f085-227">值為0表示非交錯，1表示第一個位置，2表示第二個位置，依此類推。</span><span class="sxs-lookup"><span data-stu-id="4f085-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="4f085-228">例如，在2:1 交錯中，值1表示記憶體位於偶數位置。</span><span class="sxs-lookup"><span data-stu-id="4f085-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="4f085-229">**製造商**</span><span class="sxs-lookup"><span data-stu-id="4f085-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-232">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="4f085-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-233">負責產生實體元素的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="4f085-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="4f085-234">如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4f085-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="4f085-235">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-236">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="4f085-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4f085-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-239">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.9」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-240">實體記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="4f085-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f085-241">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4f085-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4f085-242">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4f085-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="4f085-243">**DRAM** (2) </span><span class="sxs-lookup"><span data-stu-id="4f085-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="4f085-244">**同步 DRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="4f085-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="4f085-245">**CACHE DRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="4f085-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="4f085-246">**EDO** (5) </span><span class="sxs-lookup"><span data-stu-id="4f085-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="4f085-247">**EDRAM** (6) </span><span class="sxs-lookup"><span data-stu-id="4f085-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="4f085-248">**VRAM** (7) </span><span class="sxs-lookup"><span data-stu-id="4f085-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="4f085-249">**SRAM** (8) </span><span class="sxs-lookup"><span data-stu-id="4f085-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="4f085-250">**RAM** (9) </span><span class="sxs-lookup"><span data-stu-id="4f085-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="4f085-251">**ROM** (10) </span><span class="sxs-lookup"><span data-stu-id="4f085-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="4f085-252">**Flash** (11) </span><span class="sxs-lookup"><span data-stu-id="4f085-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="4f085-253">**EEPROM** (12) </span><span class="sxs-lookup"><span data-stu-id="4f085-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="4f085-254">**FEPROM** (13) </span><span class="sxs-lookup"><span data-stu-id="4f085-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="4f085-255">**EPROM** (14) </span><span class="sxs-lookup"><span data-stu-id="4f085-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="4f085-256">**CDRAM** (15) </span><span class="sxs-lookup"><span data-stu-id="4f085-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="4f085-257">**3DRAM** (16) </span><span class="sxs-lookup"><span data-stu-id="4f085-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="4f085-258">**SDRAM** (17) </span><span class="sxs-lookup"><span data-stu-id="4f085-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="4f085-259">**SGRAM** (18) </span><span class="sxs-lookup"><span data-stu-id="4f085-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="4f085-260">**RDRAM** (19) </span><span class="sxs-lookup"><span data-stu-id="4f085-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="4f085-261">**DDR** (20) </span><span class="sxs-lookup"><span data-stu-id="4f085-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="4f085-262">**DDR2** (21) </span><span class="sxs-lookup"><span data-stu-id="4f085-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="4f085-263">**DDR2 FB-DIMM** (22) </span><span class="sxs-lookup"><span data-stu-id="4f085-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f085-264">**型號**</span><span class="sxs-lookup"><span data-stu-id="4f085-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-265">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-267">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4f085-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-268">實體元素一般已知的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f085-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="4f085-269">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-270">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4f085-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-273">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4f085-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-274">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4f085-274">Label by which the object is known.</span></span> <span data-ttu-id="4f085-275">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4f085-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4f085-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4f085-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f085-280">除了資產標記資訊以外的其他資料，可用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="4f085-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="4f085-281">其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。</span><span class="sxs-lookup"><span data-stu-id="4f085-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="4f085-282">請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="4f085-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="4f085-283">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-284">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="4f085-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-287">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="4f085-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-288">由產生或製造實體元素的組織所指派的元件編號。</span><span class="sxs-lookup"><span data-stu-id="4f085-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="4f085-289">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-290">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="4f085-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-291">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f085-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-293">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置對應位址 \| 001.6」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-294">實體記憶體在資料列中的位置。</span><span class="sxs-lookup"><span data-stu-id="4f085-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="4f085-295">例如，如果使用 2 8 位的記憶體裝置形成16位的資料列，則值2會指出記憶體是第二個裝置。</span><span class="sxs-lookup"><span data-stu-id="4f085-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="4f085-296">0值是此屬性的無效值。</span><span class="sxs-lookup"><span data-stu-id="4f085-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="4f085-297">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="4f085-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-298">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f085-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f085-300">若 **為 TRUE**，則表示實體元素已開啟電源。</span><span class="sxs-lookup"><span data-stu-id="4f085-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="4f085-301">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-302">**移動**</span><span class="sxs-lookup"><span data-stu-id="4f085-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-303">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f085-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f085-305">若 **為 TRUE**，則會將這個專案設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。</span><span class="sxs-lookup"><span data-stu-id="4f085-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="4f085-306">即使電源必須關閉才能執行移除，套件仍會被視為可移動。</span><span class="sxs-lookup"><span data-stu-id="4f085-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="4f085-307">如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。</span><span class="sxs-lookup"><span data-stu-id="4f085-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="4f085-308">例如，ungradable 處理器晶片是可移動的。</span><span class="sxs-lookup"><span data-stu-id="4f085-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="4f085-309">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-310">**更換**</span><span class="sxs-lookup"><span data-stu-id="4f085-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-311">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4f085-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f085-313">若 **為 TRUE**，則可以使用實體不同的元素來取代專案。</span><span class="sxs-lookup"><span data-stu-id="4f085-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="4f085-314">例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。</span><span class="sxs-lookup"><span data-stu-id="4f085-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="4f085-315">在此情況下，即表示處理器被視為可更換。</span><span class="sxs-lookup"><span data-stu-id="4f085-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="4f085-316">所有卸載式元件本身都可取代。</span><span class="sxs-lookup"><span data-stu-id="4f085-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="4f085-317">這個屬性繼承自 [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-318">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4f085-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-321">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4f085-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-322">製造商配置的數位，用來識別實體元素。</span><span class="sxs-lookup"><span data-stu-id="4f085-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="4f085-323">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-324">**SKU**</span><span class="sxs-lookup"><span data-stu-id="4f085-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-327">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4f085-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-328">實體元素的庫存單位號碼。</span><span class="sxs-lookup"><span data-stu-id="4f085-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="4f085-329">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-330">**速度**</span><span class="sxs-lookup"><span data-stu-id="4f085-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-331">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f085-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-333">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「毫微秒」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-334">實體記憶體的速度（以毫微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4f085-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="4f085-335">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4f085-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-338">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4f085-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-339">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4f085-339">Current status of the object.</span></span> <span data-ttu-id="4f085-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4f085-341">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4f085-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4f085-342">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4f085-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4f085-343">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4f085-344">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f085-345">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4f085-346">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4f085-347">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4f085-348">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4f085-349">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4f085-350">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4f085-351">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4f085-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4f085-352">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4f085-353">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4f085-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f085-354">**Tag**</span><span class="sxs-lookup"><span data-stu-id="4f085-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-357">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="4f085-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-358">可唯一識別實體元素並作為專案索引鍵的任一字元串。</span><span class="sxs-lookup"><span data-stu-id="4f085-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="4f085-359">這個屬性可包含資產標記或序號資料等資訊。</span><span class="sxs-lookup"><span data-stu-id="4f085-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="4f085-360">在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。</span><span class="sxs-lookup"><span data-stu-id="4f085-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="4f085-361">例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。</span><span class="sxs-lookup"><span data-stu-id="4f085-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="4f085-362">物件仍會持續存在，甚至可以插入至不同的範圍容器。</span><span class="sxs-lookup"><span data-stu-id="4f085-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="4f085-363">實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。</span><span class="sxs-lookup"><span data-stu-id="4f085-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="4f085-364">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f085-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="4f085-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-366">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4f085-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-368">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="4f085-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4f085-369">實體記憶體的總寬度（以位為單位），包括檢查或錯誤修正位。</span><span class="sxs-lookup"><span data-stu-id="4f085-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="4f085-370">如果沒有錯誤更正位，這個屬性中的值應該符合針對 **DataWidth** 屬性所指定的值。</span><span class="sxs-lookup"><span data-stu-id="4f085-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="4f085-371">**版本**</span><span class="sxs-lookup"><span data-stu-id="4f085-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f085-372">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f085-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f085-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f085-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f085-374">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4f085-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4f085-375">實體元素的版本。</span><span class="sxs-lookup"><span data-stu-id="4f085-375">Version of the physical element.</span></span>

<span data-ttu-id="4f085-376">這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f085-377">備註</span><span class="sxs-lookup"><span data-stu-id="4f085-377">Remarks</span></span>

<span data-ttu-id="4f085-378">**Cim \_ PhysicalMemory** 類別衍生自 [**cim \_ 晶片**](cim-chip.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="4f085-379">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4f085-379">WMI does not implement this class.</span></span> <span data-ttu-id="4f085-380">針對衍生自 **CIM \_ PHYSICALMEMORY** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="4f085-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4f085-381">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4f085-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4f085-382">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4f085-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f085-383">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f085-383">Requirements</span></span>



| <span data-ttu-id="4f085-384">需求</span><span class="sxs-lookup"><span data-stu-id="4f085-384">Requirement</span></span> | <span data-ttu-id="4f085-385">值</span><span class="sxs-lookup"><span data-stu-id="4f085-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f085-386">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f085-386">Minimum supported client</span></span><br/> | <span data-ttu-id="4f085-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f085-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f085-388">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f085-388">Minimum supported server</span></span><br/> | <span data-ttu-id="4f085-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f085-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f085-390">命名空間</span><span class="sxs-lookup"><span data-stu-id="4f085-390">Namespace</span></span><br/>                | <span data-ttu-id="4f085-391">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4f085-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f085-392">MOF</span><span class="sxs-lookup"><span data-stu-id="4f085-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f085-393"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f085-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f085-394">DLL</span><span class="sxs-lookup"><span data-stu-id="4f085-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f085-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f085-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f085-396">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f085-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f085-397">**CIM \_ 晶片**</span><span class="sxs-lookup"><span data-stu-id="4f085-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 

