---
description: 取得度量值。
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Msvm_MetricService 類別的 GetMetricValues 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987375"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="84032-103">Msvm MetricService 類別的 GetMetricValues 方法 \_</span><span class="sxs-lookup"><span data-stu-id="84032-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="84032-104">取得度量值。</span><span class="sxs-lookup"><span data-stu-id="84032-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="84032-105">語法</span><span class="sxs-lookup"><span data-stu-id="84032-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="84032-106">參數</span><span class="sxs-lookup"><span data-stu-id="84032-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84032-107">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84032-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84032-108">識別將傳回其計量的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 。</span><span class="sxs-lookup"><span data-stu-id="84032-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="84032-109">*範圍* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84032-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84032-110">識別如何選取實例。</span><span class="sxs-lookup"><span data-stu-id="84032-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="84032-111">排序值實例的演算法是特定的度量定義。</span><span class="sxs-lookup"><span data-stu-id="84032-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="84032-112">**最小** (2) </span><span class="sxs-lookup"><span data-stu-id="84032-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="84032-113">**最大** (3) </span><span class="sxs-lookup"><span data-stu-id="84032-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="84032-114">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="84032-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="84032-115">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="84032-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="84032-116">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84032-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84032-117">識別方法所傳回的最大實例數目。</span><span class="sxs-lookup"><span data-stu-id="84032-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="84032-118">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="84032-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84032-119">當方法成功完成時，會包含 [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md)實例的參考，並根據輸入參數的值進行篩選。</span><span class="sxs-lookup"><span data-stu-id="84032-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84032-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="84032-120">Return value</span></span>

<span data-ttu-id="84032-121">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="84032-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="84032-122">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="84032-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84032-123">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="84032-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84032-124">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="84032-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84032-125">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="84032-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84032-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="84032-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84032-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="84032-127">Requirements</span></span>



| <span data-ttu-id="84032-128">需求</span><span class="sxs-lookup"><span data-stu-id="84032-128">Requirement</span></span> | <span data-ttu-id="84032-129">值</span><span class="sxs-lookup"><span data-stu-id="84032-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84032-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84032-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84032-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="84032-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="84032-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84032-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84032-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84032-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="84032-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="84032-134">Namespace</span></span><br/>                | <span data-ttu-id="84032-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="84032-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84032-136">MOF</span><span class="sxs-lookup"><span data-stu-id="84032-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84032-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="84032-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84032-138">DLL</span><span class="sxs-lookup"><span data-stu-id="84032-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84032-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84032-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84032-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84032-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84032-141">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="84032-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




