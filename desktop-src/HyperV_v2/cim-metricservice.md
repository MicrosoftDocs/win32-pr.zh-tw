---
description: 管理受控元素的度量。
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: CIM_MetricService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978992"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="85f34-103">CIM \_ MetricService 類別</span><span class="sxs-lookup"><span data-stu-id="85f34-103">CIM\_MetricService class</span></span>

<span data-ttu-id="85f34-104">管理受控元素的度量。</span><span class="sxs-lookup"><span data-stu-id="85f34-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f34-105">語法</span><span class="sxs-lookup"><span data-stu-id="85f34-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="85f34-106">成員</span><span class="sxs-lookup"><span data-stu-id="85f34-106">Members</span></span>

<span data-ttu-id="85f34-107">**CIM \_ MetricService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="85f34-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="85f34-108">方法</span><span class="sxs-lookup"><span data-stu-id="85f34-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="85f34-109">方法</span><span class="sxs-lookup"><span data-stu-id="85f34-109">Methods</span></span>

<span data-ttu-id="85f34-110">**CIM \_ MetricService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="85f34-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="85f34-111">方法</span><span class="sxs-lookup"><span data-stu-id="85f34-111">Method</span></span>                                                                   | <span data-ttu-id="85f34-112">描述</span><span class="sxs-lookup"><span data-stu-id="85f34-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85f34-113">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="85f34-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="85f34-114">啟用及停用計量收集。</span><span class="sxs-lookup"><span data-stu-id="85f34-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="85f34-115">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="85f34-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="85f34-116">啟用及停用類別的計量集合。</span><span class="sxs-lookup"><span data-stu-id="85f34-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="85f34-117">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="85f34-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="85f34-118">指定收集計量的時機。</span><span class="sxs-lookup"><span data-stu-id="85f34-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="85f34-119">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="85f34-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="85f34-120">抓取度量值的篩選清單。</span><span class="sxs-lookup"><span data-stu-id="85f34-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="85f34-121">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="85f34-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="85f34-122">指出是否已針對指定的 managed 專案啟用計量收集，並指出可針對每個 managed 元素收集的計量。</span><span class="sxs-lookup"><span data-stu-id="85f34-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="85f34-123">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="85f34-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="85f34-124">指出可針對 CIM 類別的所有實例收集哪些計量。</span><span class="sxs-lookup"><span data-stu-id="85f34-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="85f34-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="85f34-125">Requirements</span></span>



| <span data-ttu-id="85f34-126">需求</span><span class="sxs-lookup"><span data-stu-id="85f34-126">Requirement</span></span> | <span data-ttu-id="85f34-127">值</span><span class="sxs-lookup"><span data-stu-id="85f34-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f34-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85f34-128">Minimum supported client</span></span><br/> | <span data-ttu-id="85f34-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="85f34-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="85f34-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85f34-130">Minimum supported server</span></span><br/> | <span data-ttu-id="85f34-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85f34-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="85f34-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="85f34-132">Namespace</span></span><br/>                | <span data-ttu-id="85f34-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="85f34-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="85f34-134">MOF</span><span class="sxs-lookup"><span data-stu-id="85f34-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85f34-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="85f34-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85f34-136">DLL</span><span class="sxs-lookup"><span data-stu-id="85f34-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85f34-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85f34-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85f34-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85f34-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f34-139">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="85f34-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




