---
title: 'MCIWNDM_REALIZE 訊息 (Vfw .h) '
description: MCIWNDM \_ 實現訊息會在 MCIWnd 視窗中瞭解 MCI 裝置目前所使用的調色板。 這個宏是使用 MCIWNDM 的實現訊息來定義的 \_ 。 您可以使用 MCIWndRealize 宏明確地傳送此訊息。
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933981"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="36036-106">MCIWNDM \_ 實現訊息</span><span class="sxs-lookup"><span data-stu-id="36036-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="36036-107">**MCIWNDM \_ 實現** 訊息會在 MCIWnd 視窗中瞭解 MCI 裝置目前所使用的調色板。</span><span class="sxs-lookup"><span data-stu-id="36036-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="36036-108">這個宏是使用 MCIWNDM 的 **\_ 實現** 訊息來定義的。</span><span class="sxs-lookup"><span data-stu-id="36036-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="36036-109">您可以使用 [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="36036-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="36036-110">參數</span><span class="sxs-lookup"><span data-stu-id="36036-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36036-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span><span class="sxs-lookup"><span data-stu-id="36036-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="36036-112">背景旗標。</span><span class="sxs-lookup"><span data-stu-id="36036-112">Background flag.</span></span> <span data-ttu-id="36036-113">如果視窗是背景應用程式，請為此參數指定 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="36036-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36036-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="36036-114">Return Value</span></span>

<span data-ttu-id="36036-115">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="36036-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36036-116">備註</span><span class="sxs-lookup"><span data-stu-id="36036-116">Remarks</span></span>

<span data-ttu-id="36036-117">**MCIWNDM \_**「請注意」會使用 MCI 裝置的選擇區，並呼叫 [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)函式。</span><span class="sxs-lookup"><span data-stu-id="36036-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="36036-118">如果您的應用程式明確處理 [**wm \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**wm \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 訊息，您應該在應用程式中使用此訊息，而不是使用 **RealizePalette**。</span><span class="sxs-lookup"><span data-stu-id="36036-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="36036-119">如果其中一個訊息處理常式的主體只包含 **RealizePalette**，則會將訊息轉寄至 MCIWnd 視窗，這將會自動實現調色板。</span><span class="sxs-lookup"><span data-stu-id="36036-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="36036-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="36036-120">Requirements</span></span>



| <span data-ttu-id="36036-121">需求</span><span class="sxs-lookup"><span data-stu-id="36036-121">Requirement</span></span> | <span data-ttu-id="36036-122">值</span><span class="sxs-lookup"><span data-stu-id="36036-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36036-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36036-123">Minimum supported client</span></span><br/> | <span data-ttu-id="36036-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36036-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="36036-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36036-125">Minimum supported server</span></span><br/> | <span data-ttu-id="36036-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36036-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36036-127">標頭</span><span class="sxs-lookup"><span data-stu-id="36036-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="36036-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="36036-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36036-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36036-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36036-130">**MCIWndRealize**</span><span class="sxs-lookup"><span data-stu-id="36036-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="36036-131">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="36036-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="36036-132">**WM \_ PALETTECHANGED**</span><span class="sxs-lookup"><span data-stu-id="36036-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="36036-133">**WM \_ QUERYNEWPALETTE**</span><span class="sxs-lookup"><span data-stu-id="36036-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

