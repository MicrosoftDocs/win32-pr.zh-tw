---
title: 如何執行 In-Place 工具提示
description: 就地工具提示是用來顯示已裁剪之物件的文字字串。 如需圖例，請參閱關於工具提示控制項。
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd3b01d30a20b52cbb80121cc8c1d793965acf0ea3cf4f2be1ce4553f4ccb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671724"
---
# <a name="how-to-implement-in-place-tooltips"></a>如何執行 In-Place 工具提示

就地工具提示是用來顯示已裁剪之物件的文字字串。 如需圖例，請參閱 [關於工具提示控制項](tooltip-controls.md)。

一般和就地工具提示的差異在於定位。 依預設，當滑鼠指標停留在具有相關工具提示的區域上方時，工具提示會顯示在區域旁邊。 不過，工具提示是 windows，而且可以藉由呼叫 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)，放置在您選擇的任何位置。 建立就地工具提示是放置工具提示視窗，使其覆迭文字字串。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>先決條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="positioning-an-in-place-tooltip"></a>定位 In-Place 工具提示

放置就地工具提示時，您需要追蹤三個矩形：

1.  圍繞完整標籤文字的矩形。
2.  圍繞工具提示文字的矩形。 工具提示文字與完整標籤文字相同，而且通常是相同的大小和字型。 這兩個文字矩形通常會是相同的大小。
3.  工具提示視窗矩形。 這個矩形比它所括住的工具提示文字矩形稍微大一點。


下圖顯示三個矩形架構上。 標籤文字的隱藏部分會以灰色背景表示。

![顯示長字串的圖表，其中一半具有灰色背景，然後是較大工具提示視窗矩形內的相同字串](images/inplace.png)

若要建立就地工具提示，您必須定位工具提示文字矩形，使其重迭標籤文字矩形。 將兩個矩形對齊的程式相當簡單：

1.  定義標籤文字矩形。
2.  定位工具提示視窗，讓工具提示文字矩形重迭標籤文字矩形。


在實務上，您通常已足以對齊兩個文字矩形的左上角。 嘗試調整工具提示文字矩形的大小，使其完全符合標籤文字矩形，可能會造成工具提示顯示的問題。

這個簡單的配置有個問題，就是您無法直接定位工具提示文字矩形。 相反地，您必須將 [工具提示視窗] 矩形放置在 [標籤文字] 矩形的上方和左邊，使兩個文字矩形的角落相符。 換句話說，您需要知道工具提示視窗矩形與其括住的文字矩形之間的位移。 一般來說，並沒有簡單的方法可以判斷這個位移。

### <a name="implement-in-place-tooltips"></a>執行工具提示 In-Place

下列程式碼片段說明如何在 [TTN \_ SHOW](ttn-show.md)處理常式中使用 [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)訊息，以顯示就地工具提示。 您的應用程式會將私用 *fMyStringIsTruncated* 變數設為 **TRUE**，以指出標籤文字已被截斷。 處理常式會呼叫應用程式定義函數 **GetMyItemRect**，以抓取標籤文字矩形。 這個矩形會以 **TTM \_ ADJUSTRECT** 傳遞給工具提示控制項，其會傳回對應的視窗矩形。 接著會呼叫 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) ，以將工具提示置於標籤上。


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



此範例不會變更工具提示的大小，只會變更其位置。 這兩個文字矩形會對齊其左上角，但不一定會有相同的維度。 在實務上，差別通常很小，而這種方法建議用於大部分的用途。 雖然您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 來調整大小並重新調整工具提示的位置，但是這樣做可能會產生無法預期的結果。

## <a name="remarks"></a>備註

通用控制項 [5.80 版](common-control-versions.md) 藉由新增新的訊息 [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)，簡化了就地工具提示的使用。 使用您希望工具提示重迭的標籤文字矩形座標來傳送此訊息，並傳回適當定位之工具提示視窗矩形的座標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

 