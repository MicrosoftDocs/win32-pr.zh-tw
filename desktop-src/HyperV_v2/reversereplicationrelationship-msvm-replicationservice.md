---
description: 將已容錯移轉的虛擬機器複寫回主伺服器。
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Msvm_ReplicationService 類別的 ReverseReplicationRelationship 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969346"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="132a0-103">Msvm ReplicationService 類別的 ReverseReplicationRelationship 方法 \_</span><span class="sxs-lookup"><span data-stu-id="132a0-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="132a0-104">將已容錯移轉的虛擬機器複寫回主伺服器。</span><span class="sxs-lookup"><span data-stu-id="132a0-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="132a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="132a0-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="132a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="132a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="132a0-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="132a0-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="132a0-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應反轉複寫的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="132a0-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="132a0-109">*ReplicationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="132a0-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="132a0-110">定義複寫設定之 [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) 類別實例的字串表示。</span><span class="sxs-lookup"><span data-stu-id="132a0-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="132a0-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="132a0-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="132a0-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="132a0-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="132a0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="132a0-113">Return value</span></span>

<span data-ttu-id="132a0-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="132a0-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="132a0-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="132a0-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="132a0-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="132a0-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="132a0-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="132a0-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="132a0-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="132a0-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="132a0-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="132a0-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="132a0-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="132a0-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="132a0-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="132a0-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="132a0-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="132a0-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="132a0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="132a0-129">Requirements</span></span>



| <span data-ttu-id="132a0-130">需求</span><span class="sxs-lookup"><span data-stu-id="132a0-130">Requirement</span></span> | <span data-ttu-id="132a0-131">值</span><span class="sxs-lookup"><span data-stu-id="132a0-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="132a0-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="132a0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="132a0-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="132a0-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="132a0-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="132a0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="132a0-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="132a0-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="132a0-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="132a0-136">Namespace</span></span><br/>                | <span data-ttu-id="132a0-137">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="132a0-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="132a0-138">MOF</span><span class="sxs-lookup"><span data-stu-id="132a0-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="132a0-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="132a0-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="132a0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="132a0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="132a0-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="132a0-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="132a0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="132a0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="132a0-143">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="132a0-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

