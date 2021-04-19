---
title: 'SBM_SETSCROLLINFO 訊息 (Winuser .h) '
description: 傳送 SBM \_ SETSCROLLINFO 訊息來設定捲軸的參數。
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968188"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="fabb7-104">SBM \_ SETSCROLLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="fabb7-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="fabb7-105">傳送 **SBM \_ SETSCROLLINFO** 訊息來設定捲軸的參數。</span><span class="sxs-lookup"><span data-stu-id="fabb7-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="fabb7-106">應用程式不應直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fabb7-106">Applications should not send this message directly.</span></span> <span data-ttu-id="fabb7-107">相反地，它們應該使用 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="fabb7-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="fabb7-108">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="fabb7-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="fabb7-109">執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollInfo** 函數才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="fabb7-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="fabb7-110">參數</span><span class="sxs-lookup"><span data-stu-id="fabb7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fabb7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fabb7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fabb7-112">指定捲軸是否重繪，以反映新的捲動方塊位置。</span><span class="sxs-lookup"><span data-stu-id="fabb7-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="fabb7-113">如果此參數為 **TRUE**，則會重新繪製捲軸。</span><span class="sxs-lookup"><span data-stu-id="fabb7-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="fabb7-114">如果為 **FALSE**，則不會重新繪製捲軸。</span><span class="sxs-lookup"><span data-stu-id="fabb7-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="fabb7-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fabb7-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fabb7-116">[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fabb7-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="fabb7-117">在呼叫 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)之前，請將結構的 **cbSize** 成員設定為 **sizeof** (**SCROLLINFO**) 、設定 **fMask** 成員以指出要設定的參數，並在適當的成員中指定新的參數值。</span><span class="sxs-lookup"><span data-stu-id="fabb7-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="fabb7-118">**FMask** 成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="fabb7-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="fabb7-119">值</span><span class="sxs-lookup"><span data-stu-id="fabb7-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="fabb7-120">意義</span><span class="sxs-lookup"><span data-stu-id="fabb7-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="fabb7-121"><dt>**SIF \_ DISABLENOSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="fabb7-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="fabb7-122">除非捲軸的新參數使捲軸不是必要的，否則會停用捲軸，而不是移除它。</span><span class="sxs-lookup"><span data-stu-id="fabb7-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="fabb7-123"><dt>**SIF \_ 頁面**</dt></span><span class="sxs-lookup"><span data-stu-id="fabb7-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="fabb7-124">將滾動頁設定為 **nPage** 成員中指定的值。</span><span class="sxs-lookup"><span data-stu-id="fabb7-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="fabb7-125"><dt>**SIF \_ POS**</dt></span><span class="sxs-lookup"><span data-stu-id="fabb7-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="fabb7-126">將滾動位置設定為 **nPos** 成員中指定的值。</span><span class="sxs-lookup"><span data-stu-id="fabb7-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="fabb7-127"><dt>**SIF \_ 範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="fabb7-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="fabb7-128">將捲軸範圍設定為 **n 每天下限** 和 **n 上限** 成員中指定的值。</span><span class="sxs-lookup"><span data-stu-id="fabb7-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fabb7-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="fabb7-129">Return value</span></span>

<span data-ttu-id="fabb7-130">傳回值是捲動方塊的目前位置。</span><span class="sxs-lookup"><span data-stu-id="fabb7-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="fabb7-131">備註</span><span class="sxs-lookup"><span data-stu-id="fabb7-131">Remarks</span></span>

<span data-ttu-id="fabb7-132">表示捲軸位置、 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md)的訊息，只提供16個位的位置資料。</span><span class="sxs-lookup"><span data-stu-id="fabb7-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="fabb7-133">但是， [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)、 **SBM \_ SETSCROLLINFO**、 [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)和 [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)所使用的 [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構會提供32位的捲軸位置資料。</span><span class="sxs-lookup"><span data-stu-id="fabb7-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="fabb7-134">您可以在處理 **WM \_ HSCROLL** 或 **WM \_ VSCROLL** 訊息時使用這些訊息和函式，以取得32位捲軸位置資料。</span><span class="sxs-lookup"><span data-stu-id="fabb7-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fabb7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fabb7-135">Requirements</span></span>



| <span data-ttu-id="fabb7-136">需求</span><span class="sxs-lookup"><span data-stu-id="fabb7-136">Requirement</span></span> | <span data-ttu-id="fabb7-137">值</span><span class="sxs-lookup"><span data-stu-id="fabb7-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabb7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fabb7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fabb7-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fabb7-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fabb7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fabb7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fabb7-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fabb7-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fabb7-142">標頭</span><span class="sxs-lookup"><span data-stu-id="fabb7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fabb7-143"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fabb7-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fabb7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fabb7-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="fabb7-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="fabb7-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fabb7-146">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="fabb7-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="fabb7-147">**SBM \_ GETSCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="fabb7-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="fabb7-148">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="fabb7-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="fabb7-149">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="fabb7-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

