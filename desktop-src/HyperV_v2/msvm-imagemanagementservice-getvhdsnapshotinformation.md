---
description: 抓取 VHD 設定檔中 VHD 快照集的相關資訊。
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Msvm_ImageManagementService 類別的 GetVHDSnapshotInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001341"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="f1c07-103">Msvm ImageManagementService 類別的 GetVHDSnapshotInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f1c07-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="f1c07-104">抓取 VHD 設定檔中 VHD 快照集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1c07-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c07-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1c07-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f1c07-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1c07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1c07-107">*VHDSetPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1c07-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c07-108">指定 VHD 設定檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f1c07-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="f1c07-109">*SnapshotIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1c07-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c07-110">Guid 清單，代表所要求之資訊的每個快照集的快照集識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1c07-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="f1c07-111">如果此參數為 Null，則會抓取所有快照集的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1c07-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f1c07-112">*AdditionalInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1c07-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c07-113">陣列，指定應該針對每個 VHD 快照集收集哪些額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1c07-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="f1c07-114">陣列中的每個專案都是一種額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="f1c07-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="f1c07-115">如果此參數為 Null，則不會抓取任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="f1c07-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1c07-116">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f1c07-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1c07-117">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f1c07-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="f1c07-118">**父路徑** (2) </span><span class="sxs-lookup"><span data-stu-id="f1c07-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f1c07-119">*SnapshotInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1c07-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c07-120">如果成功，則為每個所要求快照集的相關資訊陣列。</span><span class="sxs-lookup"><span data-stu-id="f1c07-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="f1c07-121">每個元素都是 [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="f1c07-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1c07-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1c07-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1c07-123">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="f1c07-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1c07-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1c07-124">Return value</span></span>

<span data-ttu-id="f1c07-125">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f1c07-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f1c07-126">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f1c07-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-127">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f1c07-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-128">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="f1c07-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-129">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="f1c07-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-130">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="f1c07-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-131">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="f1c07-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-132">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="f1c07-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-133">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="f1c07-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-134">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="f1c07-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-135">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="f1c07-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-136">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="f1c07-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-137">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="f1c07-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-138">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="f1c07-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f1c07-139">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="f1c07-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f1c07-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1c07-140">Requirements</span></span>



| <span data-ttu-id="f1c07-141">需求</span><span class="sxs-lookup"><span data-stu-id="f1c07-141">Requirement</span></span> | <span data-ttu-id="f1c07-142">值</span><span class="sxs-lookup"><span data-stu-id="f1c07-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c07-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1c07-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c07-144">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1c07-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f1c07-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1c07-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c07-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f1c07-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f1c07-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1c07-147">Namespace</span></span><br/>                | <span data-ttu-id="f1c07-148">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1c07-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1c07-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f1c07-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1c07-150"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f1c07-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1c07-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f1c07-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1c07-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1c07-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1c07-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1c07-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c07-154">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="f1c07-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




