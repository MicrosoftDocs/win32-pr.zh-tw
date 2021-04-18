---
title: 'SBM_GETSCROLLINFO 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETSCROLLINFO 訊息以抓取捲軸的參數。
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965950"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="36cbf-104">SBM \_ GETSCROLLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="36cbf-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="36cbf-105">傳送 **SBM \_ GETSCROLLINFO** 訊息以抓取捲軸的參數。</span><span class="sxs-lookup"><span data-stu-id="36cbf-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="36cbf-106">應用程式不應直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="36cbf-106">Applications should not send this message directly.</span></span> <span data-ttu-id="36cbf-107">相反地，它們應該使用 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="36cbf-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="36cbf-108">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="36cbf-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="36cbf-109">執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollInfo** 函數才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="36cbf-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="36cbf-110">參數</span><span class="sxs-lookup"><span data-stu-id="36cbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cbf-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36cbf-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cbf-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="36cbf-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36cbf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36cbf-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cbf-114">[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="36cbf-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="36cbf-115">在呼叫 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)之前，請將結構的 **cbSize** 成員設定為 **sizeof** (**SCROLLINFO**) ，並設定 **fMask** 成員以指定要取出的捲軸參數。</span><span class="sxs-lookup"><span data-stu-id="36cbf-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="36cbf-116">在傳回之前，訊息會將指定的參數複製到結構的適當成員。</span><span class="sxs-lookup"><span data-stu-id="36cbf-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="36cbf-117">**FMask** 成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="36cbf-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="36cbf-118">值</span><span class="sxs-lookup"><span data-stu-id="36cbf-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="36cbf-119">意義</span><span class="sxs-lookup"><span data-stu-id="36cbf-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="36cbf-120"><dt>**SIF \_ 全部**</dt></span><span class="sxs-lookup"><span data-stu-id="36cbf-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="36cbf-121">SIF \_ 頁面、sif \_ POS、sif \_ 範圍和 sif TRACKPOS 的組合 \_ 。</span><span class="sxs-lookup"><span data-stu-id="36cbf-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="36cbf-122"><dt>**SIF \_ 頁面**</dt></span><span class="sxs-lookup"><span data-stu-id="36cbf-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="36cbf-123">將滾動頁複製到 nPage 成員。</span><span class="sxs-lookup"><span data-stu-id="36cbf-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="36cbf-124"><dt>**SIF \_ POS**</dt></span><span class="sxs-lookup"><span data-stu-id="36cbf-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="36cbf-125">將滾動位置複製到 nPos 成員。</span><span class="sxs-lookup"><span data-stu-id="36cbf-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="36cbf-126"><dt>**SIF \_ 範圍**</dt></span><span class="sxs-lookup"><span data-stu-id="36cbf-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="36cbf-127">將捲軸範圍複製到 N 每天下限和 N 上限成員。</span><span class="sxs-lookup"><span data-stu-id="36cbf-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="36cbf-128"><dt>**SIF \_ TRACKPOS**</dt></span><span class="sxs-lookup"><span data-stu-id="36cbf-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="36cbf-129">將目前的捲動方塊追蹤位置複製到 nTrackPos 成員。</span><span class="sxs-lookup"><span data-stu-id="36cbf-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cbf-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="36cbf-130">Return value</span></span>

<span data-ttu-id="36cbf-131">如果訊息抓取任何值，則傳回值為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="36cbf-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="36cbf-132">備註</span><span class="sxs-lookup"><span data-stu-id="36cbf-132">Remarks</span></span>

<span data-ttu-id="36cbf-133">表示捲軸位置、 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**WM \_ VSCROLL**](wm-vscroll.md)的訊息，只提供16個位的位置資料。</span><span class="sxs-lookup"><span data-stu-id="36cbf-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="36cbf-134">但是， **SBM \_ GETSCROLLINFO**、 [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)、 [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)和 [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)所使用的 [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構會提供32位的捲軸位置資料。</span><span class="sxs-lookup"><span data-stu-id="36cbf-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="36cbf-135">您可以在處理 **WM \_ HSCROLL** 或 **WM \_ VSCROLL** 訊息時使用這些訊息和函式，以取得32位捲軸位置資料。</span><span class="sxs-lookup"><span data-stu-id="36cbf-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="36cbf-136">若要取得捲動方塊的32位位置 (\_ 在 [**WM \_ HSCROLL**](wm-hscroll.md)或 [**WM \_ VSCROLL**](wm-vscroll.md)訊息中的 SB THUMBTRACK 要求程式碼期間) ，請在 GETSCROLLINFO 結構的 TRACKPOS 成員中，傳送 **SBM \_ fMask** 與 SCROLLINFO \_ 成員中 [](/windows/win32/api/winuser/ns-winuser-scrollinfo)的 SI光圈值。 </span><span class="sxs-lookup"><span data-stu-id="36cbf-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="36cbf-137">訊息會傳回 **SCROLLINFO** 結構之 **nTrackPos** 成員中捲動方塊的追蹤位置。</span><span class="sxs-lookup"><span data-stu-id="36cbf-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="36cbf-138">這可讓您在使用者移動捲動方塊時取得捲動方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="36cbf-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="36cbf-139">或者，您可以使用 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) 函數來取得相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="36cbf-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cbf-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="36cbf-140">Requirements</span></span>



| <span data-ttu-id="36cbf-141">需求</span><span class="sxs-lookup"><span data-stu-id="36cbf-141">Requirement</span></span> | <span data-ttu-id="36cbf-142">值</span><span class="sxs-lookup"><span data-stu-id="36cbf-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36cbf-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36cbf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="36cbf-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cbf-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36cbf-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36cbf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="36cbf-146">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cbf-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36cbf-147">標頭</span><span class="sxs-lookup"><span data-stu-id="36cbf-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cbf-148"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="36cbf-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cbf-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36cbf-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="36cbf-150">**參考**</span><span class="sxs-lookup"><span data-stu-id="36cbf-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36cbf-151">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="36cbf-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="36cbf-152">**SBM \_ SETSCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="36cbf-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="36cbf-153">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="36cbf-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="36cbf-154">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="36cbf-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

