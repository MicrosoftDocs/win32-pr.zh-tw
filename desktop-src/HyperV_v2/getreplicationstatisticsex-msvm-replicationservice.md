---
description: 抓取與虛擬機器的指定複寫關聯性相關聯的複寫統計資料。
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: Msvm_ReplicationService：： GetReplicationStatisticsEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971425"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="5fee9-103">Msvm \_ ReplicationService：： GetReplicationStatisticsEx 方法</span><span class="sxs-lookup"><span data-stu-id="5fee9-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="5fee9-104">抓取與虛擬機器的指定複寫關聯性相關聯的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="5fee9-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fee9-105">語法</span><span class="sxs-lookup"><span data-stu-id="5fee9-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="5fee9-106">參數</span><span class="sxs-lookup"><span data-stu-id="5fee9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fee9-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fee9-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要取得其複寫統計資料的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5fee9-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="5fee9-109">*ReplicationRelationship* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fee9-110">[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別之內嵌實例的字串表示，它會定義要取得其複寫統計資料的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="5fee9-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="5fee9-111">*ReplicationStatistics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fee9-112">如果成功，則會收到 [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) 類別的內嵌實例，其中包含所要求複寫關聯性的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="5fee9-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="5fee9-113">*ReplicationHealthIssues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fee9-114">如果成功，會接收 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例陣列，指出所要求之虛擬機器的任何複寫警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fee9-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="5fee9-115">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fee9-116">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="5fee9-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="5fee9-117">如果工作已完成，此參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5fee9-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fee9-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fee9-118">Return value</span></span>

<span data-ttu-id="5fee9-119">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5fee9-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5fee9-120">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="5fee9-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="5fee9-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-122">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="5fee9-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-123">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="5fee9-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-124">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="5fee9-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-125">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="5fee9-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-126">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="5fee9-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-127">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="5fee9-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-128">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="5fee9-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-129">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="5fee9-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-130">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="5fee9-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-131">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="5fee9-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-132">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="5fee9-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5fee9-133">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="5fee9-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5fee9-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fee9-134">Requirements</span></span>



| <span data-ttu-id="5fee9-135">需求</span><span class="sxs-lookup"><span data-stu-id="5fee9-135">Requirement</span></span> | <span data-ttu-id="5fee9-136">值</span><span class="sxs-lookup"><span data-stu-id="5fee9-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fee9-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fee9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5fee9-138">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5fee9-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fee9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5fee9-140">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5fee9-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="5fee9-141">Namespace</span></span><br/>                | <span data-ttu-id="5fee9-142">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5fee9-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="5fee9-143">MOF</span><span class="sxs-lookup"><span data-stu-id="5fee9-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fee9-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5fee9-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fee9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5fee9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fee9-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fee9-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fee9-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fee9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fee9-148">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="5fee9-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="5fee9-149">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="5fee9-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

