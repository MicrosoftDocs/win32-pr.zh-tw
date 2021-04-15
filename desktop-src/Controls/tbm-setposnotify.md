---
title: 'TBM_SETPOSNOTIFY 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的目前邏輯位置。
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464772"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="118f9-104">TBM \_ SETPOSNOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="118f9-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="118f9-105">設定捲軸中滑杆的目前邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="118f9-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="118f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="118f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="118f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="118f9-108">wParam 未使用。</span><span class="sxs-lookup"><span data-stu-id="118f9-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="118f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="118f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="118f9-110">滑杆的新邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="118f9-110">New logical position of the slider.</span></span> <span data-ttu-id="118f9-111">有效的邏輯位置是在最小至最大滑杆位置的最小值範圍中的整數值。</span><span class="sxs-lookup"><span data-stu-id="118f9-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="118f9-112">如果這個值超出控制項的最大和最小範圍，則會將位置設定為最大值或最小值。</span><span class="sxs-lookup"><span data-stu-id="118f9-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118f9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="118f9-113">Return value</span></span>

<span data-ttu-id="118f9-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="118f9-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="118f9-115">備註</span><span class="sxs-lookup"><span data-stu-id="118f9-115">Remarks</span></span>

<span data-ttu-id="118f9-116">呼叫 **TBM \_ SETPOSNOTIFY** 將會設定像 [**TBM \_ SETPOS**](tbm-setpos.md) 一樣的 [顯示] 滑杆位置，但它也會導致資訊提示透過 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息來通知其父系移動。</span><span class="sxs-lookup"><span data-stu-id="118f9-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="118f9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="118f9-117">Requirements</span></span>



| <span data-ttu-id="118f9-118">需求</span><span class="sxs-lookup"><span data-stu-id="118f9-118">Requirement</span></span> | <span data-ttu-id="118f9-119">值</span><span class="sxs-lookup"><span data-stu-id="118f9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="118f9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="118f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="118f9-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="118f9-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="118f9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="118f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="118f9-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="118f9-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="118f9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="118f9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="118f9-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="118f9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





