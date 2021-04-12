---
description: 不執行任何操作。 如果應用程式 \_ 想要張貼收件者視窗將忽略的訊息，則會傳送 WM Null 訊息。
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: 'WM_Null 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192787"
---
# <a name="wm_null-message"></a><span data-ttu-id="f515a-104">WM \_ Null 訊息</span><span class="sxs-lookup"><span data-stu-id="f515a-104">WM\_NULL message</span></span>

<span data-ttu-id="f515a-105">不執行任何操作。</span><span class="sxs-lookup"><span data-stu-id="f515a-105">Performs no operation.</span></span> <span data-ttu-id="f515a-106">如果應用程式想要張貼收件者視窗將忽略的訊息，則會傳送 **WM \_ Null** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f515a-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="f515a-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="f515a-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="f515a-108">參數</span><span class="sxs-lookup"><span data-stu-id="f515a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f515a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f515a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f515a-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="f515a-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f515a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f515a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f515a-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="f515a-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f515a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f515a-113">Return value</span></span>

<span data-ttu-id="f515a-114">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="f515a-114">Type: **LRESULT**</span></span>

<span data-ttu-id="f515a-115">如果應用程式處理此訊息，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f515a-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f515a-116">備註</span><span class="sxs-lookup"><span data-stu-id="f515a-116">Remarks</span></span>

<span data-ttu-id="f515a-117">例如，如果應用程式已安裝 **WH \_ GETMESSAGE** 勾點，而且想要防止處理訊息，則 [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) 回呼函式可以將訊息編號變更為 **WM \_ Null** ，讓收件者略過它。</span><span class="sxs-lookup"><span data-stu-id="f515a-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="f515a-118">另一個範例是，應用程式可以使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)函數傳送 **WM \_ Null** 訊息，以檢查視窗是否回應訊息。</span><span class="sxs-lookup"><span data-stu-id="f515a-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f515a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f515a-119">Requirements</span></span>



| <span data-ttu-id="f515a-120">需求</span><span class="sxs-lookup"><span data-stu-id="f515a-120">Requirement</span></span> | <span data-ttu-id="f515a-121">值</span><span class="sxs-lookup"><span data-stu-id="f515a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f515a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f515a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f515a-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f515a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f515a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f515a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f515a-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f515a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f515a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f515a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f515a-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f515a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f515a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f515a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f515a-129">Windows 總覽</span><span class="sxs-lookup"><span data-stu-id="f515a-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
