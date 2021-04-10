---
title: 'CDN_INCLUDEITEM (Commdlg 的通知碼) '
description: 由 [開啟] 或 [另存新檔] 對話方塊傳送，以判斷對話方塊是否應在 shell 資料夾的專案清單中顯示專案。
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cbe830c644657425eb087dd64884da17a9a0c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686244"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="6dbae-104">CDN \_ INCLUDEITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="6dbae-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="6dbae-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6dbae-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="6dbae-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="6dbae-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6dbae-107">由 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送，以判斷對話方塊是否應在 shell 資料夾的專案清單中顯示專案。</span><span class="sxs-lookup"><span data-stu-id="6dbae-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="6dbae-108">當使用者開啟資料夾時，對話方塊會為資料夾中的每個專案傳送 **CDN \_ INCLUDEITEM** 通知。</span><span class="sxs-lookup"><span data-stu-id="6dbae-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="6dbae-109">只有在建立對話方塊時設定了 **OFN \_ ENABLEINCLUDENOTIFY** 旗標，對話方塊才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="6dbae-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="6dbae-110">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="6dbae-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="6dbae-111">參數</span><span class="sxs-lookup"><span data-stu-id="6dbae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dbae-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6dbae-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dbae-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="6dbae-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6dbae-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6dbae-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dbae-115">[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6dbae-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="6dbae-116">[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ INCLUDEITEM** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="6dbae-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="6dbae-117">[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)結構的 **.psf** 成員是要列舉其專案之資料夾的介面指標。</span><span class="sxs-lookup"><span data-stu-id="6dbae-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="6dbae-118">**Pidl** 成員是專案識別碼清單的指標，該清單會識別相對於資料夾的專案。</span><span class="sxs-lookup"><span data-stu-id="6dbae-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dbae-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6dbae-119">Return value</span></span>

<span data-ttu-id="6dbae-120">如果 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式傳回零，對話方塊就會從專案清單中排除專案。</span><span class="sxs-lookup"><span data-stu-id="6dbae-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="6dbae-121">若要包含專案，請從攔截程式傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6dbae-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dbae-122">備註</span><span class="sxs-lookup"><span data-stu-id="6dbae-122">Remarks</span></span>

<span data-ttu-id="6dbae-123">無論 **CDN \_ INCLUDEITEM** 傳回的值為何，對話方塊一律會包含同時具有 **SFGAO \_ FILESYSTEM** 和 **SFGAO \_ FILESYSANCESTOR** 屬性的專案。</span><span class="sxs-lookup"><span data-stu-id="6dbae-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dbae-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dbae-124">Requirements</span></span>



| <span data-ttu-id="6dbae-125">需求</span><span class="sxs-lookup"><span data-stu-id="6dbae-125">Requirement</span></span> | <span data-ttu-id="6dbae-126">值</span><span class="sxs-lookup"><span data-stu-id="6dbae-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dbae-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dbae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6dbae-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbae-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6dbae-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dbae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6dbae-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbae-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6dbae-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6dbae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dbae-132"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6dbae-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dbae-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dbae-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="6dbae-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="6dbae-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6dbae-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6dbae-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="6dbae-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="6dbae-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="6dbae-137">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="6dbae-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="6dbae-138">**OFNOTIFYEX**</span><span class="sxs-lookup"><span data-stu-id="6dbae-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="6dbae-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="6dbae-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6dbae-140">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="6dbae-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

