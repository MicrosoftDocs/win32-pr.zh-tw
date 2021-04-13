---
title: 'CDN_TYPECHANGE (Commdlg 的通知碼) '
description: 當使用者從 [檔案類型] 下拉式方塊中選取新的檔案類型時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送。
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465280"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="85f27-104">CDN \_ TYPECHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="85f27-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="85f27-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="85f27-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="85f27-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="85f27-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="85f27-107">當使用者從 [檔案類型] 下拉式方塊中選取新的檔案類型時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="85f27-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="85f27-108">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="85f27-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="85f27-109">參數</span><span class="sxs-lookup"><span data-stu-id="85f27-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f27-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85f27-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85f27-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="85f27-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85f27-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85f27-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85f27-113">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="85f27-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="85f27-114">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ TYPECHANGE** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="85f27-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="85f27-115">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構也包含 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標，其 **nFilterIndex** 成員表示新選取之檔案類型篩選準則的單一索引。</span><span class="sxs-lookup"><span data-stu-id="85f27-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f27-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="85f27-116">Return value</span></span>

<span data-ttu-id="85f27-117">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="85f27-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85f27-118">備註</span><span class="sxs-lookup"><span data-stu-id="85f27-118">Remarks</span></span>

<span data-ttu-id="85f27-119">只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="85f27-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f27-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="85f27-120">Requirements</span></span>



| <span data-ttu-id="85f27-121">需求</span><span class="sxs-lookup"><span data-stu-id="85f27-121">Requirement</span></span> | <span data-ttu-id="85f27-122">值</span><span class="sxs-lookup"><span data-stu-id="85f27-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f27-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85f27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="85f27-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85f27-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="85f27-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85f27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="85f27-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85f27-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85f27-127">標頭</span><span class="sxs-lookup"><span data-stu-id="85f27-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="85f27-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="85f27-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85f27-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85f27-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="85f27-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="85f27-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="85f27-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="85f27-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="85f27-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="85f27-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="85f27-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="85f27-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="85f27-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="85f27-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="85f27-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="85f27-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="85f27-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="85f27-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="85f27-137">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="85f27-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

