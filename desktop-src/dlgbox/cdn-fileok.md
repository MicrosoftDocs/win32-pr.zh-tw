---
title: 'CDN_FILEOK (Commdlg 的通知碼) '
description: 當使用者指定檔案名，並按一下 [確定] 按鈕時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送。
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- CDN_FILEOK 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968986"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="249d6-104">CDN \_ FILEOK 通知碼</span><span class="sxs-lookup"><span data-stu-id="249d6-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="249d6-105">當使用者指定檔案名，並按一下 [**確定**] 按鈕時，由 Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="249d6-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="249d6-106">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="249d6-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="249d6-107">參數</span><span class="sxs-lookup"><span data-stu-id="249d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="249d6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="249d6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="249d6-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="249d6-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="249d6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="249d6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="249d6-111">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="249d6-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="249d6-112">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ FILEOK** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="249d6-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="249d6-113">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構也包含 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標，其 **lpstrFile** 成員會指定所選檔案名的位址。</span><span class="sxs-lookup"><span data-stu-id="249d6-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="249d6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="249d6-114">Return value</span></span>

<span data-ttu-id="249d6-115">如果攔截程式傳回零，對話方塊會接受指定的檔案名並關閉。</span><span class="sxs-lookup"><span data-stu-id="249d6-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="249d6-116">若要拒絕指定的檔案名，並強制對話方塊保持開啟，請從攔截程式傳回非零值，並呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式來設定非零的 **DWL \_ MSGRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="249d6-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="249d6-117">備註</span><span class="sxs-lookup"><span data-stu-id="249d6-117">Remarks</span></span>

<span data-ttu-id="249d6-118">只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="249d6-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="249d6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="249d6-119">Requirements</span></span>



| <span data-ttu-id="249d6-120">需求</span><span class="sxs-lookup"><span data-stu-id="249d6-120">Requirement</span></span> | <span data-ttu-id="249d6-121">值</span><span class="sxs-lookup"><span data-stu-id="249d6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="249d6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="249d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="249d6-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="249d6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="249d6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="249d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="249d6-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="249d6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="249d6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="249d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="249d6-127"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="249d6-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="249d6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="249d6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="249d6-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="249d6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="249d6-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="249d6-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="249d6-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="249d6-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="249d6-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="249d6-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="249d6-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="249d6-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="249d6-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="249d6-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="249d6-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="249d6-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="249d6-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="249d6-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="249d6-137">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="249d6-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="249d6-138">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="249d6-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="249d6-139">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="249d6-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 

