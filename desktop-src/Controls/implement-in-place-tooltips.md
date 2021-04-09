---
title: 如何執行 In-Place 工具提示
description: 就地工具提示是用來顯示已裁剪之物件的文字字串。 如需圖例，請參閱關於工具提示控制項。
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024354"
---
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="d9672-104">如何執行 In-Place 工具提示</span><span class="sxs-lookup"><span data-stu-id="d9672-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="d9672-105">就地工具提示是用來顯示已裁剪之物件的文字字串。</span><span class="sxs-lookup"><span data-stu-id="d9672-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="d9672-106">如需圖例，請參閱 [關於工具提示控制項](tooltip-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="d9672-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="d9672-107">一般和就地工具提示的差異在於定位。</span><span class="sxs-lookup"><span data-stu-id="d9672-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="d9672-108">依預設，當滑鼠指標停留在具有相關工具提示的區域上方時，工具提示會顯示在區域旁邊。</span><span class="sxs-lookup"><span data-stu-id="d9672-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="d9672-109">不過，工具提示是 windows，而且可以藉由呼叫 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)，放置在您選擇的任何位置。</span><span class="sxs-lookup"><span data-stu-id="d9672-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="d9672-110">建立就地工具提示是放置工具提示視窗，使其覆迭文字字串。</span><span class="sxs-lookup"><span data-stu-id="d9672-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d9672-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d9672-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d9672-112">技術</span><span class="sxs-lookup"><span data-stu-id="d9672-112">Technologies</span></span>

-   [<span data-ttu-id="d9672-113">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d9672-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d9672-114">必要條件</span><span class="sxs-lookup"><span data-stu-id="d9672-114">Prerequisites</span></span>

-   <span data-ttu-id="d9672-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="d9672-115">C/C++</span></span>
-   <span data-ttu-id="d9672-116">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d9672-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d9672-117">指示</span><span class="sxs-lookup"><span data-stu-id="d9672-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="d9672-118">定位 In-Place 工具提示</span><span class="sxs-lookup"><span data-stu-id="d9672-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="d9672-119">放置就地工具提示時，您需要追蹤三個矩形：</span><span class="sxs-lookup"><span data-stu-id="d9672-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="d9672-120">圍繞完整標籤文字的矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="d9672-121">圍繞工具提示文字的矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="d9672-122">工具提示文字與完整標籤文字相同，而且通常是相同的大小和字型。</span><span class="sxs-lookup"><span data-stu-id="d9672-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="d9672-123">這兩個文字矩形通常會是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="d9672-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="d9672-124">工具提示視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-124">The tooltip window rectangle.</span></span> <span data-ttu-id="d9672-125">這個矩形比它所括住的工具提示文字矩形稍微大一點。</span><span class="sxs-lookup"><span data-stu-id="d9672-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="d9672-126">下圖顯示三個矩形架構上。</span><span class="sxs-lookup"><span data-stu-id="d9672-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="d9672-127">標籤文字的隱藏部分會以灰色背景表示。</span><span class="sxs-lookup"><span data-stu-id="d9672-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![顯示長字串的圖表，其中一半具有灰色背景，然後是較大工具提示視窗矩形內的相同字串](images/inplace.png)

<span data-ttu-id="d9672-129">若要建立就地工具提示，您必須定位工具提示文字矩形，使其重迭標籤文字矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="d9672-130">將兩個矩形對齊的程式相當簡單：</span><span class="sxs-lookup"><span data-stu-id="d9672-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="d9672-131">定義標籤文字矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="d9672-132">定位工具提示視窗，讓工具提示文字矩形重迭標籤文字矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="d9672-133">在實務上，您通常已足以對齊兩個文字矩形的左上角。</span><span class="sxs-lookup"><span data-stu-id="d9672-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="d9672-134">嘗試調整工具提示文字矩形的大小，使其完全符合標籤文字矩形，可能會造成工具提示顯示的問題。</span><span class="sxs-lookup"><span data-stu-id="d9672-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="d9672-135">這個簡單的配置有個問題，就是您無法直接定位工具提示文字矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="d9672-136">相反地，您必須將 [工具提示視窗] 矩形放置在 [標籤文字] 矩形的上方和左邊，使兩個文字矩形的角落相符。</span><span class="sxs-lookup"><span data-stu-id="d9672-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="d9672-137">換句話說，您需要知道工具提示視窗矩形與其括住的文字矩形之間的位移。</span><span class="sxs-lookup"><span data-stu-id="d9672-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="d9672-138">一般來說，並沒有簡單的方法可以判斷這個位移。</span><span class="sxs-lookup"><span data-stu-id="d9672-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="d9672-139">執行工具提示 In-Place</span><span class="sxs-lookup"><span data-stu-id="d9672-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="d9672-140">下列程式碼片段說明如何在 [TTN \_ SHOW](ttn-show.md)處理常式中使用 [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)訊息，以顯示就地工具提示。</span><span class="sxs-lookup"><span data-stu-id="d9672-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="d9672-141">您的應用程式會將私用 *fMyStringIsTruncated* 變數設為 **TRUE**，以指出標籤文字已被截斷。</span><span class="sxs-lookup"><span data-stu-id="d9672-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="d9672-142">處理常式會呼叫應用程式定義函數 **GetMyItemRect**，以抓取標籤文字矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="d9672-143">這個矩形會以 **TTM \_ ADJUSTRECT** 傳遞給工具提示控制項，其會傳回對應的視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="d9672-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="d9672-144">接著會呼叫 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) ，以將工具提示置於標籤上。</span><span class="sxs-lookup"><span data-stu-id="d9672-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



<span data-ttu-id="d9672-145">此範例不會變更工具提示的大小，只會變更其位置。</span><span class="sxs-lookup"><span data-stu-id="d9672-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="d9672-146">這兩個文字矩形會對齊其左上角，但不一定會有相同的維度。</span><span class="sxs-lookup"><span data-stu-id="d9672-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="d9672-147">在實務上，差別通常很小，而這種方法建議用於大部分的用途。</span><span class="sxs-lookup"><span data-stu-id="d9672-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="d9672-148">雖然您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 來調整大小並重新調整工具提示的位置，但是這樣做可能會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="d9672-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9672-149">備註</span><span class="sxs-lookup"><span data-stu-id="d9672-149">Remarks</span></span>

<span data-ttu-id="d9672-150">通用控制項 [5.80 版](common-control-versions.md) 藉由新增新的訊息 [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)，簡化了就地工具提示的使用。</span><span class="sxs-lookup"><span data-stu-id="d9672-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="d9672-151">使用您希望工具提示重迭的標籤文字矩形座標來傳送此訊息，並傳回適當定位之工具提示視窗矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="d9672-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9672-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9672-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9672-153">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="d9672-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 