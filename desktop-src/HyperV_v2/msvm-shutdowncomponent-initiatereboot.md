---
description: 在相關聯的子虛擬機器上起始作業系統重新開機操作。
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Msvm_ShutdownComponent 類別的 InitiateReboot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991767"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="cbc78-103">Msvm ShutdownComponent 類別的 InitiateReboot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cbc78-103">InitiateReboot method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="cbc78-104">在相關聯的子虛擬機器上起始作業系統重新開機操作。</span><span class="sxs-lookup"><span data-stu-id="cbc78-104">Initiates an operating system reboot operation on the associated child virtual machine.</span></span>

<span data-ttu-id="cbc78-105">如果傳回零 (0) ，則會成功啟動重新開機。</span><span class="sxs-lookup"><span data-stu-id="cbc78-105">If zero (0) is returned, then the reboot was initiated successfully.</span></span> <span data-ttu-id="cbc78-106">任何其他傳回碼表示錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="cbc78-106">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc78-107">語法</span><span class="sxs-lookup"><span data-stu-id="cbc78-107">Syntax</span></span>


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="cbc78-108">參數</span><span class="sxs-lookup"><span data-stu-id="cbc78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc78-109">*Force* \[in\]</span><span class="sxs-lookup"><span data-stu-id="cbc78-109">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc78-110">若為 TRUE，則會強制關閉應用程式，儘管有尚未儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="cbc78-110">A flag which, if TRUE, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="cbc78-111">*原因* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cbc78-111">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc78-112">重新開機操作的原因。</span><span class="sxs-lookup"><span data-stu-id="cbc78-112">The reason for the reboot operation.</span></span> <span data-ttu-id="cbc78-113">這是使用者定義的字串。</span><span class="sxs-lookup"><span data-stu-id="cbc78-113">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc78-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbc78-114">Return value</span></span>

<span data-ttu-id="cbc78-115">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cbc78-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="cbc78-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="cbc78-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="cbc78-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="cbc78-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="cbc78-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="cbc78-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="cbc78-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="cbc78-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="cbc78-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-124">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="cbc78-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="cbc78-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="cbc78-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="cbc78-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="cbc78-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="cbc78-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-130">**系統未就緒** (32780) </span><span class="sxs-lookup"><span data-stu-id="cbc78-130">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-131">**電腦已鎖定，無法在沒有強制選項的情況下關閉** (32781) </span><span class="sxs-lookup"><span data-stu-id="cbc78-131">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="cbc78-132">**系統關機正在進行中** (32782) </span><span class="sxs-lookup"><span data-stu-id="cbc78-132">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cbc78-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbc78-133">Requirements</span></span>



| <span data-ttu-id="cbc78-134">需求</span><span class="sxs-lookup"><span data-stu-id="cbc78-134">Requirement</span></span> | <span data-ttu-id="cbc78-135">值</span><span class="sxs-lookup"><span data-stu-id="cbc78-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc78-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbc78-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc78-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbc78-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cbc78-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbc78-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc78-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cbc78-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cbc78-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="cbc78-140">Namespace</span></span><br/>                | <span data-ttu-id="cbc78-141">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="cbc78-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cbc78-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cbc78-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbc78-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cbc78-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbc78-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc78-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc78-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbc78-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbc78-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbc78-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc78-147">**Msvm \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="cbc78-147">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




