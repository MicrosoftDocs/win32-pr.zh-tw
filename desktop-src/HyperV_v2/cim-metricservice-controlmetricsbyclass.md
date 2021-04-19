---
description: 啟用及停用計量收集。
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: CIM_MetricService 類別的 ControlMetricsByClass 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 46e961b298c212a7635599818fb1f7079805372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976930"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="df3d4-103">CIM MetricService 類別的 ControlMetricsByClass 方法 \_</span><span class="sxs-lookup"><span data-stu-id="df3d4-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="df3d4-104">啟用及停用計量收集。**ControlMetricsByClass** 用來控制每個類別實例的集合，或類別的所有實例之特定度量集合的集合。</span><span class="sxs-lookup"><span data-stu-id="df3d4-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="df3d4-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="df3d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="df3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df3d4-107">主旨 \[在\]</span><span class="sxs-lookup"><span data-stu-id="df3d4-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df3d4-108">識別將控制其計量的 [**CIM \_ ManagedElement**](cim-managedelement.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="df3d4-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="df3d4-109">*定義* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df3d4-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df3d4-110">識別將控制其計量的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 。</span><span class="sxs-lookup"><span data-stu-id="df3d4-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="df3d4-111">*MetricCollectionEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df3d4-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df3d4-112">表示要在度量上執行的所需操作。</span><span class="sxs-lookup"><span data-stu-id="df3d4-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="df3d4-113">**啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="df3d4-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="df3d4-114">**停** 用 (3) </span><span class="sxs-lookup"><span data-stu-id="df3d4-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="df3d4-115">**重設** (4) </span><span class="sxs-lookup"><span data-stu-id="df3d4-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="df3d4-116">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="df3d4-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="df3d4-117">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="df3d4-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="df3d4-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="df3d4-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="df3d4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="df3d4-119">Return value</span></span>

<span data-ttu-id="df3d4-120">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="df3d4-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="df3d4-121">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="df3d4-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df3d4-122">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="df3d4-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df3d4-123">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="df3d4-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="df3d4-124">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="df3d4-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="df3d4-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="df3d4-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="df3d4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="df3d4-126">Requirements</span></span>



| <span data-ttu-id="df3d4-127">需求</span><span class="sxs-lookup"><span data-stu-id="df3d4-127">Requirement</span></span> | <span data-ttu-id="df3d4-128">值</span><span class="sxs-lookup"><span data-stu-id="df3d4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df3d4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df3d4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="df3d4-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="df3d4-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="df3d4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df3d4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="df3d4-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df3d4-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="df3d4-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="df3d4-133">Namespace</span></span><br/>                | <span data-ttu-id="df3d4-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="df3d4-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df3d4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="df3d4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df3d4-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="df3d4-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df3d4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="df3d4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df3d4-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df3d4-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df3d4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df3d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3d4-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="df3d4-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




