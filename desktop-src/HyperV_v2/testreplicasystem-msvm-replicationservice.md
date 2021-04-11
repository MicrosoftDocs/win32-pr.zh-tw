---
description: 使用指定的快照集建立虛擬機器的新複本，以供測試之用。
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Msvm_ReplicationService 類別的 TestReplicaSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851836"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="fe65d-103">Msvm ReplicationService 類別的 TestReplicaSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fe65d-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="fe65d-104">使用指定的快照集建立虛擬機器的新複本，以供測試之用。</span><span class="sxs-lookup"><span data-stu-id="fe65d-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe65d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe65d-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fe65d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe65d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe65d-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe65d-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe65d-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應測試複寫的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fe65d-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="fe65d-109">*SnapshotSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe65d-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe65d-110">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))實例的參考，表示用來建立測試容錯移轉系統的快照集。</span><span class="sxs-lookup"><span data-stu-id="fe65d-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="fe65d-111">如果此參數為 **Null**，則會從最近的時間點執行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="fe65d-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="fe65d-112">*ResultingSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe65d-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe65d-113">如果虛擬機器已成功定義，就會接收到代表新定義之測試虛擬機器之 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 系統類型實例的參考。</span><span class="sxs-lookup"><span data-stu-id="fe65d-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="fe65d-114">當不再需要此系統時，請呼叫 [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) 方法加以終結。</span><span class="sxs-lookup"><span data-stu-id="fe65d-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fe65d-115">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe65d-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe65d-116">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="fe65d-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe65d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe65d-117">Return value</span></span>

<span data-ttu-id="fe65d-118">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fe65d-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fe65d-119">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="fe65d-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-120">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="fe65d-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-121">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="fe65d-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-122">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="fe65d-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-123">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="fe65d-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-124">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="fe65d-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-125">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="fe65d-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-126">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="fe65d-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-127">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="fe65d-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-128">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="fe65d-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-129">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="fe65d-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-130">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="fe65d-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-131">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="fe65d-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fe65d-132">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="fe65d-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fe65d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe65d-133">Requirements</span></span>



| <span data-ttu-id="fe65d-134">需求</span><span class="sxs-lookup"><span data-stu-id="fe65d-134">Requirement</span></span> | <span data-ttu-id="fe65d-135">值</span><span class="sxs-lookup"><span data-stu-id="fe65d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe65d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe65d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fe65d-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe65d-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fe65d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe65d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fe65d-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe65d-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe65d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe65d-140">Namespace</span></span><br/>                | <span data-ttu-id="fe65d-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fe65d-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe65d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fe65d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe65d-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fe65d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe65d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fe65d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe65d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe65d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe65d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe65d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe65d-147">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="fe65d-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

