---
description: 要求虛擬機器複寫關聯性的複寫狀態變更為指定的值。
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: Msvm_ComputerSystem：： RequestReplicationStateChangeEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987216"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="e371a-103">Msvm \_ ：： RequestReplicationStateChangeEx 方法</span><span class="sxs-lookup"><span data-stu-id="e371a-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="e371a-104">要求虛擬機器複寫關聯性的複寫狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="e371a-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="e371a-105">當狀態變更正在進行時， **ReplicationState** 屬性會變更為 *RequestedState* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="e371a-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="e371a-106">只有代表虛擬機器的 Msvm 同機類別 [**\_**](msvm-computersystem.md) 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e371a-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e371a-107">語法</span><span class="sxs-lookup"><span data-stu-id="e371a-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="e371a-108">參數</span><span class="sxs-lookup"><span data-stu-id="e371a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e371a-109">*ReplicationRelationship* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e371a-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e371a-110">[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別之內嵌實例的字串表示，這個類別會定義狀態變更要求的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="e371a-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="e371a-111">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="e371a-111">This parameter is optional.</span></span> <span data-ttu-id="e371a-112">未指定時，會在主要複寫關聯性上執行要求。</span><span class="sxs-lookup"><span data-stu-id="e371a-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="e371a-113">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e371a-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e371a-114">新的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="e371a-114">The new replication state.</span></span> <span data-ttu-id="e371a-115">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e371a-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="e371a-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**準備開始初始** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="e371a-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e371a-117">準備開始初始複寫。</span><span class="sxs-lookup"><span data-stu-id="e371a-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="e371a-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="e371a-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e371a-119">正在等候完成初始複寫。</span><span class="sxs-lookup"><span data-stu-id="e371a-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="e371a-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="e371a-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e371a-121">複寫。</span><span class="sxs-lookup"><span data-stu-id="e371a-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="e371a-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**同步複寫完成** (4) </span><span class="sxs-lookup"><span data-stu-id="e371a-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e371a-123">同步的複寫完成。</span><span class="sxs-lookup"><span data-stu-id="e371a-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="e371a-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="e371a-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e371a-125">暫止複寫。</span><span class="sxs-lookup"><span data-stu-id="e371a-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="e371a-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**取消重新同步** 處理 (9) </span><span class="sxs-lookup"><span data-stu-id="e371a-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="e371a-127">取消重新同步處理。</span><span class="sxs-lookup"><span data-stu-id="e371a-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e371a-128">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e371a-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e371a-129">如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。</span><span class="sxs-lookup"><span data-stu-id="e371a-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="e371a-130">如果有，則會使用傳回的參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="e371a-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="e371a-131">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e371a-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e371a-132">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="e371a-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e371a-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="e371a-133">Return value</span></span>

<span data-ttu-id="e371a-134">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e371a-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="e371a-135">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e371a-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="e371a-136">Description</span><span class="sxs-lookup"><span data-stu-id="e371a-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e371a-137"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="e371a-138">Success</span><span class="sxs-lookup"><span data-stu-id="e371a-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="e371a-139"><dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="e371a-140">轉換是非同步。</span><span class="sxs-lookup"><span data-stu-id="e371a-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="e371a-141"><dt>**失敗**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-142"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-143"><dt>**不支援**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-144"><dt>**狀態為未知**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-145"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-146"><dt>**不正確參數**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="e371a-147">不支援其中一個參數所指定的值。</span><span class="sxs-lookup"><span data-stu-id="e371a-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="e371a-148"><dt>**系統使用中**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-149"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="e371a-150">在目前的複寫模式或狀態中，不支援在 *RequestedState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="e371a-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="e371a-151"><dt>**不正確的資料類型**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-152"><dt>**系統無法使用**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-153"><dt>**記憶體不足**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="e371a-154"><dt>**找不到**</dt>檔案 <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="e371a-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="e371a-155">Requirements</span></span>



| <span data-ttu-id="e371a-156">需求</span><span class="sxs-lookup"><span data-stu-id="e371a-156">Requirement</span></span> | <span data-ttu-id="e371a-157">值</span><span class="sxs-lookup"><span data-stu-id="e371a-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e371a-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e371a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e371a-159">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e371a-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e371a-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e371a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e371a-161">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e371a-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e371a-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="e371a-162">Namespace</span></span><br/>                | <span data-ttu-id="e371a-163">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e371a-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e371a-164">MOF</span><span class="sxs-lookup"><span data-stu-id="e371a-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e371a-165"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e371a-166">DLL</span><span class="sxs-lookup"><span data-stu-id="e371a-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e371a-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e371a-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e371a-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e371a-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e371a-169">**Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="e371a-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




