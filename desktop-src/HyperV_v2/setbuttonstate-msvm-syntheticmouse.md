---
description: 設定指定裝置按鈕的目前狀態。
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Msvm_SyntheticMouse 類別的 SetButtonState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192668"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="fbb93-103">Msvm SyntheticMouse 類別的 SetButtonState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fbb93-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="fbb93-104">設定指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fbb93-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb93-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbb93-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="fbb93-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbb93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb93-107">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb93-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb93-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fbb93-108">Type: **uint32**</span></span>

<span data-ttu-id="fbb93-109">要修改之按鈕的以1起始的索引。</span><span class="sxs-lookup"><span data-stu-id="fbb93-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="fbb93-110">*isDown* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb93-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb93-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fbb93-111">Type: **boolean**</span></span>

<span data-ttu-id="fbb93-112">按鈕的新關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="fbb93-112">The new down state of the button.</span></span> <span data-ttu-id="fbb93-113">**True** 值表示按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="fbb93-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb93-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb93-114">Return value</span></span>

<span data-ttu-id="fbb93-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fbb93-115">Type: **uint32**</span></span>

<span data-ttu-id="fbb93-116">非零值表示無法修改按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="fbb93-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="fbb93-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="fbb93-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="fbb93-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="fbb93-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="fbb93-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="fbb93-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="fbb93-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="fbb93-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="fbb93-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-125">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="fbb93-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="fbb93-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="fbb93-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="fbb93-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fbb93-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="fbb93-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fbb93-130">備註</span><span class="sxs-lookup"><span data-stu-id="fbb93-130">Remarks</span></span>

<span data-ttu-id="fbb93-131">存取 [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="fbb93-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fbb93-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="fbb93-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb93-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb93-133">Requirements</span></span>



| <span data-ttu-id="fbb93-134">需求</span><span class="sxs-lookup"><span data-stu-id="fbb93-134">Requirement</span></span> | <span data-ttu-id="fbb93-135">值</span><span class="sxs-lookup"><span data-stu-id="fbb93-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb93-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbb93-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb93-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb93-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbb93-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbb93-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb93-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb93-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbb93-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="fbb93-140">Namespace</span></span><br/>                | <span data-ttu-id="fbb93-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fbb93-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbb93-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fbb93-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbb93-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fbb93-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbb93-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fbb93-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbb93-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbb93-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbb93-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbb93-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb93-147">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="fbb93-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

