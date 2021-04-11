---
description: 將對應至視窗的文字複製到呼叫端所提供的緩衝區。
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: 'WM_GETTEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693856"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="2b248-103">WM \_ GETTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="2b248-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="2b248-104">將對應至視窗的文字複製到呼叫端所提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2b248-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="2b248-105">參數</span><span class="sxs-lookup"><span data-stu-id="2b248-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b248-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b248-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b248-107">要複製的字元數上限，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2b248-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="2b248-108">ANSI 應用程式可能會將緩衝區中的字串縮減 (為 *wParam* 值的最小值一半，) 因為從 ANSI 轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="2b248-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="2b248-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b248-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b248-110">要接收文字之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="2b248-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b248-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b248-111">Return value</span></span>

<span data-ttu-id="2b248-112">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2b248-112">Type: **LRESULT**</span></span>

<span data-ttu-id="2b248-113">傳回值是複製的字元數，不包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2b248-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b248-114">備註</span><span class="sxs-lookup"><span data-stu-id="2b248-114">Remarks</span></span>

<span data-ttu-id="2b248-115">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將與視窗相關聯的文字複製到指定的緩衝區，並傳回復制的字元數。</span><span class="sxs-lookup"><span data-stu-id="2b248-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="2b248-116">請注意，對於非文字靜態控制項，這會提供您原先建立控制項的文字，也就是 ID 編號。</span><span class="sxs-lookup"><span data-stu-id="2b248-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="2b248-117">不過，它會提供您原本建立之非文字靜態控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b248-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="2b248-118">也就是說，如果您之後使用了 **STM \_ SETIMAGE** 來變更它，仍會傳回原始識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b248-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="2b248-119">若為編輯控制項，要複製的文字是編輯控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="2b248-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="2b248-120">在下拉式方塊中，文字是編輯控制項的內容 (或下拉式方塊的靜態文字) 部分。</span><span class="sxs-lookup"><span data-stu-id="2b248-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="2b248-121">若為按鈕，文字就是按鈕名稱。</span><span class="sxs-lookup"><span data-stu-id="2b248-121">For a button, the text is the button name.</span></span> <span data-ttu-id="2b248-122">若為其他視窗，則文字為視窗標題。</span><span class="sxs-lookup"><span data-stu-id="2b248-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="2b248-123">若要在清單方塊中複製專案的文字，應用程式可以使用 [**LB \_ GETTEXT**](../controls/lb-gettext.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="2b248-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="2b248-124">將 **WM \_ GETTEXT** 訊息傳送至具有 **SS \_ 圖示** 樣式的靜態控制項時，會在 *lParam* 所指向之緩衝區的前四個位元組中傳回圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2b248-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="2b248-125">只有在使用 [**WM \_ SETTEXT**](wm-settext.md) 訊息來設定圖示時，才會發生此情況。</span><span class="sxs-lookup"><span data-stu-id="2b248-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="2b248-126">**Rich Edit：** 如果要複製的文字超過64K，請使用 [**em \_ STREAMOUT**](../controls/em-streamout.md) 或 [**em \_ GETSELTEXT**](../controls/em-getseltext.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="2b248-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="2b248-127">將 **WM \_ GETTEXT** 訊息傳送至非文字靜態控制項（例如靜態點陣圖或靜態圖示控制項）時，不會傳回字串值。</span><span class="sxs-lookup"><span data-stu-id="2b248-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="2b248-128">相反地，它會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2b248-128">Instead, it returns zero.</span></span> <span data-ttu-id="2b248-129">此外，在舊版的 Windows 中，應用程式可以將 **WM \_ GETTEXT** 訊息傳送至非文字靜態控制項，以取得控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b248-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="2b248-130">若要抓取控制項的識別碼，應用程式可以使用 [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)傳遞 **GWL \_ 識別碼** 作為索引值，或使用 **GWLP \_ 識別碼** 來 [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) 。</span><span class="sxs-lookup"><span data-stu-id="2b248-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b248-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b248-131">Requirements</span></span>



| <span data-ttu-id="2b248-132">需求</span><span class="sxs-lookup"><span data-stu-id="2b248-132">Requirement</span></span> | <span data-ttu-id="2b248-133">值</span><span class="sxs-lookup"><span data-stu-id="2b248-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b248-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b248-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2b248-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b248-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b248-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b248-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2b248-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b248-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b248-138">標頭</span><span class="sxs-lookup"><span data-stu-id="2b248-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b248-139"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2b248-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b248-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b248-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b248-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="2b248-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b248-142">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2b248-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2b248-143">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="2b248-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="2b248-144">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="2b248-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="2b248-145">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="2b248-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="2b248-146">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="2b248-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="2b248-147">**WM \_ GETTEXTLENGTH**</span><span class="sxs-lookup"><span data-stu-id="2b248-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="2b248-148">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="2b248-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="2b248-149">**概念**</span><span class="sxs-lookup"><span data-stu-id="2b248-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b248-150">Windows</span><span class="sxs-lookup"><span data-stu-id="2b248-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="2b248-151">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="2b248-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2b248-152">**EM \_ GETSELTEXT**</span><span class="sxs-lookup"><span data-stu-id="2b248-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="2b248-153">**EM \_ STREAMOUT**</span><span class="sxs-lookup"><span data-stu-id="2b248-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="2b248-154">**LB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="2b248-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 
