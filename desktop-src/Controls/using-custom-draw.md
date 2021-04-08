---
title: 使用自訂繪圖
description: 本節包含示範如何執行自訂繪製的範例。
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023100"
---
# <a name="using-custom-draw"></a><span data-ttu-id="85a2e-103">使用自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="85a2e-103">Using Custom Draw</span></span>

<span data-ttu-id="85a2e-104">本節包含示範如何執行自訂繪製的範例。</span><span class="sxs-lookup"><span data-stu-id="85a2e-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="85a2e-105">下列程式碼片段是 [**WM \_ 通知**](wm-notify.md) 處理常式的一部分，說明如何處理傳送至清單視圖控制項的自訂繪製通知。</span><span class="sxs-lookup"><span data-stu-id="85a2e-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



<span data-ttu-id="85a2e-106">第一個 [NM \_ CUSTOMDRAW](nm-customdraw.md)通知會將 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員設為 **CDDS \_ PREPAINT**。</span><span class="sxs-lookup"><span data-stu-id="85a2e-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="85a2e-107">處理常式會傳回 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) ，表示它想要個別修改一個或多個專案。</span><span class="sxs-lookup"><span data-stu-id="85a2e-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="85a2e-108">如果在上一個步驟中傳回 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) ，則下一個 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知會將 **dwDrawStage** 設定為 **CDDS \_ ITEMPREPAINT**。</span><span class="sxs-lookup"><span data-stu-id="85a2e-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="85a2e-109">處理常式會抓取目前的色彩和字型值。</span><span class="sxs-lookup"><span data-stu-id="85a2e-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="85a2e-110">此時，您可以為小型圖示、大型圖示和清單模式指定新的值。</span><span class="sxs-lookup"><span data-stu-id="85a2e-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="85a2e-111">如果控制項處於報表模式，您也可以指定將套用至專案的所有子專案的新值。</span><span class="sxs-lookup"><span data-stu-id="85a2e-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="85a2e-112">如果您已變更任何變更，請傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="85a2e-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="85a2e-113">如果控制項在報表模式中，而且您想要個別處理子工作，則會傳回 **CDRF \_ NOTIFYSUBITEMDRAW**。</span><span class="sxs-lookup"><span data-stu-id="85a2e-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="85a2e-114">只有當控制項處於報表模式，且您在上一個步驟中傳回 **CDRF \_ NOTIFYSUBITEMDRAW** 時，才會傳送最後的通知。</span><span class="sxs-lookup"><span data-stu-id="85a2e-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="85a2e-115">變更字型和色彩的程式與該步驟相同，但只適用于單一子工作。</span><span class="sxs-lookup"><span data-stu-id="85a2e-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="85a2e-116">傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md) ，以在色彩或字型變更時通知控制項。</span><span class="sxs-lookup"><span data-stu-id="85a2e-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85a2e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="85a2e-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="85a2e-118">**概念**</span><span class="sxs-lookup"><span data-stu-id="85a2e-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="85a2e-119">關於自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="85a2e-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="85a2e-120">自訂繪圖參考</span><span class="sxs-lookup"><span data-stu-id="85a2e-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="85a2e-121">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="85a2e-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="85a2e-122">範例： CustDTv 說明 TreeView 中的自訂繪製 (Q248496) </span><span class="sxs-lookup"><span data-stu-id="85a2e-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




