---
description: 在輸入法產生組合字元串作為按鍵結果前立即傳送。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: 'WM_IME_STARTCOMPOSITION 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848055"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="87ea4-104">WM \_ 輸入法 \_ STARTCOMPOSITION 訊息</span><span class="sxs-lookup"><span data-stu-id="87ea4-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="87ea4-105">在輸入法產生組合字元串作為按鍵結果前立即傳送。</span><span class="sxs-lookup"><span data-stu-id="87ea4-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="87ea4-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="87ea4-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="87ea4-107">參數</span><span class="sxs-lookup"><span data-stu-id="87ea4-107">Parameters</span></span>

<span data-ttu-id="87ea4-108">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="87ea4-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="87ea4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="87ea4-109">Return value</span></span>

<span data-ttu-id="87ea4-110">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="87ea4-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ea4-111">備註</span><span class="sxs-lookup"><span data-stu-id="87ea4-111">Remarks</span></span>

<span data-ttu-id="87ea4-112">這則訊息是 IME 視窗開啟其撰寫視窗的通知。</span><span class="sxs-lookup"><span data-stu-id="87ea4-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="87ea4-113">如果應用程式顯示覆合字元本身，就應該處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="87ea4-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="87ea4-114">如果應用程式已建立 IME 視窗，則應該將此訊息傳遞至該視窗。</span><span class="sxs-lookup"><span data-stu-id="87ea4-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="87ea4-115">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會藉由將訊息傳遞至預設 IME 視窗來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="87ea4-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ea4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="87ea4-116">Requirements</span></span>



| <span data-ttu-id="87ea4-117">需求</span><span class="sxs-lookup"><span data-stu-id="87ea4-117">Requirement</span></span> | <span data-ttu-id="87ea4-118">值</span><span class="sxs-lookup"><span data-stu-id="87ea4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ea4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87ea4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="87ea4-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87ea4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="87ea4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87ea4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="87ea4-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87ea4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87ea4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="87ea4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ea4-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="87ea4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ea4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87ea4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ea4-126">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="87ea4-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="87ea4-127">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="87ea4-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
