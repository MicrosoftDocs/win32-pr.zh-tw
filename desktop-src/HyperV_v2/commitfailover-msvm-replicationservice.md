---
description: 認可 InitiateFailover 方法用於容錯移轉的修復快照。
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Msvm_ReplicationService 類別的 CommitFailover 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982472"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="44bf6-103">Msvm ReplicationService 類別的 CommitFailover 方法 \_</span><span class="sxs-lookup"><span data-stu-id="44bf6-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="44bf6-104">認可 [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) 方法用於容錯移轉的修復快照。</span><span class="sxs-lookup"><span data-stu-id="44bf6-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="44bf6-105">這個方法會套用復原快照集，以在復原虛擬機器上壓平合併復原點。</span><span class="sxs-lookup"><span data-stu-id="44bf6-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="44bf6-106">完成之後，就無法取消容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="44bf6-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="44bf6-107">使用者通常會在用於容錯移轉的複寫點很滿意，而且復原虛擬機器可以將角色變更為主要時，才會執行此工作。</span><span class="sxs-lookup"><span data-stu-id="44bf6-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="44bf6-108">語法</span><span class="sxs-lookup"><span data-stu-id="44bf6-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="44bf6-109">參數</span><span class="sxs-lookup"><span data-stu-id="44bf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44bf6-110">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="44bf6-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44bf6-111">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要認可容錯移轉的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="44bf6-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="44bf6-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="44bf6-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44bf6-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="44bf6-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44bf6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="44bf6-114">Return value</span></span>

<span data-ttu-id="44bf6-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="44bf6-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="44bf6-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="44bf6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="44bf6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="44bf6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="44bf6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="44bf6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="44bf6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="44bf6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="44bf6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="44bf6-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="44bf6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="44bf6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="44bf6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="44bf6-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="44bf6-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="44bf6-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="44bf6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="44bf6-130">Requirements</span></span>



| <span data-ttu-id="44bf6-131">需求</span><span class="sxs-lookup"><span data-stu-id="44bf6-131">Requirement</span></span> | <span data-ttu-id="44bf6-132">值</span><span class="sxs-lookup"><span data-stu-id="44bf6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bf6-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44bf6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="44bf6-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44bf6-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="44bf6-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44bf6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="44bf6-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44bf6-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44bf6-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="44bf6-137">Namespace</span></span><br/>                | <span data-ttu-id="44bf6-138">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="44bf6-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="44bf6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="44bf6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44bf6-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="44bf6-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44bf6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44bf6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44bf6-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44bf6-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44bf6-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44bf6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44bf6-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="44bf6-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

