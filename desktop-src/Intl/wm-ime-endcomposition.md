---
description: 當 IME 結束組合時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: 'WM_IME_ENDCOMPOSITION 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318428"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="3dc60-104">WM \_ 輸入法 \_ ENDCOMPOSITION 訊息</span><span class="sxs-lookup"><span data-stu-id="3dc60-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="3dc60-105">當 IME 結束組合時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="3dc60-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="3dc60-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="3dc60-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="3dc60-107">參數</span><span class="sxs-lookup"><span data-stu-id="3dc60-107">Parameters</span></span>

<span data-ttu-id="3dc60-108">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3dc60-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="3dc60-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dc60-109">Return value</span></span>

<span data-ttu-id="3dc60-110">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="3dc60-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc60-111">備註</span><span class="sxs-lookup"><span data-stu-id="3dc60-111">Remarks</span></span>

<span data-ttu-id="3dc60-112">如果應用程式顯示覆合字元本身，就應該處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="3dc60-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="3dc60-113">如果應用程式已建立 IME 視窗，則應該將此訊息傳遞至該視窗。</span><span class="sxs-lookup"><span data-stu-id="3dc60-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="3dc60-114">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將此訊息傳遞至預設的 IME 視窗來進行處理。</span><span class="sxs-lookup"><span data-stu-id="3dc60-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc60-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dc60-115">Requirements</span></span>



| <span data-ttu-id="3dc60-116">需求</span><span class="sxs-lookup"><span data-stu-id="3dc60-116">Requirement</span></span> | <span data-ttu-id="3dc60-117">值</span><span class="sxs-lookup"><span data-stu-id="3dc60-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc60-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3dc60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc60-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dc60-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3dc60-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3dc60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc60-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dc60-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3dc60-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3dc60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dc60-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3dc60-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc60-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dc60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc60-125">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="3dc60-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="3dc60-126">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="3dc60-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
