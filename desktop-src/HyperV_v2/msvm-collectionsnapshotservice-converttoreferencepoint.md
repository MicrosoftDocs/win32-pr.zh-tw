---
description: 將現有的集合快照集轉換為參考點集合。 快照集集合被刪除為副作用。 只有修復快照集可以轉換成參考點。
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Msvm_CollectionSnapshotService 類別的 ConvertToReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852968"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="2b740-105">Msvm CollectionSnapshotService 類別的 ConvertToReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2b740-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="2b740-106">將現有的集合快照集轉換為參考點集合。</span><span class="sxs-lookup"><span data-stu-id="2b740-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="2b740-107">快照集集合被刪除為副作用。</span><span class="sxs-lookup"><span data-stu-id="2b740-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="2b740-108">只有修復快照集可以轉換成參考點。</span><span class="sxs-lookup"><span data-stu-id="2b740-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b740-109">語法</span><span class="sxs-lookup"><span data-stu-id="2b740-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2b740-110">參數</span><span class="sxs-lookup"><span data-stu-id="2b740-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b740-111">*AffectedSnapshotCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b740-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b740-112">參考包含受影響之虛擬系統快照集集合的 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 。</span><span class="sxs-lookup"><span data-stu-id="2b740-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="2b740-113">*ResultingReferencePointCollection* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2b740-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b740-114">[**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)的參考，其中包含產生的虛擬系統參考點集合</span><span class="sxs-lookup"><span data-stu-id="2b740-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="2b740-115">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b740-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b740-116">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="2b740-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b740-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b740-117">Return value</span></span>

<span data-ttu-id="2b740-118">成功時，會傳回 0 (完成) 或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2b740-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2b740-119">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2b740-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-120">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2b740-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-121">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="2b740-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-122">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="2b740-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-123">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="2b740-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-124">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="2b740-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-125">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="2b740-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-126">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2b740-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-127">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2b740-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-128">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="2b740-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2b740-129">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="2b740-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2b740-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b740-130">Requirements</span></span>



| <span data-ttu-id="2b740-131">需求</span><span class="sxs-lookup"><span data-stu-id="2b740-131">Requirement</span></span> | <span data-ttu-id="2b740-132">值</span><span class="sxs-lookup"><span data-stu-id="2b740-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b740-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b740-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2b740-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b740-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2b740-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b740-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2b740-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2b740-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2b740-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="2b740-137">Namespace</span></span><br/>                | <span data-ttu-id="2b740-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b740-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b740-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2b740-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b740-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2b740-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b740-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2b740-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b740-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b740-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b740-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b740-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b740-144">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="2b740-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




