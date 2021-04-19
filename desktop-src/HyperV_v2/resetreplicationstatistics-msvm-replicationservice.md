---
description: 重設虛擬機器的複寫統計資料，並在虛擬機器的主要複寫關聯性上運作。
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Msvm_ReplicationService 類別的 ResetReplicationStatistics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001714"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="956bb-103">Msvm ReplicationService 類別的 ResetReplicationStatistics 方法 \_</span><span class="sxs-lookup"><span data-stu-id="956bb-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="956bb-104">重設虛擬機器的複寫統計資料，並在虛擬機器的主要複寫關聯性上運作。</span><span class="sxs-lookup"><span data-stu-id="956bb-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="956bb-105">從 Windows 8.1 開始，建議您不再使用 **ResetReplicationStatistics** 來重設複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="956bb-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="956bb-106">相反地，請使用 [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)。</span><span class="sxs-lookup"><span data-stu-id="956bb-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="956bb-107">語法</span><span class="sxs-lookup"><span data-stu-id="956bb-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="956bb-108">參數</span><span class="sxs-lookup"><span data-stu-id="956bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956bb-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="956bb-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="956bb-110">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)系統類型實例的參考，代表要重設其複寫統計資料的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="956bb-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="956bb-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="956bb-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="956bb-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="956bb-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956bb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="956bb-113">Return value</span></span>

<span data-ttu-id="956bb-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="956bb-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="956bb-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="956bb-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="956bb-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="956bb-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="956bb-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="956bb-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="956bb-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="956bb-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="956bb-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-123">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="956bb-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="956bb-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="956bb-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="956bb-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="956bb-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="956bb-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="956bb-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="956bb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="956bb-129">Requirements</span></span>



| <span data-ttu-id="956bb-130">需求</span><span class="sxs-lookup"><span data-stu-id="956bb-130">Requirement</span></span> | <span data-ttu-id="956bb-131">值</span><span class="sxs-lookup"><span data-stu-id="956bb-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="956bb-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="956bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="956bb-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="956bb-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="956bb-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="956bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="956bb-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="956bb-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="956bb-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="956bb-136">Namespace</span></span><br/>                | <span data-ttu-id="956bb-137">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="956bb-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="956bb-138">MOF</span><span class="sxs-lookup"><span data-stu-id="956bb-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="956bb-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="956bb-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="956bb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="956bb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="956bb-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="956bb-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="956bb-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="956bb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="956bb-143">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="956bb-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="956bb-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="956bb-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

