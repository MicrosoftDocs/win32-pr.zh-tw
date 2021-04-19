---
description: 以指定的水準和垂直差異來位移滑鼠指標的位置。
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Msvm_Ps2Mouse 類別的 SetRelativePosition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975768"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="46327-103">Msvm Ps2Mouse 類別的 SetRelativePosition 方法 \_</span><span class="sxs-lookup"><span data-stu-id="46327-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="46327-104">以指定的水準和垂直差異來位移滑鼠指標的位置。</span><span class="sxs-lookup"><span data-stu-id="46327-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="46327-105">語法</span><span class="sxs-lookup"><span data-stu-id="46327-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="46327-106">參數</span><span class="sxs-lookup"><span data-stu-id="46327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46327-107">*horizontalDelta* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46327-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46327-108">類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="46327-108">Type: **sint8**</span></span>

<span data-ttu-id="46327-109">滑鼠位置的水準變更（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="46327-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="46327-110">*verticalDelta* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46327-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46327-111">類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="46327-111">Type: **sint8**</span></span>

<span data-ttu-id="46327-112">滑鼠位置的垂直變更（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="46327-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46327-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="46327-113">Return value</span></span>

<span data-ttu-id="46327-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="46327-114">Type: **uint32**</span></span>

<span data-ttu-id="46327-115">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="46327-115">A return value of zero indicates success.</span></span> <span data-ttu-id="46327-116">非零值表示無法改變滑鼠位置。</span><span class="sxs-lookup"><span data-stu-id="46327-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="46327-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="46327-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46327-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="46327-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="46327-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="46327-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="46327-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="46327-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="46327-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="46327-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="46327-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="46327-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="46327-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="46327-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="46327-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="46327-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="46327-125">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="46327-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="46327-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="46327-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="46327-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="46327-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="46327-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="46327-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="46327-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="46327-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="46327-130">備註</span><span class="sxs-lookup"><span data-stu-id="46327-130">Remarks</span></span>

<span data-ttu-id="46327-131">存取 [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="46327-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="46327-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="46327-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="46327-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="46327-133">Requirements</span></span>



| <span data-ttu-id="46327-134">需求</span><span class="sxs-lookup"><span data-stu-id="46327-134">Requirement</span></span> | <span data-ttu-id="46327-135">值</span><span class="sxs-lookup"><span data-stu-id="46327-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46327-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46327-136">Minimum supported client</span></span><br/> | <span data-ttu-id="46327-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46327-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46327-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46327-138">Minimum supported server</span></span><br/> | <span data-ttu-id="46327-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46327-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46327-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="46327-140">Namespace</span></span><br/>                | <span data-ttu-id="46327-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="46327-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46327-142">MOF</span><span class="sxs-lookup"><span data-stu-id="46327-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46327-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="46327-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46327-144">DLL</span><span class="sxs-lookup"><span data-stu-id="46327-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46327-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46327-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46327-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46327-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46327-147">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="46327-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

