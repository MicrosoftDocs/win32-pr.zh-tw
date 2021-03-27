---
description: WM \_ PALETTEISCHANGING 訊息會通知應用程式，應用程式會實現它的邏輯調色板。
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: 'WM_PALETTEISCHANGING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693892"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="9ab98-103">WM \_ PALETTEISCHANGING 訊息</span><span class="sxs-lookup"><span data-stu-id="9ab98-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="9ab98-104">**WM \_ PALETTEISCHANGING** 訊息會通知應用程式，應用程式會實現它的邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="9ab98-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="9ab98-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="9ab98-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="9ab98-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ab98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ab98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab98-108">即將實現其邏輯調色板的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="9ab98-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="9ab98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ab98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab98-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="9ab98-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab98-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ab98-111">Return value</span></span>

<span data-ttu-id="9ab98-112">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="9ab98-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab98-113">備註</span><span class="sxs-lookup"><span data-stu-id="9ab98-113">Remarks</span></span>

<span data-ttu-id="9ab98-114">變更其調色板的應用程式不會在變更選擇區和傳送 [**WM \_ PALETTECHANGED**](wm-palettechanged.md) 訊息之前等候此訊息的確認。</span><span class="sxs-lookup"><span data-stu-id="9ab98-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="9ab98-115">如此一來，當應用程式收到此訊息時，可能已經變更了此元件。</span><span class="sxs-lookup"><span data-stu-id="9ab98-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="9ab98-116">如果應用程式忽略或無法處理這個訊息，而第二個應用程式發現它的選擇區，而第一個應用程式使用的是選擇區索引，則在後續的繪圖作業期間，使用者可能會看到非預期的色彩。</span><span class="sxs-lookup"><span data-stu-id="9ab98-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab98-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ab98-117">Requirements</span></span>



| <span data-ttu-id="9ab98-118">需求</span><span class="sxs-lookup"><span data-stu-id="9ab98-118">Requirement</span></span> | <span data-ttu-id="9ab98-119">值</span><span class="sxs-lookup"><span data-stu-id="9ab98-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab98-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ab98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab98-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ab98-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ab98-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ab98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab98-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ab98-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ab98-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9ab98-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ab98-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9ab98-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab98-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ab98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab98-127">色彩總覽</span><span class="sxs-lookup"><span data-stu-id="9ab98-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="9ab98-128">色彩訊息</span><span class="sxs-lookup"><span data-stu-id="9ab98-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="9ab98-129">**WM \_ PALETTECHANGED**</span><span class="sxs-lookup"><span data-stu-id="9ab98-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="9ab98-130">**WM \_ QUERYNEWPALETTE**</span><span class="sxs-lookup"><span data-stu-id="9ab98-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
