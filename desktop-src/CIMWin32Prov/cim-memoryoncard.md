---
description: CIM \_ MemoryOnCard 類別會將位於主機板、介面卡等上的實體記憶體相關聯。 此關聯會明確定義記憶體與卡片之間的關聯性。
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: CIM_MemoryOnCard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970328"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="914c5-104">CIM \_ MemoryOnCard 類別</span><span class="sxs-lookup"><span data-stu-id="914c5-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="914c5-105">**CIM \_ MemoryOnCard** 類別會將位於主機板、介面卡等上的實體記憶體相關聯。</span><span class="sxs-lookup"><span data-stu-id="914c5-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="914c5-106">此關聯會明確定義記憶體與卡片之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="914c5-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="914c5-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="914c5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="914c5-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="914c5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="914c5-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="914c5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="914c5-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="914c5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="914c5-111">語法</span><span class="sxs-lookup"><span data-stu-id="914c5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="914c5-112">成員</span><span class="sxs-lookup"><span data-stu-id="914c5-112">Members</span></span>

<span data-ttu-id="914c5-113">**CIM \_ MemoryOnCard** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="914c5-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="914c5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="914c5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="914c5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="914c5-115">Properties</span></span>

<span data-ttu-id="914c5-116">**CIM \_ MemoryOnCard** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="914c5-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="914c5-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="914c5-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="914c5-118">資料類型： **CIM \_ 卡片**</span><span class="sxs-lookup"><span data-stu-id="914c5-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="914c5-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="914c5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="914c5-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="914c5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="914c5-121">一種 [**CIM \_ 卡片**](cim-card.md) ，描述包含或「包含」記憶體的卡片。</span><span class="sxs-lookup"><span data-stu-id="914c5-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="914c5-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="914c5-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="914c5-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="914c5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="914c5-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="914c5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="914c5-125">自由格式的字串，表示實體元素在實體封裝內的位置。</span><span class="sxs-lookup"><span data-stu-id="914c5-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="914c5-126">與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。</span><span class="sxs-lookup"><span data-stu-id="914c5-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="914c5-127">此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="914c5-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="914c5-128">這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。</span><span class="sxs-lookup"><span data-stu-id="914c5-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="914c5-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="914c5-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="914c5-130">資料類型： **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="914c5-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="914c5-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="914c5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="914c5-132">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="914c5-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="914c5-133">[**CIM \_ PhysicalMemory**](cim-physicalmemory.md) ，描述位於卡片上的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="914c5-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="914c5-134">備註</span><span class="sxs-lookup"><span data-stu-id="914c5-134">Remarks</span></span>

<span data-ttu-id="914c5-135">**Cim \_ MemoryOnCard** 類別衍生自 [**cim \_ PackagedComponent**](cim-packagedcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="914c5-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="914c5-136">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="914c5-136">WMI does not implement this class.</span></span>

<span data-ttu-id="914c5-137">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="914c5-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="914c5-138">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="914c5-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="914c5-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="914c5-139">Requirements</span></span>



| <span data-ttu-id="914c5-140">需求</span><span class="sxs-lookup"><span data-stu-id="914c5-140">Requirement</span></span> | <span data-ttu-id="914c5-141">值</span><span class="sxs-lookup"><span data-stu-id="914c5-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="914c5-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="914c5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="914c5-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="914c5-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="914c5-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="914c5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="914c5-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="914c5-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="914c5-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="914c5-146">Namespace</span></span><br/>                | <span data-ttu-id="914c5-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="914c5-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="914c5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="914c5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="914c5-149"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="914c5-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="914c5-150">DLL</span><span class="sxs-lookup"><span data-stu-id="914c5-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="914c5-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="914c5-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914c5-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="914c5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="914c5-153">**CIM \_ PackagedComponent**</span><span class="sxs-lookup"><span data-stu-id="914c5-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

