---
description: 將現有的虛擬系統快照集轉換為參考點。 快照集會被刪除做為副作用。 只有修復快照集可以轉換成參考點。
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Msvm_VirtualSystemSnapshotService 類別的 ConvertToReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972001"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="7d797-105">Msvm VirtualSystemSnapshotService 類別的 ConvertToReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7d797-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="7d797-106">將現有的虛擬系統快照集轉換為參考點。</span><span class="sxs-lookup"><span data-stu-id="7d797-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="7d797-107">快照集會被刪除做為副作用。</span><span class="sxs-lookup"><span data-stu-id="7d797-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="7d797-108">只有修復快照集可以轉換成參考點。</span><span class="sxs-lookup"><span data-stu-id="7d797-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d797-109">語法</span><span class="sxs-lookup"><span data-stu-id="7d797-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7d797-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d797-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d797-111">*AffectedSnapshot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d797-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d797-112">受影響之虛擬系統快照集的參考。</span><span class="sxs-lookup"><span data-stu-id="7d797-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7d797-113">*ReferencePointSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d797-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d797-114">參數設定。</span><span class="sxs-lookup"><span data-stu-id="7d797-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="7d797-115">*ResultingReferencePoint* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7d797-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d797-116">產生的虛擬系統參考點</span><span class="sxs-lookup"><span data-stu-id="7d797-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="7d797-117">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d797-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d797-118">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="7d797-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d797-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d797-119">Return value</span></span>

<span data-ttu-id="7d797-120">成功時傳回 0;否則，會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="7d797-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="7d797-121">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="7d797-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-122">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="7d797-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-123">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="7d797-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-124">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="7d797-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-125">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="7d797-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-126">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="7d797-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-127">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="7d797-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-128">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="7d797-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-129">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="7d797-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-130">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="7d797-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7d797-131">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="7d797-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7d797-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d797-132">Requirements</span></span>



| <span data-ttu-id="7d797-133">需求</span><span class="sxs-lookup"><span data-stu-id="7d797-133">Requirement</span></span> | <span data-ttu-id="7d797-134">值</span><span class="sxs-lookup"><span data-stu-id="7d797-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d797-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d797-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7d797-136">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d797-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7d797-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d797-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7d797-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7d797-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7d797-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d797-139">Namespace</span></span><br/>                | <span data-ttu-id="7d797-140">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="7d797-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7d797-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7d797-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d797-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7d797-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d797-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7d797-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d797-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d797-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d797-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d797-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d797-146">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="7d797-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




