---
description: CIM \_ RealizesAggregatePExtent 關聯表示在 \_ 實體媒體上實現 CIM AggregatePExtent 類別的關聯性。
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: CIM_RealizesAggregatePExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999834"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="8926a-103">CIM \_ RealizesAggregatePExtent 類別</span><span class="sxs-lookup"><span data-stu-id="8926a-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="8926a-104">**Cim \_ RealizesAggregatePExtent** 關聯表示在實體媒體上實現 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)類別的關聯性。</span><span class="sxs-lookup"><span data-stu-id="8926a-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8926a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8926a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8926a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8926a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8926a-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8926a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8926a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8926a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8926a-109">語法</span><span class="sxs-lookup"><span data-stu-id="8926a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8926a-110">成員</span><span class="sxs-lookup"><span data-stu-id="8926a-110">Members</span></span>

<span data-ttu-id="8926a-111">**CIM \_ RealizesAggregatePExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8926a-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="8926a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8926a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8926a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8926a-113">Properties</span></span>

<span data-ttu-id="8926a-114">**CIM \_ RealizesAggregatePExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8926a-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8926a-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="8926a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8926a-116">資料類型： **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="8926a-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="8926a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8926a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8926a-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="8926a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8926a-119">[**CIM \_ PhysicalMedia**](cim-physicalmedia.md) ，描述已實現範圍的實體媒體。</span><span class="sxs-lookup"><span data-stu-id="8926a-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="8926a-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8926a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8926a-121">資料類型： **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="8926a-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="8926a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8926a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8926a-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="8926a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8926a-124">位於媒體上的 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) 。</span><span class="sxs-lookup"><span data-stu-id="8926a-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8926a-125">備註</span><span class="sxs-lookup"><span data-stu-id="8926a-125">Remarks</span></span>

<span data-ttu-id="8926a-126">**Cim \_ RealizesAggregatePExtent** 類別衍生自 [**cim \_**](cim-realizes.md)。</span><span class="sxs-lookup"><span data-stu-id="8926a-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="8926a-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="8926a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="8926a-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8926a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8926a-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8926a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8926a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8926a-130">Requirements</span></span>



| <span data-ttu-id="8926a-131">需求</span><span class="sxs-lookup"><span data-stu-id="8926a-131">Requirement</span></span> | <span data-ttu-id="8926a-132">值</span><span class="sxs-lookup"><span data-stu-id="8926a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8926a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8926a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8926a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8926a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8926a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8926a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8926a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8926a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8926a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="8926a-137">Namespace</span></span><br/>                | <span data-ttu-id="8926a-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8926a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8926a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8926a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8926a-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8926a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8926a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8926a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8926a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8926a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8926a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8926a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8926a-144">**CIM \_ 意識**</span><span class="sxs-lookup"><span data-stu-id="8926a-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

