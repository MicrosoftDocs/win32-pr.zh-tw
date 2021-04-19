---
description: 根據指定的虛擬機器定義，建立新的規劃的電腦系統。
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Msvm_VirtualSystemManagementService 類別的 ImportSystemDefinition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974996"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ec1a0-103">Msvm VirtualSystemManagementService 類別的 ImportSystemDefinition 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ec1a0-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ec1a0-104">根據指定的虛擬機器定義，建立新的規劃的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec1a0-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ec1a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec1a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec1a0-107">*SystemDefinitionFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1a0-108">系統定義檔的完整路徑 ( .xml 或 exp) 代表要匯入的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="ec1a0-109">主機系統或虛擬化平臺不能使用定義檔。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="ec1a0-110">*SnapshotFolder* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1a0-111">可在其中找到此虛擬機器的快照集設定之資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="ec1a0-112">系統會搜尋此資料夾，以找出虛擬機器定義所參考的任何快照集。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="ec1a0-113">在此位置中找不到的任何參考快照集都必須使用 [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) 方法來刪除，或在實現規劃的電腦系統之前使用 [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) 方法匯入。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="ec1a0-114">*GenerateNewSystemIdentifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1a0-115">指出是否要重複使用虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="ec1a0-116">如果此參數為 **True**，則會產生新的系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="ec1a0-117">如果此參數為 **False**，則會使用現有的系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="ec1a0-118">*ImportedSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1a0-119">如果作業同步完成，則為代表已匯入虛擬機器之 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ec1a0-120">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec1a0-121">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec1a0-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec1a0-122">Return value</span></span>

<span data-ttu-id="ec1a0-123">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ec1a0-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ec1a0-124">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-125">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-126">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-127">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-128">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-129">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-130">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-131">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-132">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-133">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-134">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-135">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-136">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ec1a0-137">**使用中的** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="ec1a0-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ec1a0-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec1a0-138">Requirements</span></span>



| <span data-ttu-id="ec1a0-139">需求</span><span class="sxs-lookup"><span data-stu-id="ec1a0-139">Requirement</span></span> | <span data-ttu-id="ec1a0-140">值</span><span class="sxs-lookup"><span data-stu-id="ec1a0-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1a0-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec1a0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1a0-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ec1a0-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec1a0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1a0-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec1a0-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec1a0-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec1a0-145">Namespace</span></span><br/>                | <span data-ttu-id="ec1a0-146">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ec1a0-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ec1a0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ec1a0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec1a0-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ec1a0-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec1a0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="ec1a0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec1a0-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec1a0-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec1a0-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec1a0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1a0-152">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="ec1a0-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

