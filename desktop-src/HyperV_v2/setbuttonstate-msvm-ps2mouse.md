---
description: 設定指定裝置按鈕的目前狀態。
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: Msvm_Ps2Mouse 類別的 SetButtonState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34475edfa27d08cbe9de488502686a84e4391eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974443"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="9b6d2-103">Msvm Ps2Mouse 類別的 SetButtonState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9b6d2-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="9b6d2-104">設定指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b6d2-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="9b6d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b6d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6d2-107">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b6d2-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6d2-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d2-108">Type: **uint32**</span></span>

<span data-ttu-id="9b6d2-109">要修改之按鈕的以1起始的索引。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="9b6d2-110">*buttonState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b6d2-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6d2-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9b6d2-111">Type: **boolean**</span></span>

<span data-ttu-id="9b6d2-112">按鈕的新關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-112">The new down state of the button.</span></span> <span data-ttu-id="9b6d2-113">**True** 值表示按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6d2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b6d2-114">Return value</span></span>

<span data-ttu-id="9b6d2-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9b6d2-115">Type: **uint32**</span></span>

<span data-ttu-id="9b6d2-116">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-116">A return value of zero indicates success.</span></span> <span data-ttu-id="9b6d2-117">非零值表示無法修改按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="9b6d2-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-126">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9b6d2-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="9b6d2-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9b6d2-131">備註</span><span class="sxs-lookup"><span data-stu-id="9b6d2-131">Remarks</span></span>

<span data-ttu-id="9b6d2-132">存取 [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9b6d2-133">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="9b6d2-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6d2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b6d2-134">Requirements</span></span>



| <span data-ttu-id="9b6d2-135">需求</span><span class="sxs-lookup"><span data-stu-id="9b6d2-135">Requirement</span></span> | <span data-ttu-id="9b6d2-136">值</span><span class="sxs-lookup"><span data-stu-id="9b6d2-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6d2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b6d2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6d2-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b6d2-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9b6d2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b6d2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6d2-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b6d2-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b6d2-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="9b6d2-141">Namespace</span></span><br/>                | <span data-ttu-id="9b6d2-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9b6d2-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9b6d2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9b6d2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b6d2-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d2-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b6d2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9b6d2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b6d2-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b6d2-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b6d2-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b6d2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6d2-148">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="9b6d2-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

