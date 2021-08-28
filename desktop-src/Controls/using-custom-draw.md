---
title: 使用自訂繪圖
description: 本節包含示範如何執行自訂繪製的範例。
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90cff5fd4d692d31b69c85980f872f3aca4504cad81a3439d0c4d31a4c73d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655868"
---
# <a name="using-custom-draw"></a>使用自訂繪圖

本節包含示範如何執行自訂繪製的範例。

下列程式碼片段是 [**WM \_ 通知**](wm-notify.md) 處理常式的一部分，說明如何處理傳送至清單視圖控制項的自訂繪製通知。


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



第一個 [NM \_ CUSTOMDRAW](nm-customdraw.md)通知會將 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員設為 **CDDS \_ PREPAINT**。 處理常式會傳回 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) ，表示它想要個別修改一個或多個專案。

如果在上一個步驟中傳回 [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) ，則下一個 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知會將 **dwDrawStage** 設定為 **CDDS \_ ITEMPREPAINT**。 處理常式會抓取目前的色彩和字型值。 此時，您可以為小型圖示、大型圖示和清單模式指定新的值。 如果控制項處於報表模式，您也可以指定將套用至專案的所有子專案的新值。 如果您已變更任何變更，請傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)。 如果控制項在報表模式中，而且您想要個別處理子工作，則會傳回 **CDRF \_ NOTIFYSUBITEMDRAW**。

只有當控制項處於報表模式，且您在上一個步驟中傳回 **CDRF \_ NOTIFYSUBITEMDRAW** 時，才會傳送最後的通知。 變更字型和色彩的程式與該步驟相同，但只適用于單一子工作。 傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md) ，以在色彩或字型變更時通知控制項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[關於自訂繪圖](about-custom-draw.md)
</dt> <dt>

[自訂繪圖參考](custom-draw-reference.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[範例： CustDTv 說明 TreeView 中的自訂繪製 (Q248496) ](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




