---
description: 重設與指定之虛擬機器的指定複寫關聯性相關聯的複寫統計資料。
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: Msvm_ReplicationService：： ResetReplicationStatisticsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850268"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="e9136-103">Msvm \_ ReplicationService：： ResetReplicationStatisticsEx 方法</span><span class="sxs-lookup"><span data-stu-id="e9136-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="e9136-104">重設與指定之虛擬機器的指定複寫關聯性相關聯的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="e9136-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9136-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9136-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="e9136-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9136-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9136-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9136-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9136-108">表示已啟用複本之虛擬機器之 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例實例的參考。</span><span class="sxs-lookup"><span data-stu-id="e9136-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e9136-109">*ReplicationRelationship* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9136-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9136-110">[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別之內嵌實例的字串表示，其定義要重設複寫統計資料的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="e9136-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="e9136-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9136-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9136-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e9136-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="e9136-113">如果工作已完成，此參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e9136-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9136-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9136-114">Return value</span></span>

<span data-ttu-id="e9136-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e9136-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e9136-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e9136-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e9136-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="e9136-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="e9136-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="e9136-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="e9136-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="e9136-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="e9136-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-124">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="e9136-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="e9136-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="e9136-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="e9136-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="e9136-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e9136-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="e9136-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e9136-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9136-130">Requirements</span></span>



| <span data-ttu-id="e9136-131">需求</span><span class="sxs-lookup"><span data-stu-id="e9136-131">Requirement</span></span> | <span data-ttu-id="e9136-132">值</span><span class="sxs-lookup"><span data-stu-id="e9136-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9136-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9136-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e9136-134">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9136-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e9136-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9136-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e9136-136">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9136-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9136-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9136-137">Namespace</span></span><br/>                | <span data-ttu-id="e9136-138">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e9136-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e9136-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e9136-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9136-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e9136-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9136-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e9136-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9136-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9136-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9136-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9136-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9136-144">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="e9136-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e9136-145">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="e9136-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

