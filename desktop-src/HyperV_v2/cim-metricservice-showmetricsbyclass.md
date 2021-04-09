---
description: 報告下列各項：可針對 CIM 類別的所有實例收集的計量、可供收集 CIM BaseMetricDefinition 實例所定義之計量的 CIM 類別， \_ 以及目前是否正在為 managed 元素收集特定的度量。
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: CIM_MetricService 類別的 ShowMetricsByClass 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849502"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="67dfc-103">CIM MetricService 類別的 ShowMetricsByClass 方法 \_</span><span class="sxs-lookup"><span data-stu-id="67dfc-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="67dfc-104">報告下列各項：可針對 CIM 類別的所有實例收集的計量、可供收集 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例所定義之計量的 cim 類別，以及目前是否正在為 managed 元素收集特定的度量。</span><span class="sxs-lookup"><span data-stu-id="67dfc-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="67dfc-105">語法</span><span class="sxs-lookup"><span data-stu-id="67dfc-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="67dfc-106">參數</span><span class="sxs-lookup"><span data-stu-id="67dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67dfc-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="67dfc-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67dfc-108">識別 CIM 類別，其方法會將參考傳回給 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 的實例，以定義可針對類別的所有實例來捕捉的度量。</span><span class="sxs-lookup"><span data-stu-id="67dfc-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="67dfc-109">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67dfc-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67dfc-110">識別 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="67dfc-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="67dfc-111">方法會傳回 [**cim \_ ManagedElement**](cim-managedelement.md) 實例的參考，以供收集 **cim \_ BaseMetricDefinition** 實例所定義的計量。</span><span class="sxs-lookup"><span data-stu-id="67dfc-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="67dfc-112">*DefinitionList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67dfc-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67dfc-113">成功時，可能會包含 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)物件之實例的參考，這些物件定義了針對 *Subject* 參數所識別之 [**cim \_ ManagedElement**](cim-managedelement.md)可收集的計量。</span><span class="sxs-lookup"><span data-stu-id="67dfc-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="67dfc-114">*MetricNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67dfc-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67dfc-115">成功時，每個陣列索引都應該包含 *DefinitionList* 參數的對應陣列索引所參考之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的 **名稱** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="67dfc-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="67dfc-116">*MetricCollectionEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67dfc-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67dfc-117">指出是否要針對 managed 專案類別的所有實例收集度量。</span><span class="sxs-lookup"><span data-stu-id="67dfc-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67dfc-118">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="67dfc-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67dfc-119">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="67dfc-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="67dfc-120">**保留** (4) </span><span class="sxs-lookup"><span data-stu-id="67dfc-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="67dfc-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="67dfc-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="67dfc-122">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="67dfc-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="67dfc-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="67dfc-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="67dfc-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="67dfc-124">Return value</span></span>

<span data-ttu-id="67dfc-125">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="67dfc-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="67dfc-126">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="67dfc-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67dfc-127">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="67dfc-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="67dfc-128">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="67dfc-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="67dfc-129">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="67dfc-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="67dfc-130">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="67dfc-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="67dfc-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="67dfc-131">Requirements</span></span>



| <span data-ttu-id="67dfc-132">需求</span><span class="sxs-lookup"><span data-stu-id="67dfc-132">Requirement</span></span> | <span data-ttu-id="67dfc-133">值</span><span class="sxs-lookup"><span data-stu-id="67dfc-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67dfc-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67dfc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="67dfc-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="67dfc-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="67dfc-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67dfc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="67dfc-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="67dfc-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="67dfc-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="67dfc-138">Namespace</span></span><br/>                | <span data-ttu-id="67dfc-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="67dfc-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67dfc-140">MOF</span><span class="sxs-lookup"><span data-stu-id="67dfc-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67dfc-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="67dfc-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67dfc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="67dfc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67dfc-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67dfc-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67dfc-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67dfc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67dfc-145">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="67dfc-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




