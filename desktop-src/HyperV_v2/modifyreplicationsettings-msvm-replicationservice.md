---
description: 修改虛擬機器的複寫設定。 當用戶端針對複本虛擬機器呼叫這個方法時，它會修改複寫關聯性與擴充複本的複寫設定。
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Msvm_ReplicationService 類別的 ModifyReplicationSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978272"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="69f98-104">Msvm ReplicationService 類別的 ModifyReplicationSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="69f98-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="69f98-105">修改虛擬機器的複寫設定。</span><span class="sxs-lookup"><span data-stu-id="69f98-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="69f98-106">當用戶端針對複本虛擬機器呼叫這個方法時，它會修改複寫關聯性與擴充複本的複寫設定。</span><span class="sxs-lookup"><span data-stu-id="69f98-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f98-107">語法</span><span class="sxs-lookup"><span data-stu-id="69f98-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="69f98-108">參數</span><span class="sxs-lookup"><span data-stu-id="69f98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f98-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="69f98-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f98-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表應修改複寫設定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="69f98-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="69f98-111">*ReplicationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69f98-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f98-112">定義新複寫設定之 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 類別的字串表示。</span><span class="sxs-lookup"><span data-stu-id="69f98-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="69f98-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="69f98-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69f98-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="69f98-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69f98-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="69f98-115">Return value</span></span>

<span data-ttu-id="69f98-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="69f98-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="69f98-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="69f98-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="69f98-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="69f98-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="69f98-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="69f98-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="69f98-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="69f98-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="69f98-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="69f98-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="69f98-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="69f98-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="69f98-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="69f98-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="69f98-130">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="69f98-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="69f98-131">備註</span><span class="sxs-lookup"><span data-stu-id="69f98-131">Remarks</span></span>

<span data-ttu-id="69f98-132">**ModifyReplicationSettings** 會將 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 實例 (FRSD) 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="69f98-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="69f98-133">虛擬機器與主機對主機提供者相關聯的 FRSD 是預設選項。</span><span class="sxs-lookup"><span data-stu-id="69f98-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="69f98-134">針對預設提供者的每個屬性，會驗證輸入 FRSD 是否有有效的設定。</span><span class="sxs-lookup"><span data-stu-id="69f98-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="69f98-135">下表摘要說明與外部提供者相關的驗證差異。</span><span class="sxs-lookup"><span data-stu-id="69f98-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="69f98-136">屬性</span><span class="sxs-lookup"><span data-stu-id="69f98-136">Property</span></span>                                             | <span data-ttu-id="69f98-137">外部提供者</span><span class="sxs-lookup"><span data-stu-id="69f98-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="69f98-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="69f98-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="69f98-139">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-139">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="69f98-140">AuthenticationType</span></span>                                   | <span data-ttu-id="69f98-141">忽略</span><span class="sxs-lookup"><span data-stu-id="69f98-141">Ignored</span></span>                                            |
| <span data-ttu-id="69f98-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="69f98-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="69f98-143">忽略</span><span class="sxs-lookup"><span data-stu-id="69f98-143">Ignored</span></span>                                            |
| <span data-ttu-id="69f98-144">RootCertificateThumbPrint (RO) </span><span class="sxs-lookup"><span data-stu-id="69f98-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="69f98-145">忽略</span><span class="sxs-lookup"><span data-stu-id="69f98-145">Ignored</span></span>                                            |
| <span data-ttu-id="69f98-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="69f98-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="69f98-147">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-147">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="69f98-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="69f98-149">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-149">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="69f98-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="69f98-151">\*如果提供者有需求，則會忽略 (可能會變更) </span><span class="sxs-lookup"><span data-stu-id="69f98-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="69f98-152">RecoveryHostSystem (RO) </span><span class="sxs-lookup"><span data-stu-id="69f98-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="69f98-153">忽略</span><span class="sxs-lookup"><span data-stu-id="69f98-153">Ignored</span></span>                                            |
| <span data-ttu-id="69f98-154">PrimaryConnectionPoint (RO) </span><span class="sxs-lookup"><span data-stu-id="69f98-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="69f98-155">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-155">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-156">PrimaryHostSystem (RO) </span><span class="sxs-lookup"><span data-stu-id="69f98-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="69f98-157">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-157">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="69f98-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="69f98-159">\*如果提供者有需求，則會忽略 (可能會變更) </span><span class="sxs-lookup"><span data-stu-id="69f98-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="69f98-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="69f98-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="69f98-161">忽略</span><span class="sxs-lookup"><span data-stu-id="69f98-161">Ignored</span></span>                                            |
| <span data-ttu-id="69f98-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="69f98-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="69f98-163">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-163">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="69f98-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="69f98-165">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-165">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="69f98-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="69f98-167">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-167">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="69f98-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="69f98-169">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-169">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="69f98-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="69f98-171">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-171">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="69f98-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="69f98-173">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-173">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-174">EnableWriteOrderPreservationAcrossDisks (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="69f98-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="69f98-175">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-175">Same as default provider</span></span>                           |
| <span data-ttu-id="69f98-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="69f98-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="69f98-177">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="69f98-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="69f98-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="69f98-178">Requirements</span></span>



| <span data-ttu-id="69f98-179">需求</span><span class="sxs-lookup"><span data-stu-id="69f98-179">Requirement</span></span> | <span data-ttu-id="69f98-180">值</span><span class="sxs-lookup"><span data-stu-id="69f98-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f98-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69f98-181">Minimum supported client</span></span><br/> | <span data-ttu-id="69f98-182">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69f98-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="69f98-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69f98-183">Minimum supported server</span></span><br/> | <span data-ttu-id="69f98-184">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69f98-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69f98-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="69f98-185">Namespace</span></span><br/>                | <span data-ttu-id="69f98-186">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="69f98-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="69f98-187">MOF</span><span class="sxs-lookup"><span data-stu-id="69f98-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69f98-188"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="69f98-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69f98-189">DLL</span><span class="sxs-lookup"><span data-stu-id="69f98-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69f98-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69f98-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69f98-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69f98-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f98-192">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="69f98-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

