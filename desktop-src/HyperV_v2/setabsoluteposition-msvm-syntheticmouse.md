---
description: 設定滑鼠游標的水準和垂直位置。
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: 'Msvm_SyntheticMouse 類別的 SetAbsolutePosition 方法 (Dbdao) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849176"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="4d840-103">Msvm SyntheticMouse 類別的 SetAbsolutePosition 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4d840-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="4d840-104">設定滑鼠游標的水準和垂直位置。</span><span class="sxs-lookup"><span data-stu-id="4d840-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d840-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d840-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="4d840-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d840-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d840-107">*horizontalPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d840-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d840-108">類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4d840-108">Type: **sint32**</span></span>

<span data-ttu-id="4d840-109">滑鼠游標的新水準位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4d840-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4d840-110">*verticalPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d840-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d840-111">類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="4d840-111">Type: **sint32**</span></span>

<span data-ttu-id="4d840-112">滑鼠游標的新垂直位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4d840-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d840-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d840-113">Return value</span></span>

<span data-ttu-id="4d840-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4d840-114">Type: **uint32**</span></span>

<span data-ttu-id="4d840-115">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="4d840-115">A return value of zero indicates success.</span></span> <span data-ttu-id="4d840-116">非零值表示無法改變捲軸位置。</span><span class="sxs-lookup"><span data-stu-id="4d840-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="4d840-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="4d840-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="4d840-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="4d840-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="4d840-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="4d840-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="4d840-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="4d840-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="4d840-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-125">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="4d840-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="4d840-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="4d840-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="4d840-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4d840-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="4d840-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4d840-130">備註</span><span class="sxs-lookup"><span data-stu-id="4d840-130">Remarks</span></span>

<span data-ttu-id="4d840-131">存取 [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4d840-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4d840-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4d840-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d840-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d840-133">Requirements</span></span>



| <span data-ttu-id="4d840-134">需求</span><span class="sxs-lookup"><span data-stu-id="4d840-134">Requirement</span></span> | <span data-ttu-id="4d840-135">值</span><span class="sxs-lookup"><span data-stu-id="4d840-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d840-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d840-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4d840-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d840-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4d840-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d840-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4d840-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d840-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d840-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d840-140">Namespace</span></span><br/>                | <span data-ttu-id="4d840-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4d840-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4d840-142">標頭</span><span class="sxs-lookup"><span data-stu-id="4d840-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d840-143"><dt>Dbdao。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d840-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="4d840-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4d840-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d840-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4d840-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d840-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4d840-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d840-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d840-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4d840-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d840-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d840-149">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="4d840-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

