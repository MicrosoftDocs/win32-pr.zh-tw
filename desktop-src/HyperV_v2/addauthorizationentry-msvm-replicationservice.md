---
description: 將授權專案新增至復原伺服器。
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Msvm_ReplicationService 類別的 AddAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993143"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a3aec-103">Msvm ReplicationService 類別的 AddAuthorizationEntry 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a3aec-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a3aec-104">將授權專案新增至復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="a3aec-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="a3aec-105">這些專案是用來授權恢復伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="a3aec-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3aec-106">語法</span><span class="sxs-lookup"><span data-stu-id="a3aec-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a3aec-107">參數</span><span class="sxs-lookup"><span data-stu-id="a3aec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3aec-108">*AuthorizationEntry* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3aec-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3aec-109">[**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別實例的字串表示，定義要加入的授權專案。</span><span class="sxs-lookup"><span data-stu-id="a3aec-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="a3aec-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3aec-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3aec-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a3aec-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3aec-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3aec-112">Return value</span></span>

<span data-ttu-id="a3aec-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a3aec-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a3aec-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a3aec-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a3aec-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="a3aec-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="a3aec-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="a3aec-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="a3aec-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="a3aec-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="a3aec-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-122">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="a3aec-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="a3aec-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="a3aec-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="a3aec-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="a3aec-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a3aec-127">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="a3aec-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a3aec-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3aec-128">Requirements</span></span>



| <span data-ttu-id="a3aec-129">需求</span><span class="sxs-lookup"><span data-stu-id="a3aec-129">Requirement</span></span> | <span data-ttu-id="a3aec-130">值</span><span class="sxs-lookup"><span data-stu-id="a3aec-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3aec-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3aec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a3aec-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3aec-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a3aec-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3aec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a3aec-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3aec-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3aec-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="a3aec-135">Namespace</span></span><br/>                | <span data-ttu-id="a3aec-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a3aec-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a3aec-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a3aec-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3aec-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a3aec-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3aec-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a3aec-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3aec-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3aec-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a3aec-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3aec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3aec-142">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a3aec-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a3aec-143">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a3aec-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a3aec-144">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a3aec-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a3aec-145">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="a3aec-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

