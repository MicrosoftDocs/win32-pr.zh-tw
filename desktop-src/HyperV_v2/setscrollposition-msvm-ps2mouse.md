---
description: 調整指標裝置之滾輪控制項的 z 座標。
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Msvm_Ps2Mouse 類別的 SetScrollPosition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850267"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="ffe4d-103">Msvm Ps2Mouse 類別的 SetScrollPosition 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ffe4d-103">SetScrollPosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="ffe4d-104">調整指標裝置之滾輪控制項的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-104">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="ffe4d-105">寫入這個屬性的值一律為相對座標位移。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe4d-106">語法</span><span class="sxs-lookup"><span data-stu-id="ffe4d-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="ffe4d-107">參數</span><span class="sxs-lookup"><span data-stu-id="ffe4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe4d-108">*scrollPositionDelta* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffe4d-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe4d-109">類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="ffe4d-109">Type: **sint8**</span></span>

<span data-ttu-id="ffe4d-110">捲軸位置的差異。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe4d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffe4d-111">Return value</span></span>

<span data-ttu-id="ffe4d-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ffe4d-112">Type: **uint32**</span></span>

<span data-ttu-id="ffe4d-113">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-113">A return value of zero indicates success.</span></span> <span data-ttu-id="ffe4d-114">非零值表示無法改變捲軸位置。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="ffe4d-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-123">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ffe4d-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="ffe4d-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ffe4d-128">備註</span><span class="sxs-lookup"><span data-stu-id="ffe4d-128">Remarks</span></span>

<span data-ttu-id="ffe4d-129">存取 [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ffe4d-130">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="ffe4d-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe4d-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffe4d-131">Requirements</span></span>



| <span data-ttu-id="ffe4d-132">需求</span><span class="sxs-lookup"><span data-stu-id="ffe4d-132">Requirement</span></span> | <span data-ttu-id="ffe4d-133">值</span><span class="sxs-lookup"><span data-stu-id="ffe4d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe4d-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffe4d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe4d-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffe4d-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ffe4d-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffe4d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe4d-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffe4d-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffe4d-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffe4d-138">Namespace</span></span><br/>                | <span data-ttu-id="ffe4d-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ffe4d-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ffe4d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ffe4d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffe4d-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffe4d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ffe4d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffe4d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffe4d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe4d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe4d-145">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="ffe4d-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

