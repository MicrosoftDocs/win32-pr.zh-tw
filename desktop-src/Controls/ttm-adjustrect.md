---
title: 'TTM_ADJUSTRECT 訊息 (Commctrl .h) '
description: 從視窗矩形計算工具提示控制項的文字顯示矩形，或從顯示指定的文字顯示矩形所需的工具提示視窗矩形。
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934400"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="c8e78-104">TTM \_ ADJUSTRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="c8e78-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="c8e78-105">從視窗矩形計算工具提示控制項的文字顯示矩形，或從顯示指定的文字顯示矩形所需的工具提示視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="c8e78-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8e78-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8e78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e78-108">值，指定要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="c8e78-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="c8e78-109">若為 **TRUE**，則會使用 *lParam* 來指定文字顯示矩形，並接收對應的視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="c8e78-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="c8e78-110">如果為 **FALSE**，則會使用 *lParam* 來指定視窗矩形，並接收對應的文字顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="c8e78-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c8e78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8e78-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e78-112">**矩形** 結構，用來保存工具提示視窗矩形或文字顯示矩形。</span><span class="sxs-lookup"><span data-stu-id="c8e78-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e78-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8e78-113">Return value</span></span>

<span data-ttu-id="c8e78-114">如果已成功調整矩形，則傳回非零值，如果發生錯誤則傳回零。</span><span class="sxs-lookup"><span data-stu-id="c8e78-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e78-115">備註</span><span class="sxs-lookup"><span data-stu-id="c8e78-115">Remarks</span></span>

<span data-ttu-id="c8e78-116">當您想要使用工具提示控制項來顯示通常會截斷之字串的完整文字時，此訊息特別有用。</span><span class="sxs-lookup"><span data-stu-id="c8e78-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="c8e78-117">它通常會與 listview 和 treeview 控制項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c8e78-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="c8e78-118">您通常會傳送此訊息以回應 [TTN \_ 顯示](ttn-show.md) 通知程式碼，讓您可以正確定位工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="c8e78-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="c8e78-119">工具提示視窗矩形比用來限定工具提示字串的文字顯示矩形稍微大一點。</span><span class="sxs-lookup"><span data-stu-id="c8e78-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="c8e78-120">視窗原點也會從文字顯示矩形的原點位移和左邊。</span><span class="sxs-lookup"><span data-stu-id="c8e78-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="c8e78-121">若要定位文字顯示矩形，您必須計算對應的視窗矩形，然後使用該矩形來定位工具提示。</span><span class="sxs-lookup"><span data-stu-id="c8e78-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="c8e78-122">**TTM \_ADJUSTRECT** 會為您處理此計算。</span><span class="sxs-lookup"><span data-stu-id="c8e78-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="c8e78-123">如果您將 *wParam* 設為 **TRUE**， **TTM \_ ADJUSTRECT** 會採用所需工具提示文字顯示矩形的大小和位置，並傳回在指定的位置中顯示文字所需的工具提示視窗大小和位置。</span><span class="sxs-lookup"><span data-stu-id="c8e78-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="c8e78-124">如果您將 *wParam* 設定為 **FALSE**，您可以指定工具提示視窗矩形， **TTM \_ ADJUSTRECT** 將會傳回其文字矩形的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="c8e78-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="c8e78-125">下列程式碼片段說明如何使用 **TTM \_ ADJUSTRECT** 訊息來定位工具提示控制項，以顯示控制項字串的完整文字來取代截斷的字串。</span><span class="sxs-lookup"><span data-stu-id="c8e78-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="c8e78-126">應用程式定義的 **GetMyItemRect** 函式會傳回在截斷的字串上直接顯示工具提示文字所需的文字矩形。</span><span class="sxs-lookup"><span data-stu-id="c8e78-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="c8e78-127">如何執行此函式的詳細資料將取決於特定的控制項。</span><span class="sxs-lookup"><span data-stu-id="c8e78-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="c8e78-128">**TTM \_ADJUSTRECT** 用來將此文字矩形傳送至工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="c8e78-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="c8e78-129">它會傳回適當大小和定位的視窗矩形，然後用來定位工具提示視窗。</span><span class="sxs-lookup"><span data-stu-id="c8e78-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="c8e78-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8e78-130">Requirements</span></span>



| <span data-ttu-id="c8e78-131">需求</span><span class="sxs-lookup"><span data-stu-id="c8e78-131">Requirement</span></span> | <span data-ttu-id="c8e78-132">值</span><span class="sxs-lookup"><span data-stu-id="c8e78-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e78-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8e78-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e78-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8e78-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8e78-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8e78-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e78-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8e78-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8e78-137">標頭</span><span class="sxs-lookup"><span data-stu-id="c8e78-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8e78-138"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e78-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





