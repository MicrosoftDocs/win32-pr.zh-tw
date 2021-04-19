---
description: 移除指定的虛擬機器複寫關聯性。
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: Msvm_ReplicationService：： RemoveReplicationRelationshipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989921"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="5b9a0-103">Msvm \_ ReplicationService：： RemoveReplicationRelationshipEx 方法</span><span class="sxs-lookup"><span data-stu-id="5b9a0-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="5b9a0-104">移除指定的虛擬機器複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b9a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b9a0-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="5b9a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b9a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b9a0-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b9a0-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9a0-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要移除複寫的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="5b9a0-109">*ReplicationRelationship* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b9a0-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9a0-110">[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別之內嵌實例的字串表示，其定義要移除的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="5b9a0-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b9a0-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9a0-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="5b9a0-113">如果工作已完成，此參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b9a0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b9a0-114">Return value</span></span>

<span data-ttu-id="5b9a0-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5b9a0-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5b9a0-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="5b9a0-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5b9a0-130">備註</span><span class="sxs-lookup"><span data-stu-id="5b9a0-130">Remarks</span></span>

<span data-ttu-id="5b9a0-131">若為複本虛擬機器，如果已啟用延伸複寫，則無法移除主要複寫。</span><span class="sxs-lookup"><span data-stu-id="5b9a0-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b9a0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b9a0-132">Requirements</span></span>



| <span data-ttu-id="5b9a0-133">需求</span><span class="sxs-lookup"><span data-stu-id="5b9a0-133">Requirement</span></span> | <span data-ttu-id="5b9a0-134">值</span><span class="sxs-lookup"><span data-stu-id="5b9a0-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9a0-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b9a0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5b9a0-136">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b9a0-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5b9a0-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b9a0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5b9a0-138">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b9a0-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5b9a0-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b9a0-139">Namespace</span></span><br/>                | <span data-ttu-id="5b9a0-140">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5b9a0-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="5b9a0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5b9a0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b9a0-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5b9a0-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b9a0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5b9a0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b9a0-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b9a0-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b9a0-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b9a0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b9a0-146">**>createreplicationrelationship**</span><span class="sxs-lookup"><span data-stu-id="5b9a0-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="5b9a0-147">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="5b9a0-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

