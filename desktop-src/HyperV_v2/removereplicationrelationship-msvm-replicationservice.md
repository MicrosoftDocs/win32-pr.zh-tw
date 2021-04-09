---
description: 移除虛擬機器複寫關聯性，並在虛擬機器的主要複寫關聯性上運作。
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Msvm_ReplicationService 類別的 RemoveReplicationRelationship 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848197"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="94f1e-103">Msvm ReplicationService 類別的 RemoveReplicationRelationship 方法 \_</span><span class="sxs-lookup"><span data-stu-id="94f1e-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="94f1e-104">移除虛擬機器複寫關聯性，並在虛擬機器的主要複寫關聯性上運作。</span><span class="sxs-lookup"><span data-stu-id="94f1e-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="94f1e-105">從 Windows 8.1 開始，建議您不再使用 **RemoveReplicationRelationship** 來移除虛擬機器複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="94f1e-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="94f1e-106">相反地，請使用 [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)。</span><span class="sxs-lookup"><span data-stu-id="94f1e-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="94f1e-107">語法</span><span class="sxs-lookup"><span data-stu-id="94f1e-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="94f1e-108">參數</span><span class="sxs-lookup"><span data-stu-id="94f1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f1e-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94f1e-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應移除複寫關聯性的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="94f1e-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="94f1e-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94f1e-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="94f1e-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f1e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="94f1e-113">Return value</span></span>

<span data-ttu-id="94f1e-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="94f1e-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="94f1e-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="94f1e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="94f1e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="94f1e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="94f1e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="94f1e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="94f1e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="94f1e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="94f1e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="94f1e-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="94f1e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="94f1e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="94f1e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="94f1e-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="94f1e-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="94f1e-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="94f1e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="94f1e-129">Requirements</span></span>



| <span data-ttu-id="94f1e-130">需求</span><span class="sxs-lookup"><span data-stu-id="94f1e-130">Requirement</span></span> | <span data-ttu-id="94f1e-131">值</span><span class="sxs-lookup"><span data-stu-id="94f1e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94f1e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94f1e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="94f1e-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94f1e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94f1e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="94f1e-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94f1e-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94f1e-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="94f1e-136">Namespace</span></span><br/>                | <span data-ttu-id="94f1e-137">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="94f1e-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94f1e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="94f1e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94f1e-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="94f1e-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94f1e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="94f1e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94f1e-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94f1e-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94f1e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94f1e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f1e-143">**>createreplicationrelationship**</span><span class="sxs-lookup"><span data-stu-id="94f1e-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="94f1e-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="94f1e-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

