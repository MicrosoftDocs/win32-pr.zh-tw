---
description: 依類別控制度量。
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Msvm_MetricService 類別的 ControlMetricsByClass 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996970"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="fa2c6-103">Msvm MetricService 類別的 ControlMetricsByClass 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fa2c6-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="fa2c6-104">依類別控制度量。</span><span class="sxs-lookup"><span data-stu-id="fa2c6-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa2c6-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="fa2c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa2c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa2c6-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa2c6-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa2c6-108">識別將控制其計量的 CIM 類別。</span><span class="sxs-lookup"><span data-stu-id="fa2c6-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="fa2c6-109">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa2c6-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa2c6-110">識別將控制其計量的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 。</span><span class="sxs-lookup"><span data-stu-id="fa2c6-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="fa2c6-111">*MetricCollectionEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fa2c6-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa2c6-112">表示要在度量上執行的所需操作。</span><span class="sxs-lookup"><span data-stu-id="fa2c6-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="fa2c6-113">**啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="fa2c6-114">**停** 用 (3) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="fa2c6-115">**重設** (4) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fa2c6-116">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="fa2c6-117">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="fa2c6-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fa2c6-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="fa2c6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa2c6-119">Return value</span></span>

<span data-ttu-id="fa2c6-120">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="fa2c6-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="fa2c6-121">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fa2c6-122">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fa2c6-123">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fa2c6-124">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fa2c6-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="fa2c6-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fa2c6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa2c6-126">Requirements</span></span>



| <span data-ttu-id="fa2c6-127">需求</span><span class="sxs-lookup"><span data-stu-id="fa2c6-127">Requirement</span></span> | <span data-ttu-id="fa2c6-128">值</span><span class="sxs-lookup"><span data-stu-id="fa2c6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2c6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa2c6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2c6-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fa2c6-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fa2c6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa2c6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2c6-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fa2c6-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fa2c6-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa2c6-133">Namespace</span></span><br/>                | <span data-ttu-id="fa2c6-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa2c6-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fa2c6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fa2c6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa2c6-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fa2c6-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa2c6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fa2c6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa2c6-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa2c6-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa2c6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa2c6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2c6-140">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="fa2c6-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




