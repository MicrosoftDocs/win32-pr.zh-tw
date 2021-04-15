---
description: CIM \_ PExtentRedundancyComponent 類別代表參與儲存體冗余群組的實體範圍。
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: CIM_PExtentRedundancyComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468053"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="8bf3a-103">CIM \_ PExtentRedundancyComponent 類別</span><span class="sxs-lookup"><span data-stu-id="8bf3a-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="8bf3a-104">**CIM \_ PExtentRedundancyComponent** 類別代表參與儲存體冗余群組的實體範圍。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bf3a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8bf3a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8bf3a-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8bf3a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf3a-109">語法</span><span class="sxs-lookup"><span data-stu-id="8bf3a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="8bf3a-110">成員</span><span class="sxs-lookup"><span data-stu-id="8bf3a-110">Members</span></span>

<span data-ttu-id="8bf3a-111">**CIM \_ PExtentRedundancyComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8bf3a-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8bf3a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8bf3a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bf3a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8bf3a-113">Properties</span></span>

<span data-ttu-id="8bf3a-114">**CIM \_ PExtentRedundancyComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bf3a-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf3a-116">資料類型： **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="8bf3a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8bf3a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf3a-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="8bf3a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8bf3a-119">描述儲存體冗余群組的 [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) 。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="8bf3a-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf3a-121">資料類型： **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="8bf3a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8bf3a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf3a-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="8bf3a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8bf3a-124">[**CIM \_ PhysicalExtent**](cim-physicalextent.md) ，描述參與冗余群組的實體範圍。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bf3a-125">備註</span><span class="sxs-lookup"><span data-stu-id="8bf3a-125">Remarks</span></span>

<span data-ttu-id="8bf3a-126">**Cim \_ PExtentRedundancyComponent** 類別衍生自 [**cim \_ RedundancyComponent**](cim-redundancycomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="8bf3a-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="8bf3a-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8bf3a-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8bf3a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf3a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bf3a-130">Requirements</span></span>



| <span data-ttu-id="8bf3a-131">需求</span><span class="sxs-lookup"><span data-stu-id="8bf3a-131">Requirement</span></span> | <span data-ttu-id="8bf3a-132">值</span><span class="sxs-lookup"><span data-stu-id="8bf3a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf3a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bf3a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf3a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bf3a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bf3a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bf3a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf3a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bf3a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bf3a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="8bf3a-137">Namespace</span></span><br/>                | <span data-ttu-id="8bf3a-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8bf3a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8bf3a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8bf3a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bf3a-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bf3a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bf3a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf3a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf3a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bf3a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf3a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bf3a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf3a-144">**CIM \_ RedundancyComponent**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

