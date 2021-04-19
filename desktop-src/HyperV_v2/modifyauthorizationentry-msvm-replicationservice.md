---
description: 修改修復伺服器的授權專案。
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Msvm_ReplicationService 類別的 ModifyAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984626"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="41483-103">Msvm ReplicationService 類別的 ModifyAuthorizationEntry 方法 \_</span><span class="sxs-lookup"><span data-stu-id="41483-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="41483-104">修改修復伺服器的授權專案。</span><span class="sxs-lookup"><span data-stu-id="41483-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="41483-105">語法</span><span class="sxs-lookup"><span data-stu-id="41483-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="41483-106">參數</span><span class="sxs-lookup"><span data-stu-id="41483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41483-107">*AuthorizationEntry* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41483-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41483-108">[**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別實例的字串表示，定義要修改的授權專案。</span><span class="sxs-lookup"><span data-stu-id="41483-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="41483-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="41483-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41483-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="41483-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41483-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="41483-111">Return value</span></span>

<span data-ttu-id="41483-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41483-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="41483-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="41483-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41483-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="41483-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="41483-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="41483-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="41483-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="41483-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="41483-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="41483-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="41483-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="41483-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="41483-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="41483-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="41483-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="41483-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="41483-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="41483-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="41483-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="41483-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="41483-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="41483-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="41483-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="41483-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="41483-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="41483-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="41483-126">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="41483-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="41483-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="41483-127">Requirements</span></span>



| <span data-ttu-id="41483-128">需求</span><span class="sxs-lookup"><span data-stu-id="41483-128">Requirement</span></span> | <span data-ttu-id="41483-129">值</span><span class="sxs-lookup"><span data-stu-id="41483-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41483-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41483-130">Minimum supported client</span></span><br/> | <span data-ttu-id="41483-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41483-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41483-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41483-132">Minimum supported server</span></span><br/> | <span data-ttu-id="41483-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41483-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41483-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="41483-134">Namespace</span></span><br/>                | <span data-ttu-id="41483-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="41483-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41483-136">MOF</span><span class="sxs-lookup"><span data-stu-id="41483-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41483-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="41483-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41483-138">DLL</span><span class="sxs-lookup"><span data-stu-id="41483-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41483-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41483-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41483-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41483-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41483-141">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="41483-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="41483-142">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="41483-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="41483-143">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="41483-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="41483-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="41483-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

