---
description: 在指定的虛擬機器上執行重新同步處理操作。
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Msvm_ReplicationService 類別的重新同步處理方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319519"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b2261-103">Msvm ReplicationService 類別的重新同步處理方法 \_</span><span class="sxs-lookup"><span data-stu-id="b2261-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b2261-104">在指定的虛擬機器上執行重新同步處理操作。</span><span class="sxs-lookup"><span data-stu-id="b2261-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="b2261-105">當用戶端針對複本虛擬機器呼叫這個方法時，它會重新同步處理擴充的複本。</span><span class="sxs-lookup"><span data-stu-id="b2261-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="b2261-106">這種方法會比較主要和復原虛擬機器上已啟用複寫的磁片，並藉由將不同的區塊從主要複本複寫到復原，來修正任何複寫資料完整性問題。</span><span class="sxs-lookup"><span data-stu-id="b2261-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2261-107">語法</span><span class="sxs-lookup"><span data-stu-id="b2261-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b2261-108">參數</span><span class="sxs-lookup"><span data-stu-id="b2261-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2261-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2261-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2261-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要重新同步處理的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b2261-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="b2261-111">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2261-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2261-112">重新同步處理作業開始的排程開始時間。</span><span class="sxs-lookup"><span data-stu-id="b2261-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="b2261-113">如果此參數為 **Null**，則會立即啟動重新同步作業。</span><span class="sxs-lookup"><span data-stu-id="b2261-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="b2261-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2261-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2261-115">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="b2261-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2261-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2261-116">Return value</span></span>

<span data-ttu-id="b2261-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b2261-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b2261-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b2261-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b2261-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="b2261-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="b2261-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="b2261-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="b2261-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="b2261-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="b2261-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-126">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="b2261-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="b2261-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="b2261-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="b2261-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="b2261-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b2261-131">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="b2261-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b2261-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2261-132">Requirements</span></span>



| <span data-ttu-id="b2261-133">需求</span><span class="sxs-lookup"><span data-stu-id="b2261-133">Requirement</span></span> | <span data-ttu-id="b2261-134">值</span><span class="sxs-lookup"><span data-stu-id="b2261-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2261-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2261-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b2261-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2261-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2261-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2261-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b2261-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2261-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2261-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="b2261-139">Namespace</span></span><br/>                | <span data-ttu-id="b2261-140">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b2261-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2261-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b2261-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2261-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b2261-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2261-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b2261-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2261-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2261-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2261-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2261-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2261-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="b2261-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

