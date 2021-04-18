---
description: 編輯 VHD 設定檔內的 VHD 快照集專案。 如果已有問題的快照集識別碼，則會以新的專案覆寫現有的快照集專案。 否則，新的專案會新增至 VHD 設定檔案。
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Msvm_ImageManagementService 類別的 SetVHDSnapshotInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971434"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e22d3-105">Msvm ImageManagementService 類別的 SetVHDSnapshotInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e22d3-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e22d3-106">編輯 VHD 設定檔內的 VHD 快照集專案。</span><span class="sxs-lookup"><span data-stu-id="e22d3-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="e22d3-107">如果已有問題的快照集識別碼，則會以新的專案覆寫現有的快照集專案。</span><span class="sxs-lookup"><span data-stu-id="e22d3-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="e22d3-108">否則，新的專案會新增至 VHD 設定檔案。</span><span class="sxs-lookup"><span data-stu-id="e22d3-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22d3-109">語法</span><span class="sxs-lookup"><span data-stu-id="e22d3-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e22d3-110">參數</span><span class="sxs-lookup"><span data-stu-id="e22d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22d3-111">*資訊* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e22d3-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e22d3-112">要在 VHD 設定檔中變更或新增的 VHD 快照集資訊。</span><span class="sxs-lookup"><span data-stu-id="e22d3-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="e22d3-113">字串是 [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="e22d3-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e22d3-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e22d3-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e22d3-115">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="e22d3-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22d3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e22d3-116">Return value</span></span>

<span data-ttu-id="e22d3-117">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e22d3-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e22d3-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e22d3-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e22d3-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="e22d3-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="e22d3-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="e22d3-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="e22d3-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="e22d3-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="e22d3-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="e22d3-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="e22d3-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="e22d3-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="e22d3-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="e22d3-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e22d3-131">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="e22d3-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e22d3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e22d3-132">Requirements</span></span>



| <span data-ttu-id="e22d3-133">需求</span><span class="sxs-lookup"><span data-stu-id="e22d3-133">Requirement</span></span> | <span data-ttu-id="e22d3-134">值</span><span class="sxs-lookup"><span data-stu-id="e22d3-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22d3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e22d3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e22d3-136">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e22d3-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e22d3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e22d3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e22d3-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e22d3-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e22d3-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="e22d3-139">Namespace</span></span><br/>                | <span data-ttu-id="e22d3-140">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e22d3-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e22d3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e22d3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e22d3-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e22d3-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e22d3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e22d3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e22d3-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e22d3-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e22d3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e22d3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22d3-146">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="e22d3-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




