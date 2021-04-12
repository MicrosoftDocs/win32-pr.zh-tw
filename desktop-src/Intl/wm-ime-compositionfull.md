---
description: 當 IME 視窗找不到可延伸組合視窗區域的空間時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: 'WM_IME_COMPOSITIONFULL 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195427"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="16616-104">WM \_ 輸入法 \_ COMPOSITIONFULL 訊息</span><span class="sxs-lookup"><span data-stu-id="16616-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="16616-105">當 IME 視窗找不到可延伸組合視窗區域的空間時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="16616-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="16616-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="16616-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="16616-107">參數</span><span class="sxs-lookup"><span data-stu-id="16616-107">Parameters</span></span>

<span data-ttu-id="16616-108">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="16616-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="16616-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="16616-109">Return value</span></span>

<span data-ttu-id="16616-110">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="16616-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16616-111">備註</span><span class="sxs-lookup"><span data-stu-id="16616-111">Remarks</span></span>

<span data-ttu-id="16616-112">應用程式應該使用 [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) 命令指定視窗的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="16616-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="16616-113">IME 視窗（而不是 IME）會透過 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數傳送此通知訊息。</span><span class="sxs-lookup"><span data-stu-id="16616-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="16616-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="16616-114">Requirements</span></span>



| <span data-ttu-id="16616-115">需求</span><span class="sxs-lookup"><span data-stu-id="16616-115">Requirement</span></span> | <span data-ttu-id="16616-116">值</span><span class="sxs-lookup"><span data-stu-id="16616-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16616-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16616-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16616-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16616-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="16616-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16616-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16616-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16616-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16616-121">標頭</span><span class="sxs-lookup"><span data-stu-id="16616-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="16616-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="16616-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16616-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16616-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16616-124">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="16616-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="16616-125">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="16616-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="16616-126">IMC \_ SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="16616-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
