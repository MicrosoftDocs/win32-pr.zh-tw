---
description: CIM \_ AggregateRedundancyComponent 類別描述儲存體冗余群組中的匯總實體範圍。
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: CIM_AggregateRedundancyComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689035"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="62ae0-103">CIM \_ AggregateRedundancyComponent 類別</span><span class="sxs-lookup"><span data-stu-id="62ae0-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="62ae0-104">**CIM \_ AggregateRedundancyComponent** 類別描述儲存體冗余群組中的匯總實體範圍。</span><span class="sxs-lookup"><span data-stu-id="62ae0-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62ae0-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="62ae0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62ae0-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="62ae0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62ae0-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="62ae0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="62ae0-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="62ae0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ae0-109">語法</span><span class="sxs-lookup"><span data-stu-id="62ae0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="62ae0-110">成員</span><span class="sxs-lookup"><span data-stu-id="62ae0-110">Members</span></span>

<span data-ttu-id="62ae0-111">**CIM \_ AggregateRedundancyComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="62ae0-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="62ae0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="62ae0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62ae0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="62ae0-113">Properties</span></span>

<span data-ttu-id="62ae0-114">**CIM \_ AggregateRedundancyComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62ae0-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62ae0-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="62ae0-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ae0-116">資料類型： **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="62ae0-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="62ae0-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ae0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ae0-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="62ae0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="62ae0-119">包含儲存體冗余群組的 [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) 。</span><span class="sxs-lookup"><span data-stu-id="62ae0-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="62ae0-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="62ae0-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ae0-121">資料類型： **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="62ae0-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="62ae0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ae0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ae0-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="62ae0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="62ae0-124">[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) ，包含參與冗余群組的匯總實體範圍。</span><span class="sxs-lookup"><span data-stu-id="62ae0-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62ae0-125">備註</span><span class="sxs-lookup"><span data-stu-id="62ae0-125">Remarks</span></span>

<span data-ttu-id="62ae0-126">**Cim \_ AggregateRedundancyComponent** 類別衍生自 [**cim \_ RedundancyComponent**](cim-redundancycomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="62ae0-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="62ae0-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="62ae0-127">WMI does not implement this class.</span></span>

<span data-ttu-id="62ae0-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="62ae0-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62ae0-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="62ae0-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ae0-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="62ae0-130">Requirements</span></span>



| <span data-ttu-id="62ae0-131">需求</span><span class="sxs-lookup"><span data-stu-id="62ae0-131">Requirement</span></span> | <span data-ttu-id="62ae0-132">值</span><span class="sxs-lookup"><span data-stu-id="62ae0-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ae0-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62ae0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="62ae0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62ae0-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62ae0-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62ae0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="62ae0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62ae0-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62ae0-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="62ae0-137">Namespace</span></span><br/>                | <span data-ttu-id="62ae0-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62ae0-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62ae0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="62ae0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62ae0-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="62ae0-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62ae0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="62ae0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ae0-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ae0-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ae0-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62ae0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ae0-144">**CIM \_ RedundancyComponent**</span><span class="sxs-lookup"><span data-stu-id="62ae0-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

