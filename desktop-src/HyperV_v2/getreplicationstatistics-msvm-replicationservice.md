---
description: 抓取虛擬機器的複寫統計資料，並在虛擬機器的主要複寫關聯性上運作。
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Msvm_ReplicationService 類別的 GetReplicationStatistics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971426"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="2f64f-103">Msvm ReplicationService 類別的 GetReplicationStatistics 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2f64f-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2f64f-104">抓取虛擬機器的複寫統計資料，並在虛擬機器的主要複寫關聯性上運作。</span><span class="sxs-lookup"><span data-stu-id="2f64f-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="2f64f-105">從 Windows 8.1 開始，建議您不再使用 **GetReplicationStatistics** 來取出複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="2f64f-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="2f64f-106">相反地，請使用 [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f64f-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2f64f-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f64f-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2f64f-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f64f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f64f-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f64f-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f64f-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要取得其複寫統計資料的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f64f-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="2f64f-111">*ReplicationStatistics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f64f-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f64f-112">如果成功，則會收到 [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) 類別的內嵌實例，其中包含所要求之虛擬機器的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="2f64f-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2f64f-113">*ReplicationHealthIssues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f64f-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f64f-114">如果成功，會接收 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例陣列，指出所要求之虛擬機器的任何複寫警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f64f-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2f64f-115">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f64f-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f64f-116">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="2f64f-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f64f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f64f-117">Return value</span></span>

<span data-ttu-id="2f64f-118">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2f64f-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2f64f-119">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2f64f-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-120">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2f64f-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-121">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="2f64f-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-122">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="2f64f-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-123">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="2f64f-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-124">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="2f64f-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-125">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="2f64f-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-126">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="2f64f-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-127">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="2f64f-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-128">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="2f64f-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-129">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="2f64f-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-130">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="2f64f-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-131">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="2f64f-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2f64f-132">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="2f64f-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2f64f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f64f-133">Requirements</span></span>



| <span data-ttu-id="2f64f-134">需求</span><span class="sxs-lookup"><span data-stu-id="2f64f-134">Requirement</span></span> | <span data-ttu-id="2f64f-135">值</span><span class="sxs-lookup"><span data-stu-id="2f64f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f64f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f64f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f64f-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f64f-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f64f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f64f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f64f-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f64f-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f64f-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f64f-140">Namespace</span></span><br/>                | <span data-ttu-id="2f64f-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2f64f-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f64f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2f64f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f64f-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2f64f-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f64f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2f64f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f64f-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f64f-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f64f-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f64f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f64f-147">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="2f64f-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2f64f-148">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="2f64f-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

