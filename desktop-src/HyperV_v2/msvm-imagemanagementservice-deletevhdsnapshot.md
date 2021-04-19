---
description: 刪除 VHD 設定檔內的 VHD 快照集專案。
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Msvm_ImageManagementService 類別的 DeleteVHDSnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973668"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="c8f1e-103">Msvm ImageManagementService 類別的 DeleteVHDSnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c8f1e-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="c8f1e-104">刪除 VHD 設定檔內的 VHD 快照集專案。</span><span class="sxs-lookup"><span data-stu-id="c8f1e-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f1e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8f1e-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c8f1e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f1e-107">*VHDSetPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f1e-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f1e-108">字串，包含包含有問題快照集的 VHD 集檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c8f1e-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="c8f1e-109">*SnapshotId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f1e-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f1e-110">GUID，代表要刪除的 VHD 快照集專案的快照集識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8f1e-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="c8f1e-111">*PersistReferenceSnapshot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f1e-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f1e-112">是否應在刪除快照集之後保存僅參考的快照記錄。</span><span class="sxs-lookup"><span data-stu-id="c8f1e-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="c8f1e-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8f1e-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f1e-114">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="c8f1e-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f1e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8f1e-115">Return value</span></span>

<span data-ttu-id="c8f1e-116">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="c8f1e-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c8f1e-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c8f1e-130">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="c8f1e-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c8f1e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8f1e-131">Requirements</span></span>



| <span data-ttu-id="c8f1e-132">需求</span><span class="sxs-lookup"><span data-stu-id="c8f1e-132">Requirement</span></span> | <span data-ttu-id="c8f1e-133">值</span><span class="sxs-lookup"><span data-stu-id="c8f1e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f1e-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8f1e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f1e-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8f1e-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c8f1e-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8f1e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f1e-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c8f1e-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c8f1e-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8f1e-138">Namespace</span></span><br/>                | <span data-ttu-id="c8f1e-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c8f1e-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c8f1e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c8f1e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8f1e-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c8f1e-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8f1e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c8f1e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8f1e-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8f1e-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8f1e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8f1e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f1e-145">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="c8f1e-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




