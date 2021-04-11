---
description: 在相關聯的子虛擬機器上起始作業系統關閉操作。 如果傳回零 (0) ，則會成功啟動關機。 任何其他傳回碼表示錯誤狀況。
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: 'Msvm_ShutdownComponent 類別的 InitiateShutdown 方法 (Winreg. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193507"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="4e0e4-105">Msvm ShutdownComponent 類別的 InitiateShutdown 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4e0e4-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="4e0e4-106">在相關聯的子虛擬機器上起始作業系統關閉操作。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="4e0e4-107">如果傳回零 (0) ，則會成功啟動關機。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="4e0e4-108">任何其他傳回碼表示錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0e4-109">語法</span><span class="sxs-lookup"><span data-stu-id="4e0e4-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="4e0e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e0e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0e4-111">*Force* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4e0e4-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0e4-112">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4e0e4-112">Type: **boolean**</span></span>

<span data-ttu-id="4e0e4-113">若 **為 True，則** 會強制關閉應用程式，儘管有尚未儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="4e0e4-114">*原因* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e0e4-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0e4-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4e0e4-115">Type: **string**</span></span>

<span data-ttu-id="4e0e4-116">關機操作的原因。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="4e0e4-117">這是使用者定義的字串。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e0e4-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e0e4-118">Return value</span></span>

<span data-ttu-id="4e0e4-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4e0e4-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="4e0e4-120">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-122">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-123">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-124">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-125">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-126">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-127">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-128">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-129">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-130">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-131">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-132">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-133">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-134">**系統未就緒** (32780) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-135">**電腦已鎖定，無法在沒有強制選項的情況下關閉** (32781) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="4e0e4-136">**系統關機正在進行中** (32782) </span><span class="sxs-lookup"><span data-stu-id="4e0e4-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4e0e4-137">備註</span><span class="sxs-lookup"><span data-stu-id="4e0e4-137">Remarks</span></span>

<span data-ttu-id="4e0e4-138">存取 [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4e0e4-139">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4e0e4-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0e4-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e0e4-140">Requirements</span></span>



| <span data-ttu-id="4e0e4-141">需求</span><span class="sxs-lookup"><span data-stu-id="4e0e4-141">Requirement</span></span> | <span data-ttu-id="4e0e4-142">值</span><span class="sxs-lookup"><span data-stu-id="4e0e4-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0e4-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e0e4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0e4-144">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e0e4-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4e0e4-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e0e4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0e4-146">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e0e4-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e0e4-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e0e4-147">Namespace</span></span><br/>                | <span data-ttu-id="4e0e4-148">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4e0e4-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4e0e4-149">標頭</span><span class="sxs-lookup"><span data-stu-id="4e0e4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e0e4-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0e4-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="4e0e4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="4e0e4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e0e4-152"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4e0e4-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e0e4-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4e0e4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e0e4-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e0e4-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e0e4-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e0e4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0e4-156">**Msvm \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="4e0e4-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

