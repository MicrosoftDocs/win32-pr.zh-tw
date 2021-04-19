---
description: 建立虛擬系統的參考點。
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Msvm_VirtualSystemReferencePointService 類別的 CreateReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986013"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="e423b-103">Msvm VirtualSystemReferencePointService 類別的 CreateReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e423b-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="e423b-104">建立虛擬系統的參考點。</span><span class="sxs-lookup"><span data-stu-id="e423b-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e423b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e423b-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e423b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e423b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e423b-107">*AffectedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e423b-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e423b-108">參考受影響之虛擬系統的 [**Msvm \_**](msvm-computersystem.md) 系統。</span><span class="sxs-lookup"><span data-stu-id="e423b-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="e423b-109">*ReferencePointSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e423b-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e423b-110">包含參數設定。</span><span class="sxs-lookup"><span data-stu-id="e423b-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="e423b-111">*ReferencePointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e423b-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e423b-112">要求的參考點類型：</span><span class="sxs-lookup"><span data-stu-id="e423b-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="e423b-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>以 **記錄為基礎** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e423b-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e423b-114">以 Hyper-v 複本記錄檔追蹤為基礎。</span><span class="sxs-lookup"><span data-stu-id="e423b-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="e423b-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**依** (1) 的 .rct</span><span class="sxs-lookup"><span data-stu-id="e423b-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e423b-116">以虛擬磁片的復原變更追蹤為基礎。</span><span class="sxs-lookup"><span data-stu-id="e423b-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e423b-117">*ResultingReferencePoint* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e423b-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e423b-118">產生的虛擬系統參考點</span><span class="sxs-lookup"><span data-stu-id="e423b-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="e423b-119">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e423b-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e423b-120">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="e423b-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="e423b-121">在此情況下， [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 類別的實例（代表新的虛擬系統參考點）會透過 [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) 關聯來呈現，而 **AffectedElement** 屬性的值則是參考 **Msvm \_ VirtualSystemReferencePoint** 類別的新實例，代表虛擬系統參考點，而 **ElementEffects** 的值設定為 5 (建立) 。</span><span class="sxs-lookup"><span data-stu-id="e423b-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e423b-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e423b-122">Return value</span></span>

<span data-ttu-id="e423b-123">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e423b-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e423b-124">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e423b-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-125">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="e423b-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-126">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="e423b-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-127">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="e423b-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-128">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="e423b-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-129">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="e423b-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-130">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="e423b-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-131">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e423b-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-132">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e423b-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-133">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="e423b-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e423b-134">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="e423b-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e423b-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e423b-135">Requirements</span></span>



| <span data-ttu-id="e423b-136">需求</span><span class="sxs-lookup"><span data-stu-id="e423b-136">Requirement</span></span> | <span data-ttu-id="e423b-137">值</span><span class="sxs-lookup"><span data-stu-id="e423b-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e423b-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e423b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e423b-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e423b-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e423b-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e423b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e423b-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e423b-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e423b-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="e423b-142">Namespace</span></span><br/>                | <span data-ttu-id="e423b-143">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e423b-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e423b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e423b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e423b-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e423b-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e423b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e423b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e423b-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e423b-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e423b-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e423b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e423b-149">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="e423b-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




