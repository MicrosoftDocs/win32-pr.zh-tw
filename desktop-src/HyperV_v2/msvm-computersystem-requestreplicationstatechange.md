---
description: 要求將虛擬機器的複寫狀態變更為指定的值，並在虛擬機器的主要複寫關聯性上運作。
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Msvm_ComputerSystem 類別的 RequestReplicationStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513016"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="3dbb0-103">Msvm 的 RequestReplicationStateChange 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3dbb0-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="3dbb0-104">要求將虛擬機器的複寫狀態變更為指定的值，並在虛擬機器的主要複寫關聯性上運作。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="3dbb0-105">當狀態變更正在進行時， **ReplicationState** 屬性會變更為 *RequestedState* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="3dbb0-106">只有代表虛擬機器的 Msvm 同機類別 [**\_**](msvm-computersystem.md) 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="3dbb0-107">從 Windows 8.1 開始，建議您不再使用 **RequestReplicationStateChange** 來要求變更複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="3dbb0-108">相反地，請使用 [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3dbb0-109">語法</span><span class="sxs-lookup"><span data-stu-id="3dbb0-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3dbb0-110">參數</span><span class="sxs-lookup"><span data-stu-id="3dbb0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbb0-111">*RequestedState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dbb0-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbb0-112">新的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-112">The new replication state.</span></span> <span data-ttu-id="3dbb0-113">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="3dbb0-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**準備開始初始** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="3dbb0-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3dbb0-115">準備開始初始複寫。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="3dbb0-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="3dbb0-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3dbb0-117">正在等候完成初始複寫。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="3dbb0-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="3dbb0-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3dbb0-119">複寫。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="3dbb0-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**同步複寫完成** (4) </span><span class="sxs-lookup"><span data-stu-id="3dbb0-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3dbb0-121">同步的複寫完成。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="3dbb0-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="3dbb0-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3dbb0-123">暫止複寫。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="3dbb0-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**取消重新同步** 處理 (9) </span><span class="sxs-lookup"><span data-stu-id="3dbb0-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="3dbb0-125">取消重新同步處理。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3dbb0-126">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3dbb0-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbb0-127">如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="3dbb0-128">如果有，則會使用傳回的參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="3dbb0-129">*TimeoutPeriod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dbb0-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbb0-130">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbb0-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dbb0-131">Return value</span></span>

<span data-ttu-id="3dbb0-132">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="3dbb0-133">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3dbb0-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="3dbb0-134">Description</span><span class="sxs-lookup"><span data-stu-id="3dbb0-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3dbb0-135"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="3dbb0-136">Success</span><span class="sxs-lookup"><span data-stu-id="3dbb0-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="3dbb0-137"><dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="3dbb0-138">轉換是非同步。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="3dbb0-139"><dt>**失敗**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-140"><dt>**拒絕存取**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-141"><dt>**不支援**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-142"><dt>**狀態為未知**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-143"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-144"><dt>**不正確參數**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="3dbb0-145">不支援其中一個參數所指定的值。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="3dbb0-146"><dt>**系統使用中**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-147"><dt>**此操作的狀態無效**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="3dbb0-148">在目前的複寫模式或狀態中，不支援在 *RequestedState* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="3dbb0-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="3dbb0-149"><dt>**不正確的資料類型**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-150"><dt>**系統無法使用**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-151"><dt>**記憶體不足**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="3dbb0-152"><dt>**找不到**</dt>檔案 <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="3dbb0-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dbb0-153">Requirements</span></span>



| <span data-ttu-id="3dbb0-154">需求</span><span class="sxs-lookup"><span data-stu-id="3dbb0-154">Requirement</span></span> | <span data-ttu-id="3dbb0-155">值</span><span class="sxs-lookup"><span data-stu-id="3dbb0-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbb0-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3dbb0-156">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbb0-157">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dbb0-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3dbb0-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3dbb0-158">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbb0-159">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dbb0-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3dbb0-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="3dbb0-160">Namespace</span></span><br/>                | <span data-ttu-id="3dbb0-161">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3dbb0-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3dbb0-162">MOF</span><span class="sxs-lookup"><span data-stu-id="3dbb0-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dbb0-163"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dbb0-164">DLL</span><span class="sxs-lookup"><span data-stu-id="3dbb0-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dbb0-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3dbb0-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3dbb0-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dbb0-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbb0-167">**Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="3dbb0-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




