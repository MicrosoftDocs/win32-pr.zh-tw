---
description: 報告下列各項：可針對 managed 元素收集的計量、可供收集 CIM BaseMetricDefinition 實例所定義之計量的受控元素， \_ 以及目前是否正在收集 managed 專案的特定度量。
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: CIM_MetricService 類別的 ShowMetrics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115632"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="b1ddb-103">CIM MetricService 類別的 ShowMetrics 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b1ddb-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="b1ddb-104">報告下列各項：可針對 managed 元素收集的計量、可供收集 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例所定義之計量的受控元素，以及目前是否正在收集 managed 專案的特定度量。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ddb-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1ddb-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="b1ddb-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1ddb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ddb-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1ddb-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ddb-108">識別 [**cim \_ managedelement**](cim-managedelement.md) 的實例，該實例會傳回 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例的參考，而該實例會定義針對 **cim \_ ManagedElement** 所捕捉的度量。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="b1ddb-109">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1ddb-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ddb-110">識別 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="b1ddb-111">方法會傳回 [**cim \_ ManagedElement**](cim-managedelement.md) 實例的參考，以供收集 **cim \_ BaseMetricDefinition** 實例所定義的計量。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="b1ddb-112">*ManagedElements* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b1ddb-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ddb-113">成功時，可能會包含 [**CIM \_ ManagedElement**](cim-managedelement.md) 物件的參考，而這些物件是由 *定義* 參數所識別的計量可供收集。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="b1ddb-114">*DefinitionList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b1ddb-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ddb-115">成功時，可能會包含 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)物件之實例的參考，這些物件定義了針對 *Subject* 參數所識別之 [**cim \_ ManagedElement**](cim-managedelement.md)可收集的計量。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ddb-116">*MetricNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b1ddb-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ddb-117">成功時，每個陣列索引都應該包含 *DefinitionList* 參數的對應陣列索引所參考之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的 **名稱** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1ddb-118">*MetricCollectionEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b1ddb-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ddb-119">指出是否針對 managed 元素收集度量。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="b1ddb-120">**啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="b1ddb-121">**停** 用 (3) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b1ddb-122">**保留** (4) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b1ddb-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b1ddb-124">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="b1ddb-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b1ddb-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b1ddb-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1ddb-126">Return value</span></span>

<span data-ttu-id="b1ddb-127">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b1ddb-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b1ddb-128">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b1ddb-129">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b1ddb-130">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b1ddb-131">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b1ddb-132">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b1ddb-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b1ddb-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1ddb-133">Requirements</span></span>



| <span data-ttu-id="b1ddb-134">需求</span><span class="sxs-lookup"><span data-stu-id="b1ddb-134">Requirement</span></span> | <span data-ttu-id="b1ddb-135">值</span><span class="sxs-lookup"><span data-stu-id="b1ddb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ddb-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1ddb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ddb-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b1ddb-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b1ddb-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1ddb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ddb-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b1ddb-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b1ddb-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="b1ddb-140">Namespace</span></span><br/>                | <span data-ttu-id="b1ddb-141">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b1ddb-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b1ddb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b1ddb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1ddb-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b1ddb-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1ddb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ddb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1ddb-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1ddb-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b1ddb-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1ddb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ddb-147">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="b1ddb-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




