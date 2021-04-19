---
description: 表示計量值物件與其度量定義之間的關聯。
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974669"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="61447-103">Msvm \_ MetricInstance 類別</span><span class="sxs-lookup"><span data-stu-id="61447-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="61447-104">表示計量值物件與其度量定義之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="61447-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="61447-105">此關聯會將 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 的實例系結至其 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)。</span><span class="sxs-lookup"><span data-stu-id="61447-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="61447-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="61447-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61447-107">語法</span><span class="sxs-lookup"><span data-stu-id="61447-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="61447-108">成員</span><span class="sxs-lookup"><span data-stu-id="61447-108">Members</span></span>

<span data-ttu-id="61447-109">**Msvm \_ MetricInstance** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="61447-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="61447-110">屬性</span><span class="sxs-lookup"><span data-stu-id="61447-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61447-111">屬性</span><span class="sxs-lookup"><span data-stu-id="61447-111">Properties</span></span>

<span data-ttu-id="61447-112">**Msvm \_ MetricInstance** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="61447-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61447-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="61447-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61447-114">資料類型： \* \* \* \* CIM \_ ManagedElement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="61447-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="61447-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61447-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61447-116">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="61447-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="61447-117">代表度量定義之 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="61447-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="61447-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="61447-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61447-119">資料類型： \* \* \* \* CIM \_ ManagedElement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="61447-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="61447-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61447-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61447-121">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="61447-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="61447-122">[**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)類別實例的參考，代表相依于前 **一個的度量。**</span><span class="sxs-lookup"><span data-stu-id="61447-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61447-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="61447-123">Requirements</span></span>



| <span data-ttu-id="61447-124">需求</span><span class="sxs-lookup"><span data-stu-id="61447-124">Requirement</span></span> | <span data-ttu-id="61447-125">值</span><span class="sxs-lookup"><span data-stu-id="61447-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61447-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61447-126">Minimum supported client</span></span><br/> | <span data-ttu-id="61447-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61447-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61447-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61447-128">Minimum supported server</span></span><br/> | <span data-ttu-id="61447-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61447-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61447-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="61447-130">Namespace</span></span><br/>                | <span data-ttu-id="61447-131">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="61447-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61447-132">MOF</span><span class="sxs-lookup"><span data-stu-id="61447-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61447-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="61447-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61447-134">DLL</span><span class="sxs-lookup"><span data-stu-id="61447-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61447-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61447-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




