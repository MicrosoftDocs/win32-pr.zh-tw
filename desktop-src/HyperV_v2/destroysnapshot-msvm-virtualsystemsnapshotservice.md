---
description: 終結現有的虛擬機器快照集。
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Msvm_VirtualSystemSnapshotService 類別的 DestroySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852115"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="8a61d-103">Msvm VirtualSystemSnapshotService 類別的 DestroySnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8a61d-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="8a61d-104">終結現有的虛擬機器快照集。</span><span class="sxs-lookup"><span data-stu-id="8a61d-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="8a61d-105">這個方法可能會損毀其他相依于受影響快照集的快照集。</span><span class="sxs-lookup"><span data-stu-id="8a61d-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a61d-106">語法</span><span class="sxs-lookup"><span data-stu-id="8a61d-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8a61d-107">參數</span><span class="sxs-lookup"><span data-stu-id="8a61d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a61d-108">*AffectedSnapshot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a61d-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a61d-109">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))參考，代表要終結的虛擬機器快照集。</span><span class="sxs-lookup"><span data-stu-id="8a61d-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="8a61d-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a61d-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a61d-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8a61d-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a61d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a61d-112">Return value</span></span>

<span data-ttu-id="8a61d-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8a61d-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8a61d-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8a61d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8a61d-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="8a61d-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="8a61d-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="8a61d-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="8a61d-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-120">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="8a61d-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8a61d-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8a61d-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-123">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="8a61d-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8a61d-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="8a61d-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a61d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a61d-125">Requirements</span></span>



| <span data-ttu-id="8a61d-126">需求</span><span class="sxs-lookup"><span data-stu-id="8a61d-126">Requirement</span></span> | <span data-ttu-id="8a61d-127">值</span><span class="sxs-lookup"><span data-stu-id="8a61d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a61d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a61d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8a61d-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a61d-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a61d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a61d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8a61d-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a61d-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a61d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="8a61d-132">Namespace</span></span><br/>                | <span data-ttu-id="8a61d-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8a61d-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a61d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8a61d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a61d-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8a61d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a61d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8a61d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a61d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a61d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a61d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a61d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a61d-139">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="8a61d-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="8a61d-140">**RemoveVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="8a61d-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

