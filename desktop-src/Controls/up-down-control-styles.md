---
title: 'Up-Down 控制項樣式 (CommCtrl .h) '
description: 本節列出建立上下控制項時所使用的樣式。
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b27cd27123f4c1a071314fd20d1874e61b590d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994782"
---
# <a name="up-down-control-styles"></a><span data-ttu-id="38322-103">Up-Down 控制項樣式</span><span class="sxs-lookup"><span data-stu-id="38322-103">Up-Down Control Styles</span></span>

<span data-ttu-id="38322-104">本節列出建立上下控制項時所使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="38322-104">This section lists the styles used when creating up-down controls.</span></span>



| <span data-ttu-id="38322-105">常數</span><span class="sxs-lookup"><span data-stu-id="38322-105">Constant</span></span>                                                                                                                                                            | <span data-ttu-id="38322-106">描述</span><span class="sxs-lookup"><span data-stu-id="38322-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <span data-ttu-id="38322-107"><dt>**UD \_ ALIGNLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-107"><dt>**UDS\_ALIGNLEFT**</dt></span></span> </dl>       | <span data-ttu-id="38322-108">將上下控制項放在好友視窗左邊緣的旁邊。</span><span class="sxs-lookup"><span data-stu-id="38322-108">Positions the up-down control next to the left edge of the buddy window.</span></span> <span data-ttu-id="38322-109">好友視窗會移至右邊，並減少其寬度以容納上下按鈕控制項的寬度。</span><span class="sxs-lookup"><span data-stu-id="38322-109">The buddy window is moved to the right, and its width is decreased to accommodate the width of the up-down control.</span></span><br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <span data-ttu-id="38322-110"><dt>**UD \_ ALIGNRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-110"><dt>**UDS\_ALIGNRIGHT**</dt></span></span> </dl>    | <span data-ttu-id="38322-111">在好友視窗的右邊緣旁邊放置上下控制項。</span><span class="sxs-lookup"><span data-stu-id="38322-111">Positions the up-down control next to the right edge of the buddy window.</span></span> <span data-ttu-id="38322-112">好友視窗的寬度會減少以容納上下按鈕控制項的寬度。</span><span class="sxs-lookup"><span data-stu-id="38322-112">The width of the buddy window is decreased to accommodate the width of the up-down control.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <span data-ttu-id="38322-113"><dt>**UD \_ ARROWKEYS**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-113"><dt>**UDS\_ARROWKEYS**</dt></span></span> </dl>       | <span data-ttu-id="38322-114">當按下向上鍵和向下鍵時，會讓下一個控制項遞增和遞減位置。</span><span class="sxs-lookup"><span data-stu-id="38322-114">Causes the up-down control to increment and decrement the position when the UP ARROW and DOWN ARROW keys are pressed.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <span data-ttu-id="38322-115"><dt>**UD \_ AUTOBUDDY**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-115"><dt>**UDS\_AUTOBUDDY**</dt></span></span> </dl>       | <span data-ttu-id="38322-116">以迭置順序自動選取前一個視窗，做為上下按鈕控制項的合作者視窗。</span><span class="sxs-lookup"><span data-stu-id="38322-116">Automatically selects the previous window in the z-order as the up-down control's buddy window.</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <span data-ttu-id="38322-117"><dt>**UD \_ HORZ**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-117"><dt>**UDS\_HORZ**</dt></span></span> </dl>                      | <span data-ttu-id="38322-118">讓上下按鈕控制項的箭號向左和向右指向，而不是向上和向下。</span><span class="sxs-lookup"><span data-stu-id="38322-118">Causes the up-down control's arrows to point left and right instead of up and down.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <span data-ttu-id="38322-119"><dt>**UD \_ HOTTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-119"><dt>**UDS\_HOTTRACK**</dt></span></span> </dl>          | <span data-ttu-id="38322-120">使控制項呈現「熱追蹤」行為。</span><span class="sxs-lookup"><span data-stu-id="38322-120">Causes the control to exhibit "hot tracking" behavior.</span></span> <span data-ttu-id="38322-121">也就是說，它會在指標通過時，反白顯示控制項上的向上箭號和向下箭號。</span><span class="sxs-lookup"><span data-stu-id="38322-121">That is, it highlights the UP ARROW and DOWN ARROW on the control as the pointer passes over them.</span></span> <span data-ttu-id="38322-122">此樣式需要 Windows 98 或 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="38322-122">This style requires Windows 98 or Windows 2000.</span></span> <span data-ttu-id="38322-123">如果系統正在執行 Windows 95 或 Windows NT 4.0，則會忽略旗標。</span><span class="sxs-lookup"><span data-stu-id="38322-123">If the system is running Windows 95 or Windows NT 4.0, the flag is ignored.</span></span> <span data-ttu-id="38322-124">若要檢查是否已啟用熱追蹤，請呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)。</span><span class="sxs-lookup"><span data-stu-id="38322-124">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <span data-ttu-id="38322-125"><dt>**UD \_ NOTHOUSANDS**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-125"><dt>**UDS\_NOTHOUSANDS**</dt></span></span> </dl> | <span data-ttu-id="38322-126">不會在每三個小數位數之間插入千位分隔符號。</span><span class="sxs-lookup"><span data-stu-id="38322-126">Does not insert a thousands separator between every three decimal digits.</span></span> <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <span data-ttu-id="38322-127"><dt>**UD \_ SETBUDDYINT**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-127"><dt>**UDS\_SETBUDDYINT**</dt></span></span> </dl> | <span data-ttu-id="38322-128">當位置變更時，會讓下一個控制項使用 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息) 來設定合作者視窗的文字 (。</span><span class="sxs-lookup"><span data-stu-id="38322-128">Causes the up-down control to set the text of the buddy window (using the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message) when the position changes.</span></span> <span data-ttu-id="38322-129">此文字包含格式化為十進位或十六進位字串的位置。</span><span class="sxs-lookup"><span data-stu-id="38322-129">The text consists of the position formatted as a decimal or hexadecimal string.</span></span><br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <span data-ttu-id="38322-130"><dt>**UD \_ 換行**</dt></span><span class="sxs-lookup"><span data-stu-id="38322-130"><dt>**UDS\_WRAP**</dt></span></span> </dl>                      | <span data-ttu-id="38322-131">如果遞增或減少超出範圍的結束或開頭，則會使位置「換行」。</span><span class="sxs-lookup"><span data-stu-id="38322-131">Causes the position to "wrap" if it is incremented or decremented beyond the ending or beginning of the range.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="38322-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="38322-132">Requirements</span></span>



| <span data-ttu-id="38322-133">需求</span><span class="sxs-lookup"><span data-stu-id="38322-133">Requirement</span></span> | <span data-ttu-id="38322-134">值</span><span class="sxs-lookup"><span data-stu-id="38322-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38322-135">標頭</span><span class="sxs-lookup"><span data-stu-id="38322-135">Header</span></span><br/> | <dl> <span data-ttu-id="38322-136"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="38322-136"><dt>CommCtrl.h</dt></span></span> </dl> |



 

