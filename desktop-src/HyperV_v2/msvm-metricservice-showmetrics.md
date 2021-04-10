---
description: 顯示指定的計量。
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Msvm_MetricService 類別的 ShowMetrics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852391"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="b3a63-103">Msvm MetricService 類別的 ShowMetrics 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b3a63-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="b3a63-104">顯示指定的計量。</span><span class="sxs-lookup"><span data-stu-id="b3a63-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a63-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3a63-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b3a63-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3a63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a63-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3a63-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a63-108">Subject 參數會識別 [**cim \_ managedelement**](cim-managedelement.md) 的實例，該實例的方法會傳回 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例的參考，以定義要為 **cim \_ ManagedElement** 所捕獲的度量。</span><span class="sxs-lookup"><span data-stu-id="b3a63-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="b3a63-109">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3a63-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a63-110">定義參數會識別 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="b3a63-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="b3a63-111">方法會傳回 [**cim \_ ManagedElement**](cim-managedelement.md) 實例的參考，以供收集 **cim \_ BaseMetricDefinition** 實例所定義的計量。</span><span class="sxs-lookup"><span data-stu-id="b3a63-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="b3a63-112">*ManagedElements* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3a63-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a63-113">當方法成功完成時， *ManagedElements* \[ \] 參數可能會包含 [**CIM \_ ManagedElement**](cim-managedelement.md)的參考，而這些受 *定義* 參數所識別的度量可供收集。</span><span class="sxs-lookup"><span data-stu-id="b3a63-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="b3a63-114">*DefinitionList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3a63-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a63-115">當方法成功完成時， *DefinitionList* 參數可能會包含 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的參考，這些實例會定義可供 *主體* 參數所識別之 [**cim \_ ManagedElement**](cim-managedelement.md)收集的計量。</span><span class="sxs-lookup"><span data-stu-id="b3a63-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b3a63-116">*MetricNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3a63-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a63-117">當方法成功完成時， *MetricNames* 參數的每個陣列索引都應該包含 *DefinitionList* 參數的對應陣列索引所參考之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的名稱屬性值。</span><span class="sxs-lookup"><span data-stu-id="b3a63-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b3a63-118">*MetricCollectionEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3a63-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a63-119">*MetricCollectionEnabled* 參數會指出是否正在為 managed 元素收集度量。</span><span class="sxs-lookup"><span data-stu-id="b3a63-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="b3a63-120">**啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="b3a63-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="b3a63-121">**停** 用 (3) </span><span class="sxs-lookup"><span data-stu-id="b3a63-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b3a63-122">**保留** (4) </span><span class="sxs-lookup"><span data-stu-id="b3a63-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b3a63-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b3a63-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b3a63-124">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b3a63-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="b3a63-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b3a63-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b3a63-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3a63-126">Return value</span></span>

<span data-ttu-id="b3a63-127">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b3a63-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b3a63-128">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="b3a63-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b3a63-129">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b3a63-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b3a63-130">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="b3a63-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b3a63-131">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b3a63-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b3a63-132">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b3a63-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b3a63-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3a63-133">Requirements</span></span>



| <span data-ttu-id="b3a63-134">需求</span><span class="sxs-lookup"><span data-stu-id="b3a63-134">Requirement</span></span> | <span data-ttu-id="b3a63-135">值</span><span class="sxs-lookup"><span data-stu-id="b3a63-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a63-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3a63-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a63-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b3a63-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b3a63-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3a63-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a63-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b3a63-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b3a63-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3a63-140">Namespace</span></span><br/>                | <span data-ttu-id="b3a63-141">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b3a63-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b3a63-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b3a63-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3a63-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b3a63-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3a63-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b3a63-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3a63-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3a63-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3a63-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3a63-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a63-147">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="b3a63-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




