---
description: 啟動虛擬機器的複寫。
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Msvm_ReplicationService 類別的 >startreplication 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318240"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a7182-103">Msvm ReplicationService 類別的 >startreplication 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a7182-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a7182-104">啟動虛擬機器的複寫。</span><span class="sxs-lookup"><span data-stu-id="a7182-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="a7182-105">當用戶端針對複本虛擬機器呼叫這個方法時，它會啟動具有擴充複本的複寫。</span><span class="sxs-lookup"><span data-stu-id="a7182-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7182-106">語法</span><span class="sxs-lookup"><span data-stu-id="a7182-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a7182-107">參數</span><span class="sxs-lookup"><span data-stu-id="a7182-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7182-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7182-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7182-109">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應啟動複寫的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a7182-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="a7182-110">*InitialReplicationType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7182-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7182-111">要用於執行初始複寫的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="a7182-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="a7182-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**網路傳輸** (1) </span><span class="sxs-lookup"><span data-stu-id="a7182-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a7182-113">網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="a7182-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="a7182-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**匯出** (2) </span><span class="sxs-lookup"><span data-stu-id="a7182-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a7182-115">匯出。</span><span class="sxs-lookup"><span data-stu-id="a7182-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="a7182-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**植入網路傳輸** (3) </span><span class="sxs-lookup"><span data-stu-id="a7182-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a7182-117">植入的網路傳輸。</span><span class="sxs-lookup"><span data-stu-id="a7182-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a7182-118">*InitialReplicationExportLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7182-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7182-119">如果 *InitialReplicationType* 為 2 (匯出) ，此參數會包含要匯出初始複寫之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a7182-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="a7182-120">此參數不會用於其他 *InitialReplicationType* 值，而且可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7182-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="a7182-121">您可以重複使用此目錄來匯出多個虛擬機器複寫。</span><span class="sxs-lookup"><span data-stu-id="a7182-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="a7182-122">此方法會將每個虛擬機器複寫放在此路徑底下的個別子目錄中。</span><span class="sxs-lookup"><span data-stu-id="a7182-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="a7182-123">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7182-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7182-124">透過網路連接到復原伺服器的初始複寫排程開始時間。</span><span class="sxs-lookup"><span data-stu-id="a7182-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="a7182-125">當 *InitialReplicationType* 為 2 (匯出) 時，會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="a7182-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="a7182-126">如果此參數為 **Null**，則會立即開始初始複寫。</span><span class="sxs-lookup"><span data-stu-id="a7182-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="a7182-127">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a7182-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7182-128">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a7182-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7182-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7182-129">Return value</span></span>

<span data-ttu-id="a7182-130">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a7182-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a7182-131">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a7182-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-132">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a7182-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-133">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="a7182-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-134">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="a7182-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-135">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="a7182-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-136">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="a7182-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-137">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="a7182-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-138">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="a7182-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-139">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="a7182-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-140">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="a7182-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-141">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="a7182-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-142">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="a7182-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-143">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="a7182-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a7182-144">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="a7182-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a7182-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7182-145">Requirements</span></span>



| <span data-ttu-id="a7182-146">需求</span><span class="sxs-lookup"><span data-stu-id="a7182-146">Requirement</span></span> | <span data-ttu-id="a7182-147">值</span><span class="sxs-lookup"><span data-stu-id="a7182-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7182-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7182-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a7182-149">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7182-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a7182-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7182-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a7182-151">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7182-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7182-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7182-152">Namespace</span></span><br/>                | <span data-ttu-id="a7182-153">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a7182-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a7182-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a7182-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7182-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a7182-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7182-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a7182-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7182-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7182-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a7182-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7182-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7182-159">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="a7182-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

