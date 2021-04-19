---
description: 終結虛擬系統集合的現有快照集。 這個方法可能會損毀其他相依于受影響快照集的快照集。
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Msvm_CollectionSnapshotService 類別的 DestroySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969289"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="e938f-104">Msvm CollectionSnapshotService 類別的 DestroySnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e938f-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="e938f-105">終結虛擬系統集合的現有快照集。</span><span class="sxs-lookup"><span data-stu-id="e938f-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="e938f-106">這個方法可能會損毀其他相依于受影響快照集的快照集。</span><span class="sxs-lookup"><span data-stu-id="e938f-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="e938f-107">語法</span><span class="sxs-lookup"><span data-stu-id="e938f-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e938f-108">參數</span><span class="sxs-lookup"><span data-stu-id="e938f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e938f-109">*AffectedSnapshotCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e938f-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e938f-110">參考描述受影響之虛擬系統快照集集合的 [**CIM \_ 集合**](cim-collection.md) 。</span><span class="sxs-lookup"><span data-stu-id="e938f-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="e938f-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e938f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e938f-112">如果以非同步方式執行作業，則會傳回選擇性的參考。</span><span class="sxs-lookup"><span data-stu-id="e938f-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="e938f-113">如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="e938f-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e938f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e938f-114">Return value</span></span>

<span data-ttu-id="e938f-115">成功時，會傳回 0 (完成) 或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e938f-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e938f-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e938f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="e938f-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="e938f-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="e938f-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="e938f-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="e938f-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-122">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="e938f-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e938f-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e938f-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="e938f-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e938f-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="e938f-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e938f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e938f-127">Requirements</span></span>



| <span data-ttu-id="e938f-128">需求</span><span class="sxs-lookup"><span data-stu-id="e938f-128">Requirement</span></span> | <span data-ttu-id="e938f-129">值</span><span class="sxs-lookup"><span data-stu-id="e938f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e938f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e938f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e938f-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e938f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e938f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e938f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e938f-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e938f-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e938f-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="e938f-134">Namespace</span></span><br/>                | <span data-ttu-id="e938f-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e938f-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e938f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e938f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e938f-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e938f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e938f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e938f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e938f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e938f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e938f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e938f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e938f-141">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="e938f-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




