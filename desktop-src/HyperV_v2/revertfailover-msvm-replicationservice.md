---
description: 藉由捨棄目前的容錯移轉磁片來還原虛擬機器目前的容錯移轉。
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Msvm_ReplicationService 類別的 RevertFailover 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992600"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="9f703-103">Msvm ReplicationService 類別的 RevertFailover 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9f703-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="9f703-104">藉由捨棄目前的容錯移轉磁片來還原虛擬機器目前的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="9f703-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="9f703-105">完成此作業之後，就可以再次呼叫 [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) 。</span><span class="sxs-lookup"><span data-stu-id="9f703-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f703-106">語法</span><span class="sxs-lookup"><span data-stu-id="9f703-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9f703-107">參數</span><span class="sxs-lookup"><span data-stu-id="9f703-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f703-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f703-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f703-109">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要還原容錯移轉的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9f703-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="9f703-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9f703-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f703-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="9f703-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f703-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f703-112">Return value</span></span>

<span data-ttu-id="9f703-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9f703-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9f703-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9f703-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="9f703-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="9f703-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="9f703-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="9f703-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="9f703-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="9f703-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="9f703-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="9f703-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="9f703-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="9f703-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="9f703-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="9f703-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9f703-127">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="9f703-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9f703-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f703-128">Requirements</span></span>



| <span data-ttu-id="9f703-129">需求</span><span class="sxs-lookup"><span data-stu-id="9f703-129">Requirement</span></span> | <span data-ttu-id="9f703-130">值</span><span class="sxs-lookup"><span data-stu-id="9f703-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f703-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f703-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9f703-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f703-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9f703-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f703-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9f703-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f703-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f703-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f703-135">Namespace</span></span><br/>                | <span data-ttu-id="9f703-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9f703-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f703-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9f703-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f703-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9f703-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f703-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9f703-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f703-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f703-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f703-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f703-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f703-142">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="9f703-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="9f703-143">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="9f703-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="9f703-144">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="9f703-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

