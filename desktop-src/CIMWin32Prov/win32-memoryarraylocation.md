---
description: Win32 \_ MemoryArrayLocation 關聯 WMI 類別會將邏輯記憶體陣列和其所在的實體記憶體陣列產生關聯。
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Win32_MemoryArrayLocation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510687"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="7d7a8-103">Win32 \_ MemoryArrayLocation 類別</span><span class="sxs-lookup"><span data-stu-id="7d7a8-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="7d7a8-104">**Win32 \_ MemoryArrayLocation** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將邏輯記憶體陣列和其所在的實體記憶體陣列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="7d7a8-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7d7a8-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="7d7a8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7d7a8-108">成員</span><span class="sxs-lookup"><span data-stu-id="7d7a8-108">Members</span></span>

<span data-ttu-id="7d7a8-109">**Win32 \_ MemoryArrayLocation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7d7a8-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="7d7a8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7d7a8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d7a8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7d7a8-111">Properties</span></span>

<span data-ttu-id="7d7a8-112">**Win32 \_ MemoryArrayLocation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d7a8-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="7d7a8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7a8-114">資料類型： **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="7d7a8-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="7d7a8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7d7a8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d7a8-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ PhysicalMemoryArray" ) </span><span class="sxs-lookup"><span data-stu-id="7d7a8-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="7d7a8-117">[**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md) ，描述實邏輯記憶體陣列的實體記憶體陣列。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="7d7a8-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="7d7a8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7a8-119">資料類型： **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="7d7a8-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="7d7a8-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7d7a8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d7a8-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 MemoryArray」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="7d7a8-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="7d7a8-122">[**Win32 \_ MemoryArray**](win32-memoryarray.md) ，描述實體記憶體陣列所執行的邏輯記憶體陣列。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d7a8-123">備註</span><span class="sxs-lookup"><span data-stu-id="7d7a8-123">Remarks</span></span>

<span data-ttu-id="7d7a8-124">**Win32 \_ MemoryArrayLocation** 類別衍生自 [**CIM \_**](cim-realizes.md)。</span><span class="sxs-lookup"><span data-stu-id="7d7a8-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d7a8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d7a8-125">Requirements</span></span>



| <span data-ttu-id="7d7a8-126">需求</span><span class="sxs-lookup"><span data-stu-id="7d7a8-126">Requirement</span></span> | <span data-ttu-id="7d7a8-127">值</span><span class="sxs-lookup"><span data-stu-id="7d7a8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7a8-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d7a8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d7a8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d7a8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d7a8-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d7a8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d7a8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d7a8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d7a8-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d7a8-132">Namespace</span></span><br/>                | <span data-ttu-id="7d7a8-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d7a8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d7a8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7d7a8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d7a8-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d7a8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d7a8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7d7a8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d7a8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d7a8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d7a8-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d7a8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7a8-139">**CIM \_ 意識**</span><span class="sxs-lookup"><span data-stu-id="7d7a8-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="7d7a8-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="7d7a8-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

