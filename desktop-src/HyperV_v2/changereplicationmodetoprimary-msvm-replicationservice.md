---
description: 將延伸複寫關聯性變更為複本虛擬機器的主要關聯性。 複本虛擬機器必須處於容錯移轉認可狀態。
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: Msvm_ReplicationService：： ChangeReplicationModeToPrimary 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972381"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="80b24-104">Msvm \_ ReplicationService：： ChangeReplicationModeToPrimary 方法</span><span class="sxs-lookup"><span data-stu-id="80b24-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="80b24-105">將延伸複寫關聯性變更為複本虛擬機器的主要關聯性。</span><span class="sxs-lookup"><span data-stu-id="80b24-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="80b24-106">複本虛擬機器必須處於容錯移轉認可狀態。</span><span class="sxs-lookup"><span data-stu-id="80b24-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b24-107">語法</span><span class="sxs-lookup"><span data-stu-id="80b24-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="80b24-108">參數</span><span class="sxs-lookup"><span data-stu-id="80b24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b24-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="80b24-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b24-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，該實例表示此方法會將擴充複寫關聯性變更為主要關聯性的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="80b24-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="80b24-111">*ReplicationRelationship* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80b24-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b24-112">[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別之內嵌實例的字串表示，定義此方法變更為主要關聯性的延伸複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="80b24-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="80b24-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80b24-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80b24-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="80b24-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="80b24-115">如果工作已完成，此參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="80b24-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80b24-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="80b24-116">Return value</span></span>

<span data-ttu-id="80b24-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80b24-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="80b24-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="80b24-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="80b24-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="80b24-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="80b24-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="80b24-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="80b24-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="80b24-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="80b24-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="80b24-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="80b24-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="80b24-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="80b24-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="80b24-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="80b24-131">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="80b24-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80b24-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="80b24-132">Requirements</span></span>



| <span data-ttu-id="80b24-133">需求</span><span class="sxs-lookup"><span data-stu-id="80b24-133">Requirement</span></span> | <span data-ttu-id="80b24-134">值</span><span class="sxs-lookup"><span data-stu-id="80b24-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b24-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80b24-135">Minimum supported client</span></span><br/> | <span data-ttu-id="80b24-136">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80b24-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="80b24-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80b24-137">Minimum supported server</span></span><br/> | <span data-ttu-id="80b24-138">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80b24-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="80b24-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="80b24-139">Namespace</span></span><br/>                | <span data-ttu-id="80b24-140">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="80b24-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="80b24-141">MOF</span><span class="sxs-lookup"><span data-stu-id="80b24-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80b24-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="80b24-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80b24-143">DLL</span><span class="sxs-lookup"><span data-stu-id="80b24-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80b24-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80b24-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80b24-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80b24-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b24-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="80b24-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

