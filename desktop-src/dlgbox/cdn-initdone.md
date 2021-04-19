---
title: 'CDN_INITDONE (Commdlg 的通知碼) '
description: 當系統完成對話方塊中的控制項排列時，由 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊傳送。 系統會移動標準控制項，以騰出空間給子對話方塊的控制項。
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE 通知碼對話方塊
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b07c25183eced86c3a430621091bed74c53f90d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590795"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="25844-105">CDN \_ INITDONE 通知碼</span><span class="sxs-lookup"><span data-stu-id="25844-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="25844-106">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="25844-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="25844-107">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="25844-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="25844-108">當系統完成對話方塊中的控制項排列時，由 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊傳送。</span><span class="sxs-lookup"><span data-stu-id="25844-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="25844-109">系統會移動標準控制項，以騰出空間給子對話方塊的控制項。</span><span class="sxs-lookup"><span data-stu-id="25844-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="25844-110">您的 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) 攔截程式會以 [**WM \_ 通知**](../controls/wm-notify.md) 訊息的形式接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="25844-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="25844-111">參數</span><span class="sxs-lookup"><span data-stu-id="25844-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25844-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25844-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25844-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="25844-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="25844-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25844-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25844-115">[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="25844-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="25844-116">**OFNOTIFY** 結構包含 [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr)結構，其程式 **代碼** 成員會指出 **CDN \_ INITDONE** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="25844-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25844-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="25844-117">Return value</span></span>

<span data-ttu-id="25844-118">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="25844-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="25844-119">備註</span><span class="sxs-lookup"><span data-stu-id="25844-119">Remarks</span></span>

<span data-ttu-id="25844-120">只有在使用 **OFN \_ EXPLORER** 值建立對話方塊時，系統才會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="25844-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="25844-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="25844-121">Requirements</span></span>



| <span data-ttu-id="25844-122">需求</span><span class="sxs-lookup"><span data-stu-id="25844-122">Requirement</span></span> | <span data-ttu-id="25844-123">值</span><span class="sxs-lookup"><span data-stu-id="25844-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25844-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25844-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25844-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25844-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="25844-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25844-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25844-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25844-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25844-128">標頭</span><span class="sxs-lookup"><span data-stu-id="25844-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="25844-129"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="25844-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25844-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25844-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="25844-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="25844-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="25844-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="25844-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="25844-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="25844-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="25844-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="25844-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="25844-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="25844-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="25844-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="25844-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="25844-137">**概念**</span><span class="sxs-lookup"><span data-stu-id="25844-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25844-138">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="25844-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

