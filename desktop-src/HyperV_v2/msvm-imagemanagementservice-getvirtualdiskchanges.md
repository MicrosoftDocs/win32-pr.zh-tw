---
description: 從提供的復原變更追蹤識別碼或 VHDSet 快照集識別碼之後，抓取虛擬磁片指定區域的變更清單。
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Msvm_ImageManagementService 類別的 GetVirtualDiskChanges 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971029"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ab27c-103">Msvm ImageManagementService 類別的 GetVirtualDiskChanges 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ab27c-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ab27c-104">從提供的復原變更追蹤識別碼或 VHDSet 快照集識別碼之後，抓取虛擬磁片指定區域的變更清單。</span><span class="sxs-lookup"><span data-stu-id="ab27c-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab27c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab27c-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ab27c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab27c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab27c-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-108">指定虛擬硬碟檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ab27c-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-109">*LimitId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-110">復原變更追蹤識別碼或 VHD 集的快照集識別碼，表示虛擬磁片中的變更基準。</span><span class="sxs-lookup"><span data-stu-id="ab27c-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-111">*TargetSnapshotId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-112">VHDSet 快照集識別碼，指出在判斷虛擬硬碟中的變更時，要與基準比較的快照集。</span><span class="sxs-lookup"><span data-stu-id="ab27c-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="ab27c-113">此參數只對 VHD 設定檔案有效。</span><span class="sxs-lookup"><span data-stu-id="ab27c-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-114">*ByteOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-115">虛擬磁片中要查詢變更之區域的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="ab27c-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-116">*ByteLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-117">要查詢其變更之虛擬磁片區域的位元組長度。</span><span class="sxs-lookup"><span data-stu-id="ab27c-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="ab27c-118">這必須小於虛擬磁片的大小。</span><span class="sxs-lookup"><span data-stu-id="ab27c-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-119">*ProcessedByteLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-120">已處理的位元組長度總計。</span><span class="sxs-lookup"><span data-stu-id="ab27c-120">The total byte length that was processed.</span></span> <span data-ttu-id="ab27c-121">這可能等於 ByteLength 或更少。</span><span class="sxs-lookup"><span data-stu-id="ab27c-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-122">*ChangedByteOffsets* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-123">虛擬磁片中的位元組位移清單，指出每個變更範圍的開頭。</span><span class="sxs-lookup"><span data-stu-id="ab27c-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-124">*ChangedByteLengths* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-125">虛擬磁片中已變更範圍的位元組長度清單。</span><span class="sxs-lookup"><span data-stu-id="ab27c-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="ab27c-126">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab27c-127">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="ab27c-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab27c-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab27c-128">Return value</span></span>

<span data-ttu-id="ab27c-129">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ab27c-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ab27c-130">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="ab27c-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-131">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="ab27c-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-132">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="ab27c-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-133">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="ab27c-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-134">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="ab27c-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-135">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="ab27c-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-136">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="ab27c-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-137">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="ab27c-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-138">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="ab27c-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-139">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="ab27c-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-140">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="ab27c-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-141">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="ab27c-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-142">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="ab27c-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ab27c-143">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="ab27c-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ab27c-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab27c-144">Requirements</span></span>



| <span data-ttu-id="ab27c-145">需求</span><span class="sxs-lookup"><span data-stu-id="ab27c-145">Requirement</span></span> | <span data-ttu-id="ab27c-146">值</span><span class="sxs-lookup"><span data-stu-id="ab27c-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab27c-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab27c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ab27c-148">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab27c-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ab27c-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab27c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ab27c-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ab27c-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ab27c-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="ab27c-151">Namespace</span></span><br/>                | <span data-ttu-id="ab27c-152">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ab27c-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab27c-153">MOF</span><span class="sxs-lookup"><span data-stu-id="ab27c-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab27c-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ab27c-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab27c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="ab27c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab27c-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab27c-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab27c-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab27c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab27c-158">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="ab27c-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




