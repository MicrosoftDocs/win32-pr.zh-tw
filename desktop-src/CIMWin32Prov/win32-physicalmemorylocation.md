---
description: Win32 \_ PhysicalMemoryLocation 關聯 WMI 類別會將實體記憶體和其實體記憶體的陣列產生關聯。
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936515"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="e54eb-103">Win32 \_ PhysicalMemoryLocation 類別</span><span class="sxs-lookup"><span data-stu-id="e54eb-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="e54eb-104">**Win32 \_ PhysicalMemoryLocation** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將實體記憶體和其實體記憶體的陣列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e54eb-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="e54eb-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e54eb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e54eb-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e54eb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54eb-107">語法</span><span class="sxs-lookup"><span data-stu-id="e54eb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e54eb-108">成員</span><span class="sxs-lookup"><span data-stu-id="e54eb-108">Members</span></span>

<span data-ttu-id="e54eb-109">**Win32 \_ PhysicalMemoryLocation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e54eb-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="e54eb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e54eb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e54eb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e54eb-111">Properties</span></span>

<span data-ttu-id="e54eb-112">**Win32 \_ PhysicalMemoryLocation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e54eb-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e54eb-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e54eb-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e54eb-114">資料類型： **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="e54eb-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="e54eb-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e54eb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e54eb-116">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PhysicalMemoryArray" ) </span><span class="sxs-lookup"><span data-stu-id="e54eb-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="e54eb-117">[**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md) ，代表包含實體記憶體的實體記憶體陣列。</span><span class="sxs-lookup"><span data-stu-id="e54eb-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="e54eb-118">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="e54eb-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e54eb-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e54eb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e54eb-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e54eb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e54eb-121">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="e54eb-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="e54eb-122">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="e54eb-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="e54eb-123">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="e54eb-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="e54eb-124">這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="e54eb-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="e54eb-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e54eb-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e54eb-126">資料類型： **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="e54eb-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="e54eb-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e54eb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e54eb-128">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PhysicalMemory" ) </span><span class="sxs-lookup"><span data-stu-id="e54eb-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="e54eb-129">[**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) ，代表包含在實體記憶體陣列中的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="e54eb-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e54eb-130">備註</span><span class="sxs-lookup"><span data-stu-id="e54eb-130">Remarks</span></span>

<span data-ttu-id="e54eb-131">**Win32 \_ PhysicalMemoryLocation** 類別衍生自 [**CIM \_ PackagedComponent**](cim-packagedcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="e54eb-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e54eb-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e54eb-132">Requirements</span></span>



| <span data-ttu-id="e54eb-133">需求</span><span class="sxs-lookup"><span data-stu-id="e54eb-133">Requirement</span></span> | <span data-ttu-id="e54eb-134">值</span><span class="sxs-lookup"><span data-stu-id="e54eb-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e54eb-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e54eb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e54eb-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e54eb-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e54eb-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e54eb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e54eb-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e54eb-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e54eb-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="e54eb-139">Namespace</span></span><br/>                | <span data-ttu-id="e54eb-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e54eb-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e54eb-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e54eb-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e54eb-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e54eb-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e54eb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e54eb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e54eb-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e54eb-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54eb-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e54eb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54eb-146">**CIM \_ PackagedComponent**</span><span class="sxs-lookup"><span data-stu-id="e54eb-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="e54eb-147">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e54eb-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
