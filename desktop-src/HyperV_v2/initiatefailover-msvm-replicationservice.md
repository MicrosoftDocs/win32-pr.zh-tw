---
description: 起始虛擬機器對應用程式或標準複寫點映射的容錯移轉。
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Msvm_ReplicationService 類別的 InitiateFailover 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318792"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="75c6e-103">Msvm ReplicationService 類別的 InitiateFailover 方法 \_</span><span class="sxs-lookup"><span data-stu-id="75c6e-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="75c6e-104">起始虛擬機器對應用程式或標準複寫點映射的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="75c6e-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c6e-105">語法</span><span class="sxs-lookup"><span data-stu-id="75c6e-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="75c6e-106">參數</span><span class="sxs-lookup"><span data-stu-id="75c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c6e-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="75c6e-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c6e-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要起始容錯移轉的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="75c6e-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="75c6e-109">*SnapshotSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75c6e-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c6e-110">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))實例的參考，代表用於容錯移轉的快照集。</span><span class="sxs-lookup"><span data-stu-id="75c6e-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="75c6e-111">如果此參數為 **Null**，則會將容錯移轉執行至最近的時間點。</span><span class="sxs-lookup"><span data-stu-id="75c6e-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="75c6e-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="75c6e-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75c6e-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="75c6e-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c6e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="75c6e-114">Return value</span></span>

<span data-ttu-id="75c6e-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="75c6e-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75c6e-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="75c6e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="75c6e-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="75c6e-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="75c6e-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="75c6e-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="75c6e-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="75c6e-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="75c6e-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="75c6e-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="75c6e-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="75c6e-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="75c6e-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="75c6e-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="75c6e-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="75c6e-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75c6e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="75c6e-130">Requirements</span></span>



| <span data-ttu-id="75c6e-131">需求</span><span class="sxs-lookup"><span data-stu-id="75c6e-131">Requirement</span></span> | <span data-ttu-id="75c6e-132">值</span><span class="sxs-lookup"><span data-stu-id="75c6e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c6e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75c6e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="75c6e-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75c6e-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75c6e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75c6e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="75c6e-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75c6e-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75c6e-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="75c6e-137">Namespace</span></span><br/>                | <span data-ttu-id="75c6e-138">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="75c6e-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75c6e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="75c6e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75c6e-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="75c6e-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75c6e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="75c6e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c6e-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75c6e-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75c6e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75c6e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c6e-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="75c6e-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="75c6e-145">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="75c6e-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="75c6e-146">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="75c6e-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

