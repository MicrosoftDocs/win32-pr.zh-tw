---
title: 'PGM_SETSCROLLINFO 訊息 (Commctrl .h) '
description: 設定分頁控制項的滾動參數，包括超時值、每個超時的行數，以及每行的圖元。 您可以明確地傳送此訊息，或使用 [呼叫器 \_ SetScrollInfo 宏]。
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843427"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="221fa-105">PGM \_ SETSCROLLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="221fa-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="221fa-106">\[適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="221fa-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="221fa-107">未來的 Windows 版本可能不支援此訊息。\]</span><span class="sxs-lookup"><span data-stu-id="221fa-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="221fa-108">設定分頁控制項的滾動參數，包括超時值、每個超時的行數，以及每行的圖元。</span><span class="sxs-lookup"><span data-stu-id="221fa-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="221fa-109">您可以明確地傳送此訊息，或使用 [ [**呼叫器 \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) 宏]。</span><span class="sxs-lookup"><span data-stu-id="221fa-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="221fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="221fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="221fa-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="221fa-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="221fa-112">指定捲軸之超時值的 **UINT** （以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="221fa-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="221fa-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="221fa-114">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是一種 **UINT** ，可指定每個 timeout 所要滾動的行數。</span><span class="sxs-lookup"><span data-stu-id="221fa-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="221fa-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是一種 **UINT** ，可指定每行的圖元數。</span><span class="sxs-lookup"><span data-stu-id="221fa-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="221fa-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="221fa-116">Return value</span></span>

<span data-ttu-id="221fa-117">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="221fa-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="221fa-118">安全性考量</span><span class="sxs-lookup"><span data-stu-id="221fa-118">Security Considerations</span></span>

<span data-ttu-id="221fa-119">使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="221fa-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="221fa-120">備註</span><span class="sxs-lookup"><span data-stu-id="221fa-120">Remarks</span></span>

<span data-ttu-id="221fa-121">*WParam* timeout 值會控制當控制項已捕捉到滑鼠輸入並按下滑鼠左鍵時，分頁控制項產生滾動事件的速率。</span><span class="sxs-lookup"><span data-stu-id="221fa-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="221fa-122">較小的值會導致滾動更快;較大的值會導致捲動速度較慢。</span><span class="sxs-lookup"><span data-stu-id="221fa-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="221fa-123">預設值為按兩下時間的一到八。</span><span class="sxs-lookup"><span data-stu-id="221fa-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="221fa-124">如需詳細資訊，請參閱 [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime)。</span><span class="sxs-lookup"><span data-stu-id="221fa-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="221fa-125">根據預設，每個滾動事件的分頁控制項會根據呼機控制項的水準或垂直方向，將等於控制項整體寬度或高度的金額滾動。</span><span class="sxs-lookup"><span data-stu-id="221fa-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="221fa-126">*LParam* 中的值可用來覆寫預設的滾動量。</span><span class="sxs-lookup"><span data-stu-id="221fa-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="221fa-127">如果未提供非零值，則滾動量就是兩個值的乘積 (LOWORD (*lParam*) \* HIWORD (*lParam*) ) 。</span><span class="sxs-lookup"><span data-stu-id="221fa-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="221fa-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="221fa-128">Requirements</span></span>



| <span data-ttu-id="221fa-129">需求</span><span class="sxs-lookup"><span data-stu-id="221fa-129">Requirement</span></span> | <span data-ttu-id="221fa-130">值</span><span class="sxs-lookup"><span data-stu-id="221fa-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="221fa-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="221fa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="221fa-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="221fa-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="221fa-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="221fa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="221fa-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="221fa-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="221fa-135">標頭</span><span class="sxs-lookup"><span data-stu-id="221fa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="221fa-136"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="221fa-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="221fa-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="221fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221fa-138">**呼機 \_ SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="221fa-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

