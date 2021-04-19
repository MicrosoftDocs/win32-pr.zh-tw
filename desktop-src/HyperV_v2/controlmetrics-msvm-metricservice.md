---
description: 用來控制 managed 元素或元素的計量集合。
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Msvm_MetricService 類別的 ControlMetrics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971474"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="b538a-103">Msvm MetricService 類別的 ControlMetrics 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b538a-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="b538a-104">用來控制 managed 元素或元素的計量集合。</span><span class="sxs-lookup"><span data-stu-id="b538a-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b538a-105">語法</span><span class="sxs-lookup"><span data-stu-id="b538a-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="b538a-106">參數</span><span class="sxs-lookup"><span data-stu-id="b538a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b538a-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="b538a-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b538a-108">[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)實例，識別將收集計量的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="b538a-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="b538a-109">如果此參數為 **Null**，則會收集與 *定義* 參數相關聯之所有 managed 元素的度量。</span><span class="sxs-lookup"><span data-stu-id="b538a-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="b538a-110">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b538a-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b538a-111">指定將收集哪些計量的 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="b538a-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="b538a-112">如果此參數為 **Null**，則會收集與 *Subject* 參數所識別之 managed 元素相關聯之所有定義的計量。</span><span class="sxs-lookup"><span data-stu-id="b538a-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="b538a-113">*MetricCollectionEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b538a-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b538a-114">指定要在計量集合上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="b538a-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="b538a-115">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="b538a-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="b538a-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="b538a-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b538a-117">啟用計量收集。</span><span class="sxs-lookup"><span data-stu-id="b538a-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="b538a-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (3) </span><span class="sxs-lookup"><span data-stu-id="b538a-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b538a-119">停用計量收集。</span><span class="sxs-lookup"><span data-stu-id="b538a-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="b538a-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (4) </span><span class="sxs-lookup"><span data-stu-id="b538a-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b538a-121">重設度量值。</span><span class="sxs-lookup"><span data-stu-id="b538a-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b538a-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b538a-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b538a-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b538a-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="b538a-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b538a-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b538a-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="b538a-125">Return value</span></span>

<span data-ttu-id="b538a-126">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b538a-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b538a-127">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="b538a-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b538a-128">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b538a-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b538a-129">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="b538a-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b538a-130">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b538a-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b538a-131">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b538a-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b538a-132">備註</span><span class="sxs-lookup"><span data-stu-id="b538a-132">Remarks</span></span>

<span data-ttu-id="b538a-133">在下列實例中，這個方法將會失敗：</span><span class="sxs-lookup"><span data-stu-id="b538a-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="b538a-134">*主體* 和 *定義* 參數都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b538a-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="b538a-135">主旨 *和\*\*定義* 參數都不是 **Null** ，而且沒有關聯兩個實例的 [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)實例。</span><span class="sxs-lookup"><span data-stu-id="b538a-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="b538a-136">*定義* 參數是 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)實例的參考，該實例與 [**Msvm \_ MetricService**](msvm-metricservice.md)之間的關聯性不會透過 [**Msvm \_ ServiceAffectsElement**](msvm-serviceaffectselement.md)。</span><span class="sxs-lookup"><span data-stu-id="b538a-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b538a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="b538a-137">Requirements</span></span>



| <span data-ttu-id="b538a-138">需求</span><span class="sxs-lookup"><span data-stu-id="b538a-138">Requirement</span></span> | <span data-ttu-id="b538a-139">值</span><span class="sxs-lookup"><span data-stu-id="b538a-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b538a-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b538a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b538a-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b538a-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b538a-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b538a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b538a-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b538a-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b538a-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="b538a-144">Namespace</span></span><br/>                | <span data-ttu-id="b538a-145">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b538a-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b538a-146">MOF</span><span class="sxs-lookup"><span data-stu-id="b538a-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b538a-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b538a-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b538a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b538a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b538a-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b538a-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b538a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b538a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b538a-151">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="b538a-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

