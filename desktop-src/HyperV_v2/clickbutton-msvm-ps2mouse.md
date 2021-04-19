---
description: 模擬指定裝置按鈕的點擊。
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Msvm_Ps2Mouse 類別的 ClickButton 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985431"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="2dd70-103">Msvm Ps2Mouse 類別的 ClickButton 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2dd70-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="2dd70-104">模擬指定裝置按鈕的點擊。</span><span class="sxs-lookup"><span data-stu-id="2dd70-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="2dd70-105">這相當於呼叫 [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) 兩次，先按下按鈕，然後再放開。</span><span class="sxs-lookup"><span data-stu-id="2dd70-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd70-106">語法</span><span class="sxs-lookup"><span data-stu-id="2dd70-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="2dd70-107">參數</span><span class="sxs-lookup"><span data-stu-id="2dd70-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd70-108">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2dd70-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd70-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2dd70-109">Type: **uint32**</span></span>

<span data-ttu-id="2dd70-110">以1為基的按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="2dd70-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd70-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dd70-111">Return value</span></span>

<span data-ttu-id="2dd70-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2dd70-112">Type: **uint32**</span></span>

<span data-ttu-id="2dd70-113">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="2dd70-113">A return value of zero indicates success.</span></span> <span data-ttu-id="2dd70-114">非零值表示無法修改按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="2dd70-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="2dd70-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2dd70-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2dd70-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="2dd70-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="2dd70-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="2dd70-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="2dd70-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="2dd70-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="2dd70-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-123">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="2dd70-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="2dd70-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="2dd70-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="2dd70-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2dd70-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="2dd70-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2dd70-128">備註</span><span class="sxs-lookup"><span data-stu-id="2dd70-128">Remarks</span></span>

<span data-ttu-id="2dd70-129">存取 [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="2dd70-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2dd70-130">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="2dd70-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd70-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dd70-131">Requirements</span></span>



| <span data-ttu-id="2dd70-132">需求</span><span class="sxs-lookup"><span data-stu-id="2dd70-132">Requirement</span></span> | <span data-ttu-id="2dd70-133">值</span><span class="sxs-lookup"><span data-stu-id="2dd70-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd70-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2dd70-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd70-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dd70-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2dd70-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2dd70-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd70-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2dd70-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2dd70-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="2dd70-138">Namespace</span></span><br/>                | <span data-ttu-id="2dd70-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2dd70-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2dd70-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2dd70-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dd70-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2dd70-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2dd70-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2dd70-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dd70-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2dd70-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2dd70-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dd70-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd70-145">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="2dd70-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

