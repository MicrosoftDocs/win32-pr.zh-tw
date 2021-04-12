---
title: 'WM_PSD_PAGESETUPDLG 訊息 (Commdlg .h) '
description: 通知 PagePaintHook 勾點程式，[版面設定] 對話方塊即將繪製範例頁面的內容。 攔截程式可以使用此訊息來執行與繪製範例頁面內容相關的初始化工作。
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- WM_PSD_PAGESETUPDLG 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385210"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="048de-105">WM \_ PSD \_ PAGESETUPDLG 訊息</span><span class="sxs-lookup"><span data-stu-id="048de-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="048de-106">通知 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點程式，[版面 **設定** ] 對話方塊即將繪製範例頁面的內容。</span><span class="sxs-lookup"><span data-stu-id="048de-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="048de-107">攔截程式可以使用此訊息來執行與繪製範例頁面內容相關的初始化工作。</span><span class="sxs-lookup"><span data-stu-id="048de-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="048de-108">參數</span><span class="sxs-lookup"><span data-stu-id="048de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="048de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="048de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="048de-110">低序位字組指定指出紙張大小的值。</span><span class="sxs-lookup"><span data-stu-id="048de-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="048de-111">這個值可以是結構描述中所列的其中一個 **DMPAPER \_** 值。</span><span class="sxs-lookup"><span data-stu-id="048de-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="048de-112">高序位單字指定紙張或信封的方向，以及印表機是否為點矩陣或 HPPCL (Hewlett Packard 印表機控制語言) 裝置。</span><span class="sxs-lookup"><span data-stu-id="048de-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="048de-113">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="048de-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="048de-114">值</span><span class="sxs-lookup"><span data-stu-id="048de-114">Value</span></span>                                                                             | <span data-ttu-id="048de-115">意義</span><span class="sxs-lookup"><span data-stu-id="048de-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="048de-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="048de-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="048de-117">橫向模式的紙張 (點矩陣) </span><span class="sxs-lookup"><span data-stu-id="048de-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="048de-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="048de-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="048de-119">橫向模式的紙張 (HPPCL) </span><span class="sxs-lookup"><span data-stu-id="048de-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="048de-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="048de-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="048de-121">直向模式的紙張 (點矩陣) </span><span class="sxs-lookup"><span data-stu-id="048de-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="048de-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="048de-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="048de-123">直向模式的紙張 (HPPCL) </span><span class="sxs-lookup"><span data-stu-id="048de-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="048de-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="048de-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="048de-125">橫向模式的信封 (HPPCL) </span><span class="sxs-lookup"><span data-stu-id="048de-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="048de-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="048de-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="048de-127">直向模式的信封 (點矩陣) </span><span class="sxs-lookup"><span data-stu-id="048de-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="048de-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="048de-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="048de-129">以橫向模式 (點矩陣) 的信封</span><span class="sxs-lookup"><span data-stu-id="048de-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="048de-130"><dt>0x001f</dt></span><span class="sxs-lookup"><span data-stu-id="048de-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="048de-131">直向模式的信封 (HPPCL) </span><span class="sxs-lookup"><span data-stu-id="048de-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="048de-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="048de-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="048de-133">[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構的指標，其中包含用來初始化 [版面 **設定**] 對話方塊的資訊。</span><span class="sxs-lookup"><span data-stu-id="048de-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="048de-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="048de-134">Return value</span></span>

<span data-ttu-id="048de-135">如果攔截程式傳回 **TRUE**，對話方塊將不再傳送任何訊息，而且在下一次系統需要重新繪製範例頁面之前，不會在範例頁面中繪製。</span><span class="sxs-lookup"><span data-stu-id="048de-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="048de-136">如果攔截程式傳回 **FALSE**，對話方塊會傳送繪圖順序的其餘訊息。</span><span class="sxs-lookup"><span data-stu-id="048de-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="048de-137">備註</span><span class="sxs-lookup"><span data-stu-id="048de-137">Remarks</span></span>

<span data-ttu-id="048de-138">[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。</span><span class="sxs-lookup"><span data-stu-id="048de-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="048de-139">當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。</span><span class="sxs-lookup"><span data-stu-id="048de-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="048de-140">每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。</span><span class="sxs-lookup"><span data-stu-id="048de-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="048de-141">繪圖順序的前三個訊息 (**wm \_ psd \_ PAGESETUPDLG**、 [**wm \_ psd \_ FULLPAGERECT**](wm-psd-fullpagerect.md)或 [**WM \_ psd \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) 提供攔截程式可用來繪製範例頁面內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="048de-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="048de-142">其餘訊息 ([**wm \_ psd \_ MARGINRECT**](wm-psd-marginrect.md)、 [**wm \_ psd \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)、 [**wm \_ psd \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)、 [**wm \_ psd \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) 通知攔截程式，指出對話方塊即將繪製範例頁面的特定部分。</span><span class="sxs-lookup"><span data-stu-id="048de-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="048de-143">這可讓攔截程式選擇性地繪製範例頁面的部分。</span><span class="sxs-lookup"><span data-stu-id="048de-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="048de-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="048de-144">Requirements</span></span>



| <span data-ttu-id="048de-145">需求</span><span class="sxs-lookup"><span data-stu-id="048de-145">Requirement</span></span> | <span data-ttu-id="048de-146">值</span><span class="sxs-lookup"><span data-stu-id="048de-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="048de-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="048de-147">Minimum supported client</span></span><br/> | <span data-ttu-id="048de-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="048de-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="048de-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="048de-149">Minimum supported server</span></span><br/> | <span data-ttu-id="048de-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="048de-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="048de-151">標頭</span><span class="sxs-lookup"><span data-stu-id="048de-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="048de-152"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="048de-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="048de-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="048de-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="048de-154">**參考**</span><span class="sxs-lookup"><span data-stu-id="048de-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="048de-155">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="048de-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="048de-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="048de-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="048de-157">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="048de-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="048de-158">**WM \_ PSD \_ ENVSTAMPRECT**</span><span class="sxs-lookup"><span data-stu-id="048de-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="048de-159">**WM \_ PSD \_ FULLPAGERECT**</span><span class="sxs-lookup"><span data-stu-id="048de-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="048de-160">**WM \_ PSD \_ GREEKTEXTRECT**</span><span class="sxs-lookup"><span data-stu-id="048de-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="048de-161">**WM \_ PSD \_ MARGINRECT**</span><span class="sxs-lookup"><span data-stu-id="048de-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="048de-162">**WM \_ PSD \_ MINMARGINRECT**</span><span class="sxs-lookup"><span data-stu-id="048de-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="048de-163">**WM \_ PSD \_ YAFULLPAGERECT**</span><span class="sxs-lookup"><span data-stu-id="048de-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="048de-164">**概念**</span><span class="sxs-lookup"><span data-stu-id="048de-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="048de-165">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="048de-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

