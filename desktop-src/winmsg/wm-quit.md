---
description: 表示終止應用程式的要求，並在應用程式呼叫 PostQuitMessage 函數時產生。 此訊息會使 GetMessage 函式傳回零。
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: 'WM_QUIT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026777"
---
# <a name="wm_quit-message"></a><span data-ttu-id="eade2-104">WM 結束 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="eade2-104">WM\_QUIT message</span></span>

<span data-ttu-id="eade2-105">表示終止應用程式的要求，並在應用程式呼叫 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 函數時產生。</span><span class="sxs-lookup"><span data-stu-id="eade2-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="eade2-106">此訊息會使 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 函式傳回零。</span><span class="sxs-lookup"><span data-stu-id="eade2-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="eade2-107">參數</span><span class="sxs-lookup"><span data-stu-id="eade2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eade2-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eade2-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eade2-109">[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)函式中提供的結束代碼。</span><span class="sxs-lookup"><span data-stu-id="eade2-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="eade2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eade2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eade2-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="eade2-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eade2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eade2-112">Return value</span></span>

<span data-ttu-id="eade2-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="eade2-113">Type: **LRESULT**</span></span>

<span data-ttu-id="eade2-114">此訊息沒有傳回值，因為它會在訊息傳送至應用程式的視窗程式之前，讓訊息迴圈結束。</span><span class="sxs-lookup"><span data-stu-id="eade2-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="eade2-115">備註</span><span class="sxs-lookup"><span data-stu-id="eade2-115">Remarks</span></span>

<span data-ttu-id="eade2-116">**WM 結束 \_** 訊息不會與視窗相關聯，因此永遠不會透過視窗的視窗程式來接收。</span><span class="sxs-lookup"><span data-stu-id="eade2-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="eade2-117">只有 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數才能抓取它。</span><span class="sxs-lookup"><span data-stu-id="eade2-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="eade2-118">請勿使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)函式張貼 **WM \_** 結束訊息; 請使用 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)。</span><span class="sxs-lookup"><span data-stu-id="eade2-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="eade2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="eade2-119">Requirements</span></span>



| <span data-ttu-id="eade2-120">需求</span><span class="sxs-lookup"><span data-stu-id="eade2-120">Requirement</span></span> | <span data-ttu-id="eade2-121">值</span><span class="sxs-lookup"><span data-stu-id="eade2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eade2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eade2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eade2-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eade2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eade2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eade2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eade2-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eade2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eade2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="eade2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eade2-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="eade2-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eade2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eade2-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="eade2-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="eade2-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eade2-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="eade2-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="eade2-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="eade2-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="eade2-132">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="eade2-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="eade2-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="eade2-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eade2-134">Windows</span><span class="sxs-lookup"><span data-stu-id="eade2-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
