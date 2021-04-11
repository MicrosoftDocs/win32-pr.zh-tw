---
title: 'WM_NOTIFY 訊息 (Winuser .h) '
description: 當事件發生時，由通用控制項傳送至其父視窗，或控制項需要一些資訊。
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY message Windows 控制項
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934619"
---
# <a name="wm_notify-message"></a><span data-ttu-id="dee36-104">WM \_ 通知訊息</span><span class="sxs-lookup"><span data-stu-id="dee36-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="dee36-105">當事件發生時，由通用控制項傳送至其父視窗，或控制項需要一些資訊。</span><span class="sxs-lookup"><span data-stu-id="dee36-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="dee36-106">參數</span><span class="sxs-lookup"><span data-stu-id="dee36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee36-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dee36-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dee36-108">傳送訊息之通用控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dee36-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="dee36-109">此識別碼不保證是唯一的。</span><span class="sxs-lookup"><span data-stu-id="dee36-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="dee36-110">應用程式應該使用 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的 **hwndFrom** 或 **idFrom** 成員 (作為 *lParam* 參數傳遞，) 來識別控制項。</span><span class="sxs-lookup"><span data-stu-id="dee36-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="dee36-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dee36-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dee36-112">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="dee36-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="dee36-113">針對某些通知訊息，這個參數會指向較大的結構，此結構的 **NMHDR** 結構是其第一個成員。</span><span class="sxs-lookup"><span data-stu-id="dee36-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee36-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="dee36-114">Return value</span></span>

<span data-ttu-id="dee36-115">除非另有指定的通知訊息，否則會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="dee36-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee36-116">備註</span><span class="sxs-lookup"><span data-stu-id="dee36-116">Remarks</span></span>

<span data-ttu-id="dee36-117">訊息的目的地必須是控制項父系的 **HWND** 。</span><span class="sxs-lookup"><span data-stu-id="dee36-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="dee36-118">您可以使用 [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent)來取得此值，如下列範例所示，其中 *m \_ controlHwnd* 是控制項本身的 **HWND** 。</span><span class="sxs-lookup"><span data-stu-id="dee36-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="dee36-119">應用程式會在父視窗的視窗程式中處理訊息，如下列範例所示，這會處理上述範例中的自訂控制項所傳送的通知訊息。</span><span class="sxs-lookup"><span data-stu-id="dee36-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="dee36-120">某些通知會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送，CHIEFLY 已在 API 中的那些通知。</span><span class="sxs-lookup"><span data-stu-id="dee36-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="dee36-121">如需詳細資訊，請參閱 [控制訊息](control-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="dee36-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="dee36-122">如果訊息處理常式是在對話方塊程式中，您必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 來設定傳回值。</span><span class="sxs-lookup"><span data-stu-id="dee36-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="dee36-123">若為 Windows Vista 和更新版本的系統，則無法在進程間傳送 **WM \_ 通知** 訊息。</span><span class="sxs-lookup"><span data-stu-id="dee36-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="dee36-124">許多通知都有提供 ANSI 和 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="dee36-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="dee36-125">傳送 **wm \_ 通知** 訊息的視窗會使用 [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) 訊息來判斷應該使用哪一種格式。</span><span class="sxs-lookup"><span data-stu-id="dee36-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="dee36-126">如需進一步討論，請參閱 **WM \_ NOTIFYFORMAT** 。</span><span class="sxs-lookup"><span data-stu-id="dee36-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee36-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="dee36-127">Requirements</span></span>



| <span data-ttu-id="dee36-128">需求</span><span class="sxs-lookup"><span data-stu-id="dee36-128">Requirement</span></span> | <span data-ttu-id="dee36-129">值</span><span class="sxs-lookup"><span data-stu-id="dee36-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dee36-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dee36-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dee36-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee36-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dee36-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dee36-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dee36-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee36-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dee36-134">標頭</span><span class="sxs-lookup"><span data-stu-id="dee36-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee36-135"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="dee36-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee36-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dee36-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee36-137">**WM \_ NOTIFYFORMAT**</span><span class="sxs-lookup"><span data-stu-id="dee36-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

