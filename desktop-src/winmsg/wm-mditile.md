---
description: 應用程式會將 WM \_ MDITILE 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以磚格式排列所有的 MDI 子視窗。
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: 'WM_MDITILE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191288"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="48eeb-103">WM \_ MDITILE 訊息</span><span class="sxs-lookup"><span data-stu-id="48eeb-103">WM\_MDITILE message</span></span>

<span data-ttu-id="48eeb-104">應用程式會將 **WM \_ MDITILE** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以磚格式排列所有的 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="48eeb-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="48eeb-105">參數</span><span class="sxs-lookup"><span data-stu-id="48eeb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48eeb-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48eeb-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48eeb-107">平鋪選項。</span><span class="sxs-lookup"><span data-stu-id="48eeb-107">The tiling option.</span></span> <span data-ttu-id="48eeb-108">這個參數可以是下列其中一個值，並選擇性地與 **MDITILE \_ SKIPDISABLED** 結合，以防止停用的 MDI 子視窗進行並排顯示。</span><span class="sxs-lookup"><span data-stu-id="48eeb-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="48eeb-109">值</span><span class="sxs-lookup"><span data-stu-id="48eeb-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="48eeb-110">意義</span><span class="sxs-lookup"><span data-stu-id="48eeb-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="48eeb-111"><dt>**MDITILE \_水準**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="48eeb-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="48eeb-112">水準磚視窗。</span><span class="sxs-lookup"><span data-stu-id="48eeb-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="48eeb-113"><dt>**MDITILE \_垂直**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="48eeb-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="48eeb-114">垂直磚視窗。</span><span class="sxs-lookup"><span data-stu-id="48eeb-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="48eeb-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48eeb-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48eeb-116">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="48eeb-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48eeb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="48eeb-117">Return value</span></span>

<span data-ttu-id="48eeb-118">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="48eeb-118">Type: **BOOL**</span></span>

<span data-ttu-id="48eeb-119">如果訊息成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="48eeb-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="48eeb-120">如果訊息失敗，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="48eeb-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="48eeb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="48eeb-121">Requirements</span></span>



| <span data-ttu-id="48eeb-122">需求</span><span class="sxs-lookup"><span data-stu-id="48eeb-122">Requirement</span></span> | <span data-ttu-id="48eeb-123">值</span><span class="sxs-lookup"><span data-stu-id="48eeb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48eeb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48eeb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="48eeb-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48eeb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="48eeb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48eeb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="48eeb-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48eeb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48eeb-128">標頭</span><span class="sxs-lookup"><span data-stu-id="48eeb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="48eeb-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="48eeb-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48eeb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48eeb-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="48eeb-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="48eeb-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="48eeb-132">**WM \_ MDICASCADE**</span><span class="sxs-lookup"><span data-stu-id="48eeb-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="48eeb-133">**WM \_ MDIICONARRANGE**</span><span class="sxs-lookup"><span data-stu-id="48eeb-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="48eeb-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="48eeb-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48eeb-135">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="48eeb-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




