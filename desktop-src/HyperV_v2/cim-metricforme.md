---
description: 表示針對 managed 元素收集度量值的關聯。
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: CIM_MetricForME 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984586"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="eb2c6-103">CIM \_ MetricForME 類別</span><span class="sxs-lookup"><span data-stu-id="eb2c6-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="eb2c6-104">表示針對 managed 元素收集度量值的關聯。</span><span class="sxs-lookup"><span data-stu-id="eb2c6-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb2c6-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="eb2c6-106">成員</span><span class="sxs-lookup"><span data-stu-id="eb2c6-106">Members</span></span>

<span data-ttu-id="eb2c6-107">**CIM \_ MetricForME** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eb2c6-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="eb2c6-108">屬性</span><span class="sxs-lookup"><span data-stu-id="eb2c6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb2c6-109">屬性</span><span class="sxs-lookup"><span data-stu-id="eb2c6-109">Properties</span></span>

<span data-ttu-id="eb2c6-110">**CIM \_ MetricForME** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eb2c6-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb2c6-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="eb2c6-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb2c6-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="eb2c6-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="eb2c6-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb2c6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb2c6-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="eb2c6-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="eb2c6-115">關聯中的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="eb2c6-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="eb2c6-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="eb2c6-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb2c6-117">資料類型： **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="eb2c6-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="eb2c6-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb2c6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb2c6-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="eb2c6-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="eb2c6-120">關聯中的度量值。</span><span class="sxs-lookup"><span data-stu-id="eb2c6-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb2c6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb2c6-121">Requirements</span></span>



| <span data-ttu-id="eb2c6-122">需求</span><span class="sxs-lookup"><span data-stu-id="eb2c6-122">Requirement</span></span> | <span data-ttu-id="eb2c6-123">值</span><span class="sxs-lookup"><span data-stu-id="eb2c6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2c6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb2c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2c6-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eb2c6-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="eb2c6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb2c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2c6-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb2c6-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="eb2c6-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb2c6-128">Namespace</span></span><br/>                | <span data-ttu-id="eb2c6-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb2c6-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eb2c6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="eb2c6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb2c6-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="eb2c6-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb2c6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eb2c6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb2c6-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb2c6-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb2c6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb2c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb2c6-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="eb2c6-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

