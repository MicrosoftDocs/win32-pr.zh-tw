---
title: 'CDN_HELP (Commdlg 的通知碼) '
description: 當使用者按一下 [說明] 按鈕時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送。
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- CDN_HELP 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105317"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="a7051-104">CDN 說明 \_ 通知碼</span><span class="sxs-lookup"><span data-stu-id="a7051-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="a7051-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a7051-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="a7051-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="a7051-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a7051-107">當使用者按一下 [說明 **] 按鈕時，由** Explorer 樣式的 [**開啟**] 或 [**另存** 新檔] 對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="a7051-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="a7051-108">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="a7051-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="a7051-109">參數</span><span class="sxs-lookup"><span data-stu-id="a7051-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7051-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7051-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7051-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="a7051-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7051-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7051-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7051-113">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a7051-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="a7051-114">**OFNOTIFY** 結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_** 說明通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a7051-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7051-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7051-115">Return value</span></span>

<span data-ttu-id="a7051-116">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a7051-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7051-117">備註</span><span class="sxs-lookup"><span data-stu-id="a7051-117">Remarks</span></span>

<span data-ttu-id="a7051-118">只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="a7051-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7051-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7051-119">Requirements</span></span>



| <span data-ttu-id="a7051-120">需求</span><span class="sxs-lookup"><span data-stu-id="a7051-120">Requirement</span></span> | <span data-ttu-id="a7051-121">值</span><span class="sxs-lookup"><span data-stu-id="a7051-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7051-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7051-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7051-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7051-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a7051-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7051-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7051-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7051-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7051-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a7051-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7051-127"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a7051-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7051-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7051-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7051-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="a7051-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7051-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="a7051-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="a7051-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="a7051-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="a7051-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="a7051-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="a7051-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="a7051-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="a7051-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="a7051-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="a7051-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="a7051-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7051-136">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="a7051-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

