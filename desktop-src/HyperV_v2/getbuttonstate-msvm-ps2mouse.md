---
description: 抓取指定裝置按鈕的目前狀態。
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Msvm_Ps2Mouse 類別的 GetButtonState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8bb0df6ad49f0d260d95c6f65e0f0f481b393dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972068"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="b9fcf-103">Msvm Ps2Mouse 類別的 GetButtonState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b9fcf-103">GetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="b9fcf-104">抓取指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9fcf-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9fcf-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="b9fcf-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9fcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9fcf-107">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9fcf-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9fcf-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-108">Type: **uint32**</span></span>

<span data-ttu-id="b9fcf-109">要查詢之按鈕的索引（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="b9fcf-110">*buttonState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b9fcf-110">*buttonState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9fcf-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-111">Type: **boolean**</span></span>

<span data-ttu-id="b9fcf-112">按鈕目前的關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-112">The current down state of the button.</span></span> <span data-ttu-id="b9fcf-113">**True** 值表示按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9fcf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9fcf-114">Return value</span></span>

<span data-ttu-id="b9fcf-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-115">Type: **uint32**</span></span>

<span data-ttu-id="b9fcf-116">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-116">A return value of zero indicates success.</span></span> <span data-ttu-id="b9fcf-117">非零值表示查詢失敗。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="b9fcf-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-126">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b9fcf-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="b9fcf-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b9fcf-131">備註</span><span class="sxs-lookup"><span data-stu-id="b9fcf-131">Remarks</span></span>

<span data-ttu-id="b9fcf-132">存取 [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b9fcf-133">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="b9fcf-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9fcf-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9fcf-134">Requirements</span></span>



| <span data-ttu-id="b9fcf-135">需求</span><span class="sxs-lookup"><span data-stu-id="b9fcf-135">Requirement</span></span> | <span data-ttu-id="b9fcf-136">值</span><span class="sxs-lookup"><span data-stu-id="b9fcf-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9fcf-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9fcf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b9fcf-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9fcf-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9fcf-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9fcf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b9fcf-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9fcf-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9fcf-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9fcf-141">Namespace</span></span><br/>                | <span data-ttu-id="b9fcf-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b9fcf-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9fcf-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b9fcf-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9fcf-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b9fcf-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9fcf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b9fcf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9fcf-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9fcf-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9fcf-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9fcf-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9fcf-148">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

