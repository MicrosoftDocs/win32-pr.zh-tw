---
description: '\_當具有鍵盤焦點的視窗已實現其邏輯調色板，進而變更系統調色板時，會將 WM PALETTECHANGED 訊息傳送至所有最上層和重迭的視窗。'
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: 'WM_PALETTECHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692588"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="0f168-103">WM \_ PALETTECHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="0f168-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="0f168-104">當具有鍵盤焦點的視窗已實現其邏輯調色板，進而變更系統調色板時，會將 **WM \_ PALETTECHANGED** 訊息傳送至所有最上層和重迭的視窗。</span><span class="sxs-lookup"><span data-stu-id="0f168-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="0f168-105">此訊息可讓使用色彩選擇區但沒有鍵盤焦點的視窗實現其邏輯調色板，並更新其工作區。</span><span class="sxs-lookup"><span data-stu-id="0f168-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="0f168-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="0f168-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="0f168-107">參數</span><span class="sxs-lookup"><span data-stu-id="0f168-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f168-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f168-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f168-109">造成系統調色板變更的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="0f168-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="0f168-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f168-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f168-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="0f168-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f168-112">備註</span><span class="sxs-lookup"><span data-stu-id="0f168-112">Remarks</span></span>

<span data-ttu-id="0f168-113">此訊息必須傳送至所有最上層和重迭的視窗，包括變更系統調色板的視窗。</span><span class="sxs-lookup"><span data-stu-id="0f168-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="0f168-114">如果有任何子視窗使用調色板，則也必須將此訊息傳遞給它們。</span><span class="sxs-lookup"><span data-stu-id="0f168-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="0f168-115">若要避免建立無限迴圈，接收此訊息的視窗必須找不到其調色板，除非它判斷 *wParam* 不包含自己的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="0f168-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f168-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f168-116">Requirements</span></span>



| <span data-ttu-id="0f168-117">需求</span><span class="sxs-lookup"><span data-stu-id="0f168-117">Requirement</span></span> | <span data-ttu-id="0f168-118">值</span><span class="sxs-lookup"><span data-stu-id="0f168-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f168-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f168-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f168-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f168-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0f168-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f168-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f168-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f168-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f168-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0f168-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f168-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0f168-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f168-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f168-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f168-126">色彩總覽</span><span class="sxs-lookup"><span data-stu-id="0f168-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="0f168-127">色彩訊息</span><span class="sxs-lookup"><span data-stu-id="0f168-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="0f168-128">**WM \_ PALETTEISCHANGING**</span><span class="sxs-lookup"><span data-stu-id="0f168-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="0f168-129">**WM \_ QUERYNEWPALETTE**</span><span class="sxs-lookup"><span data-stu-id="0f168-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
