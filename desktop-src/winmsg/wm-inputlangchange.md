---
description: 在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。 您應該進行任何應用程式專屬的設定，並將訊息傳遞至 DefWindowProc 函式，此函式會將訊息傳遞給所有的第一層子視窗。
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: 'WM_INPUTLANGCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112845"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="87f40-104">WM \_ INPUTLANGCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="87f40-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="87f40-105">在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。</span><span class="sxs-lookup"><span data-stu-id="87f40-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="87f40-106">您應該進行任何應用程式專屬的設定，並將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，此函式會將訊息傳遞給所有的第一層子視窗。</span><span class="sxs-lookup"><span data-stu-id="87f40-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="87f40-107">這些子視窗可以將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓它將訊息傳遞給其子視窗，依此類推。</span><span class="sxs-lookup"><span data-stu-id="87f40-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="87f40-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="87f40-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="87f40-109">參數</span><span class="sxs-lookup"><span data-stu-id="87f40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f40-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87f40-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f40-111">新地區設定的字元集。</span><span class="sxs-lookup"><span data-stu-id="87f40-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="87f40-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87f40-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f40-113">輸入地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="87f40-113">The input locale identifier.</span></span> <span data-ttu-id="87f40-114">如需詳細資訊，請參閱 [語言、地區設定和鍵盤配置](../inputdev/about-keyboard-input.md)。</span><span class="sxs-lookup"><span data-stu-id="87f40-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f40-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="87f40-115">Return value</span></span>

<span data-ttu-id="87f40-116">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="87f40-116">Type: **LRESULT**</span></span>

<span data-ttu-id="87f40-117">如果應用程式處理此訊息，則應該傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="87f40-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f40-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="87f40-118">Requirements</span></span>



| <span data-ttu-id="87f40-119">需求</span><span class="sxs-lookup"><span data-stu-id="87f40-119">Requirement</span></span> | <span data-ttu-id="87f40-120">值</span><span class="sxs-lookup"><span data-stu-id="87f40-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f40-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87f40-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87f40-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f40-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="87f40-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87f40-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87f40-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f40-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87f40-125">標頭</span><span class="sxs-lookup"><span data-stu-id="87f40-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f40-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="87f40-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f40-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87f40-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="87f40-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="87f40-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87f40-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="87f40-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="87f40-130">**WM \_ INPUTLANGCHANGEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="87f40-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="87f40-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="87f40-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87f40-132">Windows</span><span class="sxs-lookup"><span data-stu-id="87f40-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
