---
description: CIM \_ MemoryCapacity 類別代表可以安裝在實體元素上的記憶體，以及最小和最大的設定。
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: CIM_MemoryCapacity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187634"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="62bf5-103">CIM \_ MemoryCapacity 類別</span><span class="sxs-lookup"><span data-stu-id="62bf5-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="62bf5-104">**CIM \_ MemoryCapacity** 類別代表可以安裝在實體元素上的記憶體，以及最小和最大的設定。</span><span class="sxs-lookup"><span data-stu-id="62bf5-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="62bf5-105">目前已安裝的記憶體和元素的最小和最大需求的資訊位於 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) 類別的實例中。</span><span class="sxs-lookup"><span data-stu-id="62bf5-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62bf5-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="62bf5-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62bf5-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="62bf5-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62bf5-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="62bf5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="62bf5-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="62bf5-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bf5-110">語法</span><span class="sxs-lookup"><span data-stu-id="62bf5-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="62bf5-111">成員</span><span class="sxs-lookup"><span data-stu-id="62bf5-111">Members</span></span>

<span data-ttu-id="62bf5-112">**CIM \_ MemoryCapacity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="62bf5-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="62bf5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="62bf5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62bf5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="62bf5-114">Properties</span></span>

<span data-ttu-id="62bf5-115">**CIM \_ MemoryCapacity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62bf5-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62bf5-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="62bf5-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bf5-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62bf5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62bf5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="62bf5-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62bf5-120">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="62bf5-120">Short textual description of the object.</span></span>

<span data-ttu-id="62bf5-121">這個屬性繼承自 [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)。</span><span class="sxs-lookup"><span data-stu-id="62bf5-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bf5-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="62bf5-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bf5-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62bf5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62bf5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bf5-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="62bf5-125">Textual description of the object.</span></span>

<span data-ttu-id="62bf5-126">這個屬性繼承自 [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)。</span><span class="sxs-lookup"><span data-stu-id="62bf5-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bf5-127">**MaximumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="62bf5-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bf5-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="62bf5-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62bf5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-130">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="62bf5-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="62bf5-131">相關聯實體元素可支援的最大記憶體數量（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="62bf5-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="62bf5-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="62bf5-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="62bf5-133">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="62bf5-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bf5-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="62bf5-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62bf5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-136">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)。**MemoryType**") </span><span class="sxs-lookup"><span data-stu-id="62bf5-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="62bf5-137">記憶體的類型，這是物件索引鍵的一部分。</span><span class="sxs-lookup"><span data-stu-id="62bf5-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="62bf5-138">值會對應至 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) 類別中可能的記憶體類型清單。</span><span class="sxs-lookup"><span data-stu-id="62bf5-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62bf5-139">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="62bf5-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62bf5-140">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="62bf5-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="62bf5-141">**DRAM** (2) </span><span class="sxs-lookup"><span data-stu-id="62bf5-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="62bf5-142">**同步 DRAM** (3) </span><span class="sxs-lookup"><span data-stu-id="62bf5-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="62bf5-143">**CACHE DRAM** (4) </span><span class="sxs-lookup"><span data-stu-id="62bf5-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="62bf5-144">**EDO** (5) </span><span class="sxs-lookup"><span data-stu-id="62bf5-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="62bf5-145">**EDRAM** (6) </span><span class="sxs-lookup"><span data-stu-id="62bf5-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="62bf5-146">**VRAM** (7) </span><span class="sxs-lookup"><span data-stu-id="62bf5-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="62bf5-147">**SRAM** (8) </span><span class="sxs-lookup"><span data-stu-id="62bf5-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="62bf5-148">**RAM** (9) </span><span class="sxs-lookup"><span data-stu-id="62bf5-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="62bf5-149">**ROM** (10) </span><span class="sxs-lookup"><span data-stu-id="62bf5-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="62bf5-150">**Flash** (11) </span><span class="sxs-lookup"><span data-stu-id="62bf5-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="62bf5-151">**EEPROM** (12) </span><span class="sxs-lookup"><span data-stu-id="62bf5-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="62bf5-152">**FEPROM** (13) </span><span class="sxs-lookup"><span data-stu-id="62bf5-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="62bf5-153">**EPROM** (14) </span><span class="sxs-lookup"><span data-stu-id="62bf5-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="62bf5-154">**CDRAM** (15) </span><span class="sxs-lookup"><span data-stu-id="62bf5-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="62bf5-155">**3DRAM** (16) </span><span class="sxs-lookup"><span data-stu-id="62bf5-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="62bf5-156">**SDRAM** (17) </span><span class="sxs-lookup"><span data-stu-id="62bf5-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="62bf5-157">**SGRAM** (18) </span><span class="sxs-lookup"><span data-stu-id="62bf5-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="62bf5-158">**RDRAM** (19) </span><span class="sxs-lookup"><span data-stu-id="62bf5-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="62bf5-159">**DDR** (20) </span><span class="sxs-lookup"><span data-stu-id="62bf5-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="62bf5-160">**DDR-2** (21) </span><span class="sxs-lookup"><span data-stu-id="62bf5-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62bf5-161">**MinimumMemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="62bf5-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bf5-162">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="62bf5-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62bf5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-164">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="62bf5-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="62bf5-165">相關實體專案正常運作所需的最小記憶體數量（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="62bf5-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="62bf5-166">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="62bf5-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="62bf5-167">**名稱**</span><span class="sxs-lookup"><span data-stu-id="62bf5-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bf5-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62bf5-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62bf5-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bf5-170">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62bf5-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62bf5-171">物件的名稱;作為物件索引鍵的一部分。</span><span class="sxs-lookup"><span data-stu-id="62bf5-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62bf5-172">備註</span><span class="sxs-lookup"><span data-stu-id="62bf5-172">Remarks</span></span>

<span data-ttu-id="62bf5-173">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="62bf5-173">WMI does not implement this class.</span></span>

<span data-ttu-id="62bf5-174">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="62bf5-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62bf5-175">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="62bf5-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62bf5-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="62bf5-176">Requirements</span></span>



| <span data-ttu-id="62bf5-177">需求</span><span class="sxs-lookup"><span data-stu-id="62bf5-177">Requirement</span></span> | <span data-ttu-id="62bf5-178">值</span><span class="sxs-lookup"><span data-stu-id="62bf5-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62bf5-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62bf5-179">Minimum supported client</span></span><br/> | <span data-ttu-id="62bf5-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62bf5-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62bf5-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62bf5-181">Minimum supported server</span></span><br/> | <span data-ttu-id="62bf5-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62bf5-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62bf5-183">命名空間</span><span class="sxs-lookup"><span data-stu-id="62bf5-183">Namespace</span></span><br/>                | <span data-ttu-id="62bf5-184">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62bf5-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62bf5-185">MOF</span><span class="sxs-lookup"><span data-stu-id="62bf5-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62bf5-186"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="62bf5-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62bf5-187">DLL</span><span class="sxs-lookup"><span data-stu-id="62bf5-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62bf5-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62bf5-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62bf5-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62bf5-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bf5-190">**CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="62bf5-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 

