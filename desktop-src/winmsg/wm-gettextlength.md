---
description: 決定與視窗相關聯之文字的長度（以字元為單位）。
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: 'WM_GETTEXTLENGTH 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944667"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="bc367-103">WM \_ GETTEXTLENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="bc367-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="bc367-104">決定與視窗相關聯之文字的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc367-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="bc367-105">參數</span><span class="sxs-lookup"><span data-stu-id="bc367-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc367-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc367-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc367-107">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="bc367-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc367-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc367-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc367-109">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="bc367-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc367-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc367-110">Return value</span></span>

<span data-ttu-id="bc367-111">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc367-111">Type: **LRESULT**</span></span>

<span data-ttu-id="bc367-112">傳回值是文字的長度（以字元為單位），不包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="bc367-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc367-113">備註</span><span class="sxs-lookup"><span data-stu-id="bc367-113">Remarks</span></span>

<span data-ttu-id="bc367-114">若為編輯控制項，要複製的文字是編輯控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="bc367-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="bc367-115">在下拉式方塊中，文字是編輯控制項的內容 (或下拉式方塊的靜態文字) 部分。</span><span class="sxs-lookup"><span data-stu-id="bc367-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="bc367-116">若為按鈕，文字就是按鈕名稱。</span><span class="sxs-lookup"><span data-stu-id="bc367-116">For a button, the text is the button name.</span></span> <span data-ttu-id="bc367-117">若為其他視窗，則文字為視窗標題。</span><span class="sxs-lookup"><span data-stu-id="bc367-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="bc367-118">若要判斷清單方塊中專案的長度，應用程式可以使用 [**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bc367-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="bc367-119">傳送 **WM \_ GETTEXTLENGTH** 訊息時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會傳回文字的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc367-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="bc367-120">在某些條件下， **DefWindowProc** 函式會傳回大於文字實際長度的值。</span><span class="sxs-lookup"><span data-stu-id="bc367-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="bc367-121">這種情況會發生在 ANSI 和 Unicode 的特定混合中，而且是因為系統允許在文字內的 (DBCS) 字元中存在雙位元組字元集。</span><span class="sxs-lookup"><span data-stu-id="bc367-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="bc367-122">不過，傳回值一律會至少與文字的實際長度一樣大：因此，您可以一律使用它來引導緩衝區配置。</span><span class="sxs-lookup"><span data-stu-id="bc367-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="bc367-123">當應用程式同時使用 ANSI 函式和使用 Unicode 的通用對話時，就可能會發生這種行為。</span><span class="sxs-lookup"><span data-stu-id="bc367-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="bc367-124">若要取得文字的確切長度，請使用 [**WM \_ GETTEXT**](wm-gettext.md)、 [**LB \_ GETTEXT**](../controls/lb-gettext.md)或 [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) 訊息或 [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="bc367-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="bc367-125">將 **WM \_ GETTEXTLENGTH** 訊息傳送至非文字靜態控制項（例如靜態點陣圖或靜態圖示 controlc）並不會傳回字串值。</span><span class="sxs-lookup"><span data-stu-id="bc367-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="bc367-126">相反地，它會傳回零。</span><span class="sxs-lookup"><span data-stu-id="bc367-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc367-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc367-127">Requirements</span></span>



| <span data-ttu-id="bc367-128">需求</span><span class="sxs-lookup"><span data-stu-id="bc367-128">Requirement</span></span> | <span data-ttu-id="bc367-129">值</span><span class="sxs-lookup"><span data-stu-id="bc367-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc367-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc367-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bc367-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc367-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bc367-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc367-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bc367-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc367-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc367-134">標頭</span><span class="sxs-lookup"><span data-stu-id="bc367-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc367-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bc367-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc367-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc367-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc367-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="bc367-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc367-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bc367-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bc367-139">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="bc367-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="bc367-140">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="bc367-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="bc367-141">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="bc367-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="bc367-142">**概念**</span><span class="sxs-lookup"><span data-stu-id="bc367-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc367-143">Windows</span><span class="sxs-lookup"><span data-stu-id="bc367-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="bc367-144">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="bc367-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bc367-145">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="bc367-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="bc367-146">**LB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="bc367-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="bc367-147">**LB \_ GETTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="bc367-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
