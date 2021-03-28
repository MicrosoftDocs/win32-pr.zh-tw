---
description: WM \_ QUERYNEWPALETTE 訊息會通知視窗，指出它即將接收鍵盤焦點，讓視窗有機會在收到焦點時，實現其邏輯調色板。
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: 'WM_QUERYNEWPALETTE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973049"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="978c1-103">WM \_ QUERYNEWPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="978c1-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="978c1-104">**WM \_ QUERYNEWPALETTE** 訊息會通知視窗，指出它即將接收鍵盤焦點，讓視窗有機會在收到焦點時，實現其邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="978c1-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="978c1-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="978c1-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="978c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="978c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="978c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="978c1-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="978c1-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="978c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="978c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="978c1-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="978c1-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978c1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="978c1-111">Return value</span></span>

<span data-ttu-id="978c1-112">如果視窗發現其邏輯元件，則必須傳回 **TRUE**;否則，它必須傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="978c1-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="978c1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="978c1-113">Requirements</span></span>



| <span data-ttu-id="978c1-114">需求</span><span class="sxs-lookup"><span data-stu-id="978c1-114">Requirement</span></span> | <span data-ttu-id="978c1-115">值</span><span class="sxs-lookup"><span data-stu-id="978c1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978c1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="978c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="978c1-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="978c1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="978c1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="978c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="978c1-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="978c1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="978c1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="978c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="978c1-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="978c1-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="978c1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="978c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978c1-123">色彩總覽</span><span class="sxs-lookup"><span data-stu-id="978c1-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="978c1-124">色彩訊息</span><span class="sxs-lookup"><span data-stu-id="978c1-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="978c1-125">**WM \_ PALETTECHANGED**</span><span class="sxs-lookup"><span data-stu-id="978c1-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="978c1-126">**WM \_ PALETTEISCHANGING**</span><span class="sxs-lookup"><span data-stu-id="978c1-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 
