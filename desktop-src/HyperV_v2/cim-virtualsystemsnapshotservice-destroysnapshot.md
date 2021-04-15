---
description: 終結現有的虛擬系統快照。 這個方法可能會損毀其他相依于受影響快照集的快照集。
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: CIM_VirtualSystemSnapshotService 類別的 DestroySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511844"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="b6b52-104">CIM VirtualSystemSnapshotService 類別的 DestroySnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b6b52-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="b6b52-105">終結現有的虛擬系統快照。</span><span class="sxs-lookup"><span data-stu-id="b6b52-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="b6b52-106">這個方法可能會損毀其他相依于受影響快照集的快照集。</span><span class="sxs-lookup"><span data-stu-id="b6b52-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b52-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6b52-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b6b52-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6b52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b52-109">*AffectedSnapshot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6b52-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b52-110">受影響之虛擬系統快照集的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="b6b52-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="b6b52-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b6b52-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b52-112">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="b6b52-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="b6b52-113">此參數在 Windows 8.1 中是讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="b6b52-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b52-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6b52-114">Return value</span></span>

<span data-ttu-id="b6b52-115">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6b52-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b6b52-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b6b52-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b6b52-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="b6b52-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="b6b52-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="b6b52-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="b6b52-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-122">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="b6b52-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b6b52-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b6b52-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="b6b52-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b6b52-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b6b52-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b6b52-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6b52-127">Requirements</span></span>



| <span data-ttu-id="b6b52-128">需求</span><span class="sxs-lookup"><span data-stu-id="b6b52-128">Requirement</span></span> | <span data-ttu-id="b6b52-129">值</span><span class="sxs-lookup"><span data-stu-id="b6b52-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b52-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6b52-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b52-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b6b52-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b6b52-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6b52-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b52-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b6b52-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b6b52-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="b6b52-134">Namespace</span></span><br/>                | <span data-ttu-id="b6b52-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6b52-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6b52-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b6b52-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6b52-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b6b52-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6b52-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b52-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b52-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6b52-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6b52-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6b52-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b52-141">**CIM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="b6b52-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




