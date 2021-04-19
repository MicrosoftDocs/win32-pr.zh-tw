---
description: 代表 CIM AggregationMetricDefinition 實例所定義之度量的實例值 \_ 。
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: CIM_AggregationMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969315"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="87542-103">CIM \_ AggregationMetricValue 類別</span><span class="sxs-lookup"><span data-stu-id="87542-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="87542-104">代表 **CIM \_ AggregationMetricDefinition** 實例所定義之度量的實例值。</span><span class="sxs-lookup"><span data-stu-id="87542-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87542-105">語法</span><span class="sxs-lookup"><span data-stu-id="87542-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="87542-106">成員</span><span class="sxs-lookup"><span data-stu-id="87542-106">Members</span></span>

<span data-ttu-id="87542-107">**CIM \_ AggregationMetricValue** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="87542-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="87542-108">屬性</span><span class="sxs-lookup"><span data-stu-id="87542-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87542-109">屬性</span><span class="sxs-lookup"><span data-stu-id="87542-109">Properties</span></span>

<span data-ttu-id="87542-110">**CIM \_ AggregationMetricValue** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="87542-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87542-111">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="87542-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87542-112">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="87542-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="87542-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87542-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87542-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**") </span><span class="sxs-lookup"><span data-stu-id="87542-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="87542-115">代表計算匯總的持續時間。</span><span class="sxs-lookup"><span data-stu-id="87542-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="87542-116">套用彙總函式的監視間隔開始時間，是從 **AggregationTimestamp** 值減去 **AggregationDuration** 值來決定。</span><span class="sxs-lookup"><span data-stu-id="87542-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="87542-117">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="87542-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87542-118">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="87542-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="87542-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87542-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87542-120">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AggregationMetricValue**.**Duration**") </span><span class="sxs-lookup"><span data-stu-id="87542-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="87542-121">套用彙總函式以判斷度量實例值的時間。</span><span class="sxs-lookup"><span data-stu-id="87542-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="87542-122">這與建立實例的時間不同。</span><span class="sxs-lookup"><span data-stu-id="87542-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="87542-123">每當套用彙總函式來計算值時， **AggregationTimeStamp** 值就會變更。</span><span class="sxs-lookup"><span data-stu-id="87542-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87542-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="87542-124">Requirements</span></span>



| <span data-ttu-id="87542-125">需求</span><span class="sxs-lookup"><span data-stu-id="87542-125">Requirement</span></span> | <span data-ttu-id="87542-126">值</span><span class="sxs-lookup"><span data-stu-id="87542-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87542-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87542-127">Minimum supported client</span></span><br/> | <span data-ttu-id="87542-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="87542-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="87542-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87542-129">Minimum supported server</span></span><br/> | <span data-ttu-id="87542-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87542-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="87542-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="87542-131">Namespace</span></span><br/>                | <span data-ttu-id="87542-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="87542-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87542-133">MOF</span><span class="sxs-lookup"><span data-stu-id="87542-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87542-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="87542-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87542-135">DLL</span><span class="sxs-lookup"><span data-stu-id="87542-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87542-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87542-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87542-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87542-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87542-138">**CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="87542-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 

