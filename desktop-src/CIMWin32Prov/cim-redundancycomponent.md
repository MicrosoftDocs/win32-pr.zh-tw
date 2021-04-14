---
description: CIM \_ RedundancyComponent 類別會將由受管理系統專案組成的複製群組產生關聯，並指出這些元素一起提供冗余。
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847055"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="f53ad-103">CIM \_ RedundancyComponent 類別</span><span class="sxs-lookup"><span data-stu-id="f53ad-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="f53ad-104">**CIM \_ RedundancyComponent** 類別會將由受管理系統專案組成的複製群組產生關聯，並指出這些元素一起提供冗余。</span><span class="sxs-lookup"><span data-stu-id="f53ad-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="f53ad-105">在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。</span><span class="sxs-lookup"><span data-stu-id="f53ad-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f53ad-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f53ad-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f53ad-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f53ad-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f53ad-108">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f53ad-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f53ad-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f53ad-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f53ad-110">語法</span><span class="sxs-lookup"><span data-stu-id="f53ad-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f53ad-111">成員</span><span class="sxs-lookup"><span data-stu-id="f53ad-111">Members</span></span>

<span data-ttu-id="f53ad-112">**CIM \_ RedundancyComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f53ad-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f53ad-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f53ad-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f53ad-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f53ad-114">Properties</span></span>

<span data-ttu-id="f53ad-115">**CIM \_ RedundancyComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f53ad-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f53ad-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f53ad-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f53ad-117">資料類型： **CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="f53ad-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="f53ad-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f53ad-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f53ad-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="f53ad-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f53ad-120">**CIM \_ RedundancyComponent** 關聯表示「這組風扇」或「這些實體範圍」參與單一的複製群組。</span><span class="sxs-lookup"><span data-stu-id="f53ad-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="f53ad-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f53ad-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f53ad-122">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="f53ad-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="f53ad-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f53ad-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f53ad-124">[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) ，描述關聯中的子項目。</span><span class="sxs-lookup"><span data-stu-id="f53ad-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="f53ad-125">這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="f53ad-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f53ad-126">備註</span><span class="sxs-lookup"><span data-stu-id="f53ad-126">Remarks</span></span>

<span data-ttu-id="f53ad-127">**CIM \_RedundancyComponent** 衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="f53ad-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="f53ad-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f53ad-128">WMI does not implement this class.</span></span>

<span data-ttu-id="f53ad-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f53ad-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f53ad-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f53ad-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53ad-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f53ad-131">Requirements</span></span>



| <span data-ttu-id="f53ad-132">需求</span><span class="sxs-lookup"><span data-stu-id="f53ad-132">Requirement</span></span> | <span data-ttu-id="f53ad-133">值</span><span class="sxs-lookup"><span data-stu-id="f53ad-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f53ad-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f53ad-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f53ad-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f53ad-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f53ad-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f53ad-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f53ad-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f53ad-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f53ad-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="f53ad-138">Namespace</span></span><br/>                | <span data-ttu-id="f53ad-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f53ad-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f53ad-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f53ad-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f53ad-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f53ad-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f53ad-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f53ad-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f53ad-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f53ad-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f53ad-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f53ad-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53ad-145">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="f53ad-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

