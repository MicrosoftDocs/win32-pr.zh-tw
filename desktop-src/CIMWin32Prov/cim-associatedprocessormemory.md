---
description: CIM \_ AssociatedProcessorMemory 類別會將處理器和系統記憶體或處理器的快取產生關聯。
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: CIM_AssociatedProcessorMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936391"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="9e8b3-103">CIM \_ AssociatedProcessorMemory 類別</span><span class="sxs-lookup"><span data-stu-id="9e8b3-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="9e8b3-104">**CIM \_ AssociatedProcessorMemory** 類別會將處理器和系統記憶體或處理器的快取產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e8b3-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e8b3-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9e8b3-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9e8b3-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8b3-109">語法</span><span class="sxs-lookup"><span data-stu-id="9e8b3-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="9e8b3-110">成員</span><span class="sxs-lookup"><span data-stu-id="9e8b3-110">Members</span></span>

<span data-ttu-id="9e8b3-111">**CIM \_ AssociatedProcessorMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9e8b3-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="9e8b3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9e8b3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e8b3-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9e8b3-113">Properties</span></span>

<span data-ttu-id="9e8b3-114">**CIM \_ AssociatedProcessorMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e8b3-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e8b3-116">資料類型： **CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="9e8b3-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e8b3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e8b3-118">[**CIM \_ 記憶體**](cim-memory.md)，描述安裝在裝置上或與裝置相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="9e8b3-119">這個屬性繼承自 [**CIM \_ AssociatedMemory**](cim-associatedmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e8b3-120">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e8b3-121">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e8b3-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e8b3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e8b3-123">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "mhz" ) </span><span class="sxs-lookup"><span data-stu-id="9e8b3-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="9e8b3-124">處理器與記憶體之間的匯流排速度，以 mhz (MHz) 。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="9e8b3-125">**依賴**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e8b3-126">資料類型： **CIM \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="9e8b3-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e8b3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e8b3-128">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="9e8b3-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9e8b3-129">[**CIM \_ 處理器**](cim-processor.md)，描述存取記憶體或使用快取的處理器。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e8b3-130">備註</span><span class="sxs-lookup"><span data-stu-id="9e8b3-130">Remarks</span></span>

<span data-ttu-id="9e8b3-131">**Cim \_ AssociatedProcessorMemory** 類別衍生自 [**cim \_ AssociatedMemory**](cim-associatedmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="9e8b3-132">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-132">WMI does not implement this class.</span></span> <span data-ttu-id="9e8b3-133">如需衍生自 **CIM \_ AssociatedProcessorMemory** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9e8b3-134">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e8b3-135">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9e8b3-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8b3-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e8b3-136">Requirements</span></span>



| <span data-ttu-id="9e8b3-137">需求</span><span class="sxs-lookup"><span data-stu-id="9e8b3-137">Requirement</span></span> | <span data-ttu-id="9e8b3-138">值</span><span class="sxs-lookup"><span data-stu-id="9e8b3-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8b3-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e8b3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8b3-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e8b3-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e8b3-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e8b3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8b3-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e8b3-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e8b3-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e8b3-143">Namespace</span></span><br/>                | <span data-ttu-id="9e8b3-144">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9e8b3-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e8b3-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9e8b3-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e8b3-146"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b3-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e8b3-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8b3-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8b3-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b3-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e8b3-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e8b3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8b3-150">**CIM \_ AssociatedMemory**</span><span class="sxs-lookup"><span data-stu-id="9e8b3-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

