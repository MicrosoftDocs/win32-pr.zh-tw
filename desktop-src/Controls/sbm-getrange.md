---
title: 'SBM_GETRANGE 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETRANGE 訊息，以抓取捲軸控制項的最小和最大位置值。
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934788"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="a4aa5-104">SBM \_ GETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="a4aa5-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="a4aa5-105">傳送 **SBM \_ GETRANGE** 訊息，以抓取捲軸控制項的最小和最大位置值。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="a4aa5-106">應用程式不應直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-106">Applications should not send this message directly.</span></span> <span data-ttu-id="a4aa5-107">相反地，它們應該使用 [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) 函數。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="a4aa5-108">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="a4aa5-109">執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollRange** 函數才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4aa5-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4aa5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4aa5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4aa5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4aa5-112">接收最小滾動位置之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="a4aa5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4aa5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4aa5-114">接收最大滾動位置之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4aa5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4aa5-115">Return value</span></span>

<span data-ttu-id="a4aa5-116">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4aa5-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4aa5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4aa5-117">Requirements</span></span>



| <span data-ttu-id="a4aa5-118">需求</span><span class="sxs-lookup"><span data-stu-id="a4aa5-118">Requirement</span></span> | <span data-ttu-id="a4aa5-119">值</span><span class="sxs-lookup"><span data-stu-id="a4aa5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4aa5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4aa5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4aa5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4aa5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a4aa5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4aa5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4aa5-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4aa5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a4aa5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a4aa5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4aa5-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a4aa5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4aa5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4aa5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4aa5-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="a4aa5-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a4aa5-128">**SBM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="a4aa5-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="a4aa5-129">**SBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="a4aa5-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="a4aa5-130">**SBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="a4aa5-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="a4aa5-131">**SBM \_ SETRANGEREDRAW**</span><span class="sxs-lookup"><span data-stu-id="a4aa5-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

