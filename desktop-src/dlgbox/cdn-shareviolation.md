---
title: 'CDN_SHAREVIOLATION (Commdlg 的通知碼) '
description: 當使用者按一下 [確定] 按鈕時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送，表示選取的檔案發生網路共用違規。
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590695"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="50e30-104">CDN \_ SHAREVIOLATION 通知碼</span><span class="sxs-lookup"><span data-stu-id="50e30-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="50e30-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="50e30-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="50e30-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="50e30-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="50e30-107">當使用者按一下 [**確定]** 按鈕時，由 Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送，表示選取的檔案發生網路共用違規。</span><span class="sxs-lookup"><span data-stu-id="50e30-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="50e30-108">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="50e30-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="50e30-109">參數</span><span class="sxs-lookup"><span data-stu-id="50e30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e30-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50e30-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50e30-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="50e30-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="50e30-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50e30-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50e30-113">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="50e30-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="50e30-114">此結構的 **pszFile** 成員是具有共用違規的檔案名之指標。</span><span class="sxs-lookup"><span data-stu-id="50e30-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="50e30-115">**OFNOTIFY** 結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ SHAREVIOLATION** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="50e30-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e30-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="50e30-116">Return value</span></span>

<span data-ttu-id="50e30-117">傳回值會指出對話方塊應該如何處理共用違規。</span><span class="sxs-lookup"><span data-stu-id="50e30-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="50e30-118">如果攔截程式傳回零，對話方塊會顯示共用違規的標準警告訊息。</span><span class="sxs-lookup"><span data-stu-id="50e30-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="50e30-119">若要防止顯示標準警告訊息，請從攔截程式傳回非零的值，然後呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數來設定下列其中一個 **DWL \_ MSGRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="50e30-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="50e30-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="50e30-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="50e30-121">Description</span><span class="sxs-lookup"><span data-stu-id="50e30-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50e30-122"><dt>**OFN \_SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="50e30-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="50e30-123">讓對話方塊傳回檔案名，而不警告使用者共用違規。</span><span class="sxs-lookup"><span data-stu-id="50e30-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="50e30-124"><dt>**OFN \_SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="50e30-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="50e30-125">讓對話方塊拒絕檔案名，而不警告使用者共用違規。</span><span class="sxs-lookup"><span data-stu-id="50e30-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="50e30-126">備註</span><span class="sxs-lookup"><span data-stu-id="50e30-126">Remarks</span></span>

<span data-ttu-id="50e30-127">只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="50e30-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="50e30-128">只有在建立對話方塊時未指定 **OFN \_ SHAREAWARE** 值時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="50e30-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e30-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="50e30-129">Requirements</span></span>



| <span data-ttu-id="50e30-130">需求</span><span class="sxs-lookup"><span data-stu-id="50e30-130">Requirement</span></span> | <span data-ttu-id="50e30-131">值</span><span class="sxs-lookup"><span data-stu-id="50e30-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e30-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50e30-132">Minimum supported client</span></span><br/> | <span data-ttu-id="50e30-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50e30-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="50e30-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50e30-134">Minimum supported server</span></span><br/> | <span data-ttu-id="50e30-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50e30-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50e30-136">標頭</span><span class="sxs-lookup"><span data-stu-id="50e30-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e30-137"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="50e30-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e30-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50e30-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="50e30-139">**參考**</span><span class="sxs-lookup"><span data-stu-id="50e30-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="50e30-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="50e30-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="50e30-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="50e30-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="50e30-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="50e30-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="50e30-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="50e30-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="50e30-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="50e30-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="50e30-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="50e30-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="50e30-146">**概念**</span><span class="sxs-lookup"><span data-stu-id="50e30-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="50e30-147">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="50e30-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

