---
description: 表示計量值實例與度量定義之間的關聯。
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: CIM_MetricInstance 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: defba85f46e037c226a96cfaa8ffac44b99244f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985198"
---
# <a name="cim_metricinstance-class"></a><span data-ttu-id="4c09d-103">CIM \_ MetricInstance 類別</span><span class="sxs-lookup"><span data-stu-id="4c09d-103">CIM\_MetricInstance class</span></span>

<span data-ttu-id="4c09d-104">表示計量值實例與度量定義之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4c09d-104">Represents an association between an instance of a metric value and a metric definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c09d-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c09d-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4c09d-106">成員</span><span class="sxs-lookup"><span data-stu-id="4c09d-106">Members</span></span>

<span data-ttu-id="4c09d-107">**CIM \_ MetricInstance** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4c09d-107">The **CIM\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="4c09d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="4c09d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c09d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4c09d-109">Properties</span></span>

<span data-ttu-id="4c09d-110">**CIM \_ MetricInstance** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4c09d-110">The **CIM\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c09d-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="4c09d-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c09d-112">資料類型： **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="4c09d-112">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="4c09d-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c09d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c09d-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="4c09d-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4c09d-115">度量值的定義。</span><span class="sxs-lookup"><span data-stu-id="4c09d-115">The definition of the metric value.</span></span>

</dd> <dt>

<span data-ttu-id="4c09d-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4c09d-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c09d-117">資料類型： **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="4c09d-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="4c09d-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c09d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c09d-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="4c09d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4c09d-120">與度量定義相關聯的度量值。</span><span class="sxs-lookup"><span data-stu-id="4c09d-120">The metric value that is associated with the metric definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c09d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c09d-121">Requirements</span></span>



| <span data-ttu-id="4c09d-122">需求</span><span class="sxs-lookup"><span data-stu-id="4c09d-122">Requirement</span></span> | <span data-ttu-id="4c09d-123">值</span><span class="sxs-lookup"><span data-stu-id="4c09d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c09d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c09d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c09d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4c09d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4c09d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c09d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c09d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c09d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4c09d-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c09d-128">Namespace</span></span><br/>                | <span data-ttu-id="4c09d-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="4c09d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4c09d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4c09d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c09d-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4c09d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c09d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4c09d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c09d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c09d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4c09d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c09d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c09d-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="4c09d-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

