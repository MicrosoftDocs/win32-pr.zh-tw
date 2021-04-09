---
description: 建立虛擬系統集合的快照集。
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Msvm_CollectionSnapshotService 類別的 >icloudblob.createsnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692255"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="b718e-103">Msvm CollectionSnapshotService 類別的 >icloudblob.createsnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b718e-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="b718e-104">建立虛擬系統集合的快照集。</span><span class="sxs-lookup"><span data-stu-id="b718e-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b718e-105">語法</span><span class="sxs-lookup"><span data-stu-id="b718e-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b718e-106">參數</span><span class="sxs-lookup"><span data-stu-id="b718e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b718e-107">*集合* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b718e-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b718e-108">參考描述受影響之虛擬系統集合的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 。</span><span class="sxs-lookup"><span data-stu-id="b718e-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="b718e-109">*SnapshotSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b718e-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b718e-110">包含參數設定。</span><span class="sxs-lookup"><span data-stu-id="b718e-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="b718e-111">*SnapshotType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b718e-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b718e-112">要求的快照集類型：</span><span class="sxs-lookup"><span data-stu-id="b718e-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b718e-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b718e-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="b718e-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**標準快照** (1) </span><span class="sxs-lookup"><span data-stu-id="b718e-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b718e-115">虛擬系統的標準快照集。</span><span class="sxs-lookup"><span data-stu-id="b718e-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="b718e-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**修復快照** (2) </span><span class="sxs-lookup"><span data-stu-id="b718e-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b718e-117">復原案例的快照，包括容錯移轉複寫和備份。</span><span class="sxs-lookup"><span data-stu-id="b718e-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b718e-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b718e-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="b718e-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b718e-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b718e-120">*ResultingSnapshotCollection* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b718e-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b718e-121">成功時，傳回包含虛擬系統快照 [**集的 CIM \_ 集合**](cim-collection.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="b718e-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="b718e-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b718e-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b718e-123">如果以非同步方式執行作業，則會傳回選擇性的參考。</span><span class="sxs-lookup"><span data-stu-id="b718e-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="b718e-124">如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="b718e-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b718e-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="b718e-125">Return value</span></span>

<span data-ttu-id="b718e-126">成功時，會傳回 0 (完成) 或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b718e-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b718e-127">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b718e-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-128">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b718e-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-129">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="b718e-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-130">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="b718e-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-131">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="b718e-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-132">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="b718e-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-133">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="b718e-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-134">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b718e-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-135">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b718e-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-136">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="b718e-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b718e-137">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b718e-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b718e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b718e-138">Requirements</span></span>



| <span data-ttu-id="b718e-139">需求</span><span class="sxs-lookup"><span data-stu-id="b718e-139">Requirement</span></span> | <span data-ttu-id="b718e-140">值</span><span class="sxs-lookup"><span data-stu-id="b718e-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b718e-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b718e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b718e-142">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b718e-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b718e-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b718e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b718e-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b718e-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b718e-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="b718e-145">Namespace</span></span><br/>                | <span data-ttu-id="b718e-146">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b718e-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b718e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b718e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b718e-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b718e-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b718e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b718e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b718e-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b718e-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b718e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b718e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b718e-152">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="b718e-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




