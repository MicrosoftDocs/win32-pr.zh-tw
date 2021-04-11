---
description: 搜尋指定的資料夾中是否有任何與指定之規劃的電腦系統相關聯的快照集定義檔案，並針對此位置中的每個關聯定義檔，在規劃的電腦系統上建立新的快照集。
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Msvm_VirtualSystemManagementService 類別的 ImportSnapshotDefinitions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848517"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="952a9-103">Msvm VirtualSystemManagementService 類別的 ImportSnapshotDefinitions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="952a9-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="952a9-104">搜尋指定的資料夾中是否有任何與指定之規劃的電腦系統相關聯的快照集定義檔案，並針對此位置中的每個關聯定義檔，在規劃的電腦系統上建立新的快照集。</span><span class="sxs-lookup"><span data-stu-id="952a9-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="952a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="952a9-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="952a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="952a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="952a9-107">*PlannedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952a9-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952a9-108">[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)物件的參考，該物件表示參考要匯入之快照集的計畫虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="952a9-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="952a9-109">*SnapshotFolder* \[在\]</span><span class="sxs-lookup"><span data-stu-id="952a9-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952a9-110">可在其中找到此虛擬機器的快照集設定之資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="952a9-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="952a9-111">*ImportedSnapshots* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="952a9-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="952a9-112">如果作業同步完成，則為 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 實例的參考陣列，代表已成功匯入的快照集。</span><span class="sxs-lookup"><span data-stu-id="952a9-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="952a9-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="952a9-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="952a9-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="952a9-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="952a9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="952a9-115">Return value</span></span>

<span data-ttu-id="952a9-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="952a9-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="952a9-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="952a9-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="952a9-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="952a9-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="952a9-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="952a9-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="952a9-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="952a9-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="952a9-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="952a9-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="952a9-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="952a9-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="952a9-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="952a9-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="952a9-130">**使用中的** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="952a9-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="952a9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="952a9-131">Requirements</span></span>



| <span data-ttu-id="952a9-132">需求</span><span class="sxs-lookup"><span data-stu-id="952a9-132">Requirement</span></span> | <span data-ttu-id="952a9-133">值</span><span class="sxs-lookup"><span data-stu-id="952a9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="952a9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="952a9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="952a9-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952a9-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="952a9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="952a9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="952a9-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="952a9-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="952a9-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="952a9-138">Namespace</span></span><br/>                | <span data-ttu-id="952a9-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="952a9-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="952a9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="952a9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="952a9-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="952a9-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="952a9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="952a9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="952a9-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="952a9-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="952a9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="952a9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952a9-145">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="952a9-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

