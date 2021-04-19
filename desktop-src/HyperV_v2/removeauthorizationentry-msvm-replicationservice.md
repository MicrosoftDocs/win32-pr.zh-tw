---
description: 從復原伺服器移除授權專案。
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Msvm_ReplicationService 類別的 RemoveAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975926"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="3d3da-103">Msvm ReplicationService 類別的 RemoveAuthorizationEntry 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3d3da-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="3d3da-104">從復原伺服器移除授權專案。</span><span class="sxs-lookup"><span data-stu-id="3d3da-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3da-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d3da-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3d3da-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d3da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d3da-107">*AllowedPrimaryHostSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d3da-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3da-108">將從伺服器移除其授權專案的主伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d3da-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="3d3da-109">這與 [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別的 **AllowedPrimaryHostSystem** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="3d3da-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3d3da-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3d3da-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3da-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3d3da-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d3da-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d3da-112">Return value</span></span>

<span data-ttu-id="3d3da-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3d3da-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3d3da-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="3d3da-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="3d3da-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="3d3da-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="3d3da-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="3d3da-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="3d3da-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="3d3da-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="3d3da-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-122">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="3d3da-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="3d3da-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="3d3da-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="3d3da-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="3d3da-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3d3da-127">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="3d3da-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3d3da-128">備註</span><span class="sxs-lookup"><span data-stu-id="3d3da-128">Remarks</span></span>

<span data-ttu-id="3d3da-129">移除授權專案將會停止所有以該專案授權之虛擬機器的複寫。</span><span class="sxs-lookup"><span data-stu-id="3d3da-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3da-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d3da-130">Requirements</span></span>



| <span data-ttu-id="3d3da-131">需求</span><span class="sxs-lookup"><span data-stu-id="3d3da-131">Requirement</span></span> | <span data-ttu-id="3d3da-132">值</span><span class="sxs-lookup"><span data-stu-id="3d3da-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3da-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d3da-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3da-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d3da-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3d3da-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d3da-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3da-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d3da-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d3da-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d3da-137">Namespace</span></span><br/>                | <span data-ttu-id="3d3da-138">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3d3da-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3d3da-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3d3da-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d3da-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3d3da-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d3da-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3d3da-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d3da-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d3da-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3d3da-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d3da-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3da-144">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3d3da-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3d3da-145">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3d3da-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3d3da-146">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="3d3da-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3d3da-147">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="3d3da-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

