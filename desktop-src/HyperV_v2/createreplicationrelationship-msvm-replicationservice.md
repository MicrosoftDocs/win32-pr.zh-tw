---
description: 為虛擬機器建立新的複寫關聯性。 當用戶端針對複本虛擬機器呼叫這個方法時，它會將複寫關聯性擴充到指定的提供者。
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Msvm_ReplicationService 類別的 >createreplicationrelationship 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988274"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="e7bad-104">Msvm ReplicationService 類別的 >createreplicationrelationship 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e7bad-104">CreateReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="e7bad-105">為虛擬機器建立新的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="e7bad-105">Creates a new replication relationship for a virtual machine.</span></span> <span data-ttu-id="e7bad-106">當用戶端針對複本虛擬機器呼叫這個方法時，它會將複寫關聯性擴充到指定的提供者。</span><span class="sxs-lookup"><span data-stu-id="e7bad-106">When a client calls this method for a replica virtual machine, it extends the replication relationship to the specified provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bad-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7bad-107">Syntax</span></span>


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e7bad-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7bad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bad-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7bad-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bad-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應啟用複寫的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e7bad-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e7bad-111">*ReplicationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7bad-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bad-112">[**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md)類別實例的字串表示，定義要為虛擬機器建立之新複寫關聯性的複寫設定。</span><span class="sxs-lookup"><span data-stu-id="e7bad-112">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the new replication relationship to be created for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e7bad-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e7bad-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bad-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e7bad-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bad-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7bad-115">Return value</span></span>

<span data-ttu-id="e7bad-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e7bad-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e7bad-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e7bad-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e7bad-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="e7bad-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="e7bad-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="e7bad-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="e7bad-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="e7bad-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="e7bad-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="e7bad-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="e7bad-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="e7bad-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="e7bad-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="e7bad-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e7bad-130">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="e7bad-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e7bad-131">備註</span><span class="sxs-lookup"><span data-stu-id="e7bad-131">Remarks</span></span>

<span data-ttu-id="e7bad-132">**>createreplicationrelationship** 會將 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 實例 (FRSD) 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="e7bad-132">**CreateReplicationRelationship** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="e7bad-133">虛擬機器與主機對主機提供者相關聯的 FRSD 是預設選項。</span><span class="sxs-lookup"><span data-stu-id="e7bad-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="e7bad-134">針對預設提供者的每個屬性，會驗證輸入 FRSD 是否有有效的設定。</span><span class="sxs-lookup"><span data-stu-id="e7bad-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="e7bad-135">下表摘要說明與外部提供者相關的驗證差異。</span><span class="sxs-lookup"><span data-stu-id="e7bad-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="e7bad-136">屬性</span><span class="sxs-lookup"><span data-stu-id="e7bad-136">Property</span></span>                                             | <span data-ttu-id="e7bad-137">外部提供者</span><span class="sxs-lookup"><span data-stu-id="e7bad-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="e7bad-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="e7bad-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="e7bad-139">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-139">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e7bad-140">AuthenticationType</span></span>                                   | <span data-ttu-id="e7bad-141">忽略</span><span class="sxs-lookup"><span data-stu-id="e7bad-141">Ignored</span></span>                                            |
| <span data-ttu-id="e7bad-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="e7bad-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="e7bad-143">忽略</span><span class="sxs-lookup"><span data-stu-id="e7bad-143">Ignored</span></span>                                            |
| <span data-ttu-id="e7bad-144">RootCertificateThumbPrint (RO) </span><span class="sxs-lookup"><span data-stu-id="e7bad-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="e7bad-145">忽略</span><span class="sxs-lookup"><span data-stu-id="e7bad-145">Ignored</span></span>                                            |
| <span data-ttu-id="e7bad-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="e7bad-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="e7bad-147">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-147">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="e7bad-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="e7bad-149">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-149">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="e7bad-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="e7bad-151">\*如果提供者有需求，則會忽略 (可能會變更) </span><span class="sxs-lookup"><span data-stu-id="e7bad-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="e7bad-152">RecoveryHostSystem (RO) </span><span class="sxs-lookup"><span data-stu-id="e7bad-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="e7bad-153">忽略</span><span class="sxs-lookup"><span data-stu-id="e7bad-153">Ignored</span></span>                                            |
| <span data-ttu-id="e7bad-154">PrimaryConnectionPoint (RO) </span><span class="sxs-lookup"><span data-stu-id="e7bad-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="e7bad-155">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-155">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-156">PrimaryHostSystem (RO) </span><span class="sxs-lookup"><span data-stu-id="e7bad-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="e7bad-157">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-157">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="e7bad-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="e7bad-159">\*如果提供者有需求，則會忽略 (可能會變更) </span><span class="sxs-lookup"><span data-stu-id="e7bad-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="e7bad-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="e7bad-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="e7bad-161">忽略</span><span class="sxs-lookup"><span data-stu-id="e7bad-161">Ignored</span></span>                                            |
| <span data-ttu-id="e7bad-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="e7bad-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="e7bad-163">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-163">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="e7bad-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="e7bad-165">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-165">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="e7bad-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="e7bad-167">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-167">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="e7bad-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="e7bad-169">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-169">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="e7bad-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="e7bad-171">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-171">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="e7bad-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="e7bad-173">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-173">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-174">EnableWriteOrderPreservationAcrossDisks (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="e7bad-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="e7bad-175">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-175">Same as default provider</span></span>                           |
| <span data-ttu-id="e7bad-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="e7bad-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="e7bad-177">與預設提供者相同</span><span class="sxs-lookup"><span data-stu-id="e7bad-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="e7bad-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7bad-178">Requirements</span></span>



| <span data-ttu-id="e7bad-179">需求</span><span class="sxs-lookup"><span data-stu-id="e7bad-179">Requirement</span></span> | <span data-ttu-id="e7bad-180">值</span><span class="sxs-lookup"><span data-stu-id="e7bad-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bad-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7bad-181">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bad-182">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7bad-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7bad-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7bad-183">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bad-184">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7bad-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7bad-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="e7bad-185">Namespace</span></span><br/>                | <span data-ttu-id="e7bad-186">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e7bad-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e7bad-187">MOF</span><span class="sxs-lookup"><span data-stu-id="e7bad-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7bad-188"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e7bad-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7bad-189">DLL</span><span class="sxs-lookup"><span data-stu-id="e7bad-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7bad-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7bad-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7bad-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7bad-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bad-192">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="e7bad-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e7bad-193">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="e7bad-193">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

