---
description: Win32 \_ AssociatedProcessorMemory 關聯 WMI 類別會使處理器與其快取記憶體產生關聯。
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Win32_AssociatedProcessorMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936454"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="6727e-103">Win32 \_ AssociatedProcessorMemory 類別</span><span class="sxs-lookup"><span data-stu-id="6727e-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="6727e-104">**Win32 \_ AssociatedProcessorMemory** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會使處理器與其快取記憶體產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6727e-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="6727e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6727e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6727e-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6727e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6727e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6727e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6727e-108">成員</span><span class="sxs-lookup"><span data-stu-id="6727e-108">Members</span></span>

<span data-ttu-id="6727e-109">**Win32 \_ AssociatedProcessorMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6727e-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="6727e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6727e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6727e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6727e-111">Properties</span></span>

<span data-ttu-id="6727e-112">**Win32 \_ AssociatedProcessorMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6727e-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6727e-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="6727e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6727e-114">資料類型： **Win32 \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="6727e-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="6727e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6727e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6727e-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ CacheMemory" ) </span><span class="sxs-lookup"><span data-stu-id="6727e-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="6727e-117">[**Win32 \_ CacheMemory**](win32-cachememory.md) ，描述可供處理器使用的快取記憶體。</span><span class="sxs-lookup"><span data-stu-id="6727e-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="6727e-118">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="6727e-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6727e-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6727e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6727e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6727e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6727e-121">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "mhz" ) </span><span class="sxs-lookup"><span data-stu-id="6727e-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="6727e-122">處理器與記憶體之間的匯流排速度，以 mhz (MHz) 。</span><span class="sxs-lookup"><span data-stu-id="6727e-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="6727e-123">這個屬性繼承自 [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)。</span><span class="sxs-lookup"><span data-stu-id="6727e-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="6727e-124">**依賴**</span><span class="sxs-lookup"><span data-stu-id="6727e-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6727e-125">資料類型： **Win32 \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="6727e-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="6727e-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6727e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6727e-127">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 \_ 處理器」 ) </span><span class="sxs-lookup"><span data-stu-id="6727e-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="6727e-128">[**Win32 \_ 處理器**](win32-processor.md)，描述使用快取記憶體的處理器。</span><span class="sxs-lookup"><span data-stu-id="6727e-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6727e-129">備註</span><span class="sxs-lookup"><span data-stu-id="6727e-129">Remarks</span></span>

<span data-ttu-id="6727e-130">**Win32 \_ AssociatedProcessorMemory** 類別衍生自 [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)。</span><span class="sxs-lookup"><span data-stu-id="6727e-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6727e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6727e-131">Requirements</span></span>



| <span data-ttu-id="6727e-132">需求</span><span class="sxs-lookup"><span data-stu-id="6727e-132">Requirement</span></span> | <span data-ttu-id="6727e-133">值</span><span class="sxs-lookup"><span data-stu-id="6727e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6727e-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6727e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6727e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6727e-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6727e-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6727e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6727e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6727e-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6727e-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="6727e-138">Namespace</span></span><br/>                | <span data-ttu-id="6727e-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6727e-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6727e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6727e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6727e-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6727e-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6727e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6727e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6727e-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6727e-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6727e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6727e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6727e-145">**CIM \_ AssociatedProcessorMemory**</span><span class="sxs-lookup"><span data-stu-id="6727e-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="6727e-146">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="6727e-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

