---
description: 起始復原虛擬機器的容錯回復。
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: Msvm_ReplicationService：： InitiateFailback 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998473"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="077a9-103">Msvm \_ ReplicationService：： InitiateFailback 方法</span><span class="sxs-lookup"><span data-stu-id="077a9-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="077a9-104">起始復原虛擬機器的容錯回復。</span><span class="sxs-lookup"><span data-stu-id="077a9-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="077a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="077a9-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="077a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="077a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="077a9-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="077a9-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="077a9-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要起始容錯回復的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="077a9-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="077a9-109">*ReplicationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="077a9-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="077a9-110">[**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md)類別之內嵌實例的字串表示，這個類別會定義容錯回復的複寫設定。</span><span class="sxs-lookup"><span data-stu-id="077a9-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="077a9-111">*RecoveryPointIdentifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="077a9-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="077a9-112">選用的輸入，可識別要求容錯回復的復原點。</span><span class="sxs-lookup"><span data-stu-id="077a9-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="077a9-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="077a9-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="077a9-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="077a9-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="077a9-115">這個參考可以用來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="077a9-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="077a9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="077a9-116">Return value</span></span>

<span data-ttu-id="077a9-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="077a9-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="077a9-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="077a9-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="077a9-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="077a9-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="077a9-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="077a9-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="077a9-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="077a9-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="077a9-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="077a9-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="077a9-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="077a9-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="077a9-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="077a9-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="077a9-131">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="077a9-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="077a9-132">備註</span><span class="sxs-lookup"><span data-stu-id="077a9-132">Remarks</span></span>

<span data-ttu-id="077a9-133">**InitiateFailback** 可在復原虛擬機器上運作，讓虛擬機器 *WaitingForFailback* 狀態。</span><span class="sxs-lookup"><span data-stu-id="077a9-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="077a9-134">**InitiateFailback** 會將容錯回復要求轉送至對應的提供者，以從新的-主要端反向會復原點。</span><span class="sxs-lookup"><span data-stu-id="077a9-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="077a9-135">在要求的復原點容錯回復完成後，複寫狀態會移至 [ *FailbackCompleted* ] 狀態。</span><span class="sxs-lookup"><span data-stu-id="077a9-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="077a9-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="077a9-136">Requirements</span></span>



| <span data-ttu-id="077a9-137">需求</span><span class="sxs-lookup"><span data-stu-id="077a9-137">Requirement</span></span> | <span data-ttu-id="077a9-138">值</span><span class="sxs-lookup"><span data-stu-id="077a9-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="077a9-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="077a9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="077a9-140">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="077a9-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="077a9-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="077a9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="077a9-142">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="077a9-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="077a9-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="077a9-143">Namespace</span></span><br/>                | <span data-ttu-id="077a9-144">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="077a9-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="077a9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="077a9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="077a9-146"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="077a9-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="077a9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="077a9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="077a9-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="077a9-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="077a9-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="077a9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="077a9-150">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="077a9-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

