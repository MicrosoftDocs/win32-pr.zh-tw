---
title: 'CDN_SELCHANGE (Commdlg 的通知碼) '
description: 當清單方塊中顯示目前開啟的資料夾或目錄的內容時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊所傳送。
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a5c7aed47d02fb7c7fcf2232b144e7a99e7c46
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590751"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="2d3a8-104">CDN \_ SELCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="2d3a8-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="2d3a8-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="2d3a8-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="2d3a8-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="2d3a8-107">當清單方塊中顯示目前開啟的資料夾或目錄的內容時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊所傳送。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="2d3a8-108">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="2d3a8-109">參數</span><span class="sxs-lookup"><span data-stu-id="2d3a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3a8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d3a8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d3a8-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d3a8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d3a8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d3a8-113">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="2d3a8-114">**OFNOTIFY** 結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ SELCHANGE** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d3a8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d3a8-115">Return value</span></span>

<span data-ttu-id="2d3a8-116">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d3a8-117">備註</span><span class="sxs-lookup"><span data-stu-id="2d3a8-117">Remarks</span></span>

<span data-ttu-id="2d3a8-118">只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="2d3a8-119">若要取得新選取的檔案或資料夾的名稱，攔截程式可以將 [**CDM \_ GETFILEPATH**](cdm-getfilepath.md) 或 [**CDM \_ GETSPEC**](cdm-getspec.md) 訊息傳送至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3a8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d3a8-120">Requirements</span></span>



| <span data-ttu-id="2d3a8-121">需求</span><span class="sxs-lookup"><span data-stu-id="2d3a8-121">Requirement</span></span> | <span data-ttu-id="2d3a8-122">值</span><span class="sxs-lookup"><span data-stu-id="2d3a8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3a8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d3a8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3a8-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d3a8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2d3a8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d3a8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3a8-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d3a8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2d3a8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2d3a8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d3a8-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2d3a8-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d3a8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d3a8-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d3a8-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d3a8-131">**CDM \_ GETFILEPATH**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="2d3a8-132">**CDM \_ GETSPEC**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="2d3a8-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="2d3a8-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="2d3a8-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="2d3a8-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="2d3a8-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="2d3a8-137">**概念**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2d3a8-138">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="2d3a8-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

