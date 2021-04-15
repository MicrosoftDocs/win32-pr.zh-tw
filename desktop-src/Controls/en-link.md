---
title: 'EN_LINK (Richedit 的通知碼) '
description: 當 \_ 使用者按下滑鼠時，或當滑鼠指標停留在具有 CFE 連結效果的文字上方時，豐富的編輯控制項就會傳送連結通知碼給您 \_ 。
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466533"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="311a0-104">EN \_ 連結通知碼</span><span class="sxs-lookup"><span data-stu-id="311a0-104">EN\_LINK notification code</span></span>

<span data-ttu-id="311a0-105">當 \_ 使用者按下滑鼠時，或當滑鼠指標停留在具有 **CFE \_ 連結** 效果的文字上方時，豐富的編輯控制項就會傳送連結通知碼給您。</span><span class="sxs-lookup"><span data-stu-id="311a0-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="311a0-106">無視窗的 rich edit 控制項會使用 [**ITextHost：： TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) 方法傳送這個通知。</span><span class="sxs-lookup"><span data-stu-id="311a0-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="311a0-107">控制項的父視窗會透過 [**WM \_ 通知**](wm-notify.md) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="311a0-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="311a0-108">參數</span><span class="sxs-lookup"><span data-stu-id="311a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="311a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="311a0-110">藉由呼叫 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 函式與 GWL 識別碼值來抓取的視窗識別碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="311a0-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="311a0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="311a0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="311a0-112">[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="311a0-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="311a0-113">結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構、通知程式碼的相關資訊，以及 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構，指出具有 **CFE \_ 連結** 效果的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="311a0-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311a0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="311a0-114">Return value</span></span>

<span data-ttu-id="311a0-115">傳回零以允許控制項繼續正常處理訊息。</span><span class="sxs-lookup"><span data-stu-id="311a0-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="311a0-116">傳回非零值，以防止控制項處理訊息。</span><span class="sxs-lookup"><span data-stu-id="311a0-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="311a0-117">**Windows 8**： [傳回連結] 會 **\_ \_ \_ 預設** 為指示 rich edit 控制項執行預設動作。</span><span class="sxs-lookup"><span data-stu-id="311a0-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="311a0-118">備註</span><span class="sxs-lookup"><span data-stu-id="311a0-118">Remarks</span></span>

<span data-ttu-id="311a0-119">若要在連結具有焦點時接收 e **\_ 連結** 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ 連結**](rich-edit-control-event-mask-flags.md)旗標。</span><span class="sxs-lookup"><span data-stu-id="311a0-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="311a0-120">如果連結沒有焦點，則若要接收 **En-us \_ 連結** 通知碼，請在以 [**EM \_ SETEDITSTYLE**](em-seteditstyle.md)訊息傳送的遮罩中指定 **SES \_ NOFOCUSLINKNOTIFY** 旗標。</span><span class="sxs-lookup"><span data-stu-id="311a0-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="311a0-121">當滑鼠指標停留在具有 **CFE \_ 連結** 效果的文字上方時，rich edit 控制項會傳送以 **\_ 連結** 通知碼傳送的訊息：</span><span class="sxs-lookup"><span data-stu-id="311a0-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="311a0-122">**WM \_ LBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="311a0-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="311a0-123">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="311a0-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="311a0-124">**WM \_ LBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="311a0-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="311a0-125">**WM \_ MOUSEMOVE**</span><span class="sxs-lookup"><span data-stu-id="311a0-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="311a0-126">**WM \_ RBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="311a0-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="311a0-127">**WM \_ RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="311a0-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="311a0-128">**WM \_ RBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="311a0-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="311a0-129">**WM \_ SETCURSOR**</span><span class="sxs-lookup"><span data-stu-id="311a0-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="311a0-130">**CFE \_ 連結** 效果通常會識別包含 URL 的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="311a0-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="311a0-131">當應用程式在 \_ url 上方時變更滑鼠指標，或藉由啟動瀏覽器來查看 url 所識別的位置，應用程式可以處理 En-us 連結通知碼。</span><span class="sxs-lookup"><span data-stu-id="311a0-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="311a0-132">如果您傳送 [**EM \_ AUTOURLDETECT**](em-autourldetect.md) 訊息來啟用自動 URL 偵測，rich edit 控制項會自動為修改過的文字設定其識別為 url 的 **CFE \_ 連結** 效果。</span><span class="sxs-lookup"><span data-stu-id="311a0-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="311a0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="311a0-133">Requirements</span></span>



| <span data-ttu-id="311a0-134">需求</span><span class="sxs-lookup"><span data-stu-id="311a0-134">Requirement</span></span> | <span data-ttu-id="311a0-135">值</span><span class="sxs-lookup"><span data-stu-id="311a0-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="311a0-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="311a0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="311a0-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="311a0-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="311a0-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="311a0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="311a0-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="311a0-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="311a0-140">標頭</span><span class="sxs-lookup"><span data-stu-id="311a0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="311a0-141"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="311a0-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="311a0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="311a0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311a0-143">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="311a0-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="311a0-144">**EM \_ AUTOURLDETECT**</span><span class="sxs-lookup"><span data-stu-id="311a0-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="311a0-145">**ENLINK**</span><span class="sxs-lookup"><span data-stu-id="311a0-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="311a0-146">**ITextRange2：： SetURL**</span><span class="sxs-lookup"><span data-stu-id="311a0-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="311a0-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="311a0-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

