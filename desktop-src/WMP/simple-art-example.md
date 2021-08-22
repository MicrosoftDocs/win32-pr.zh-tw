---
title: 簡易藝術範例
description: 簡易藝術範例
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player 的外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工圖案，範例
- Windows Media Player 的外觀範例
- 外觀，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbd50cb4ad0dbd76babd99439a885f9e77557d04e18f2698bb970effa23d6b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615923"
---
# <a name="simple-art-example"></a>簡易藝術範例

建立具有兩個按鈕的簡單面板時需要三個藝術檔案。 需要主要映射和對應影像，而替代映射則提供視覺提示給使用者，讓使用者可以按一下按鈕。

這些美工檔案是在使用圖層的尖端程式中所建立。 使用圖層可讓您更輕鬆地確保主要、對應和替代影像的大小都相同，並且彼此對齊。

有關建立藝術的詳細指示，請見面板 [建立指南](skin-creation-guide.md)。

## <a name="primary-image"></a>主要映像

主要影像是具有兩個按鈕的簡單黃色橢圓，Windows Media Player 的粉紅色和紫色按鈕來停止。 背景是稍微比橢圓稍微深一點的黃色。 下圖顯示此影像。

![主要映射](images/absam01b.png)

主要映射來自下列映射，每個映射位於不同的圖層。 第一個橢圓形是使用圖層斜面和浮凸效果所建立。 下圖顯示此影像。

![oval 影像](images/absam01s.png)

接著會建立兩個按鈕，以及圖層斜面和浮凸效果。 這會顯示在下圖中。

![兩個按鈕](images/absam01p.png)

接下來會建立影像背景。 選擇稍微較深的黃色，如此就不會注意到橢圓和背景之間的任何消除鋸齒。 色彩值為 \# CCCC00。 下圖顯示此影像。

![背景影像](images/absam01y.png)

包含這些影像的圖層會顯示出來，並儲存為點陣圖格式的複本，以建立主要映射。 **VIEW** 元素的 **backgroundImage** 屬性將使用主要複合影像。

## <a name="mapping-image"></a>對應影像

需要有對應影像，以指定按一下面板的時機和位置。 使用紅色區域和綠色區域建立地圖影像。 下圖顯示此影像。

![對應影像](images/absam01m.png)

綠色區域將用來識別面板上將開始 Windows Media Player 的區域，而紅色區域將用來停止。 對應影像的大小與主要映射相同。

地圖影像的建立方式是將按鈕圖層複製到新圖層，並關閉斜面和浮凸效果。 對應需要平面影像，因為 Windows Media Player 會在每個區域中尋找單一色彩值。 它只能搜尋您所定義的色彩，例如 (\# FF0000) 的紅色。 如果您的影像具有斜面或其他效果，則並非全部都是您所需的完全紅色。

為了讓對應按鈕具有簡單的色彩，影像以純紅色和純綠填滿，但可以使用任何色彩。 您必須記住地圖中的色彩，以便可以在 XML 面板定義檔中輸入這些數位。 在此情況下，紅色為 \# FF0000，綠色為 \# 00FF00。

然後，只要顯示新的圖層，影像就會儲存為 BMP 檔案的副本。 它會由 **BUTTONGROUP** 元素的 **mappingImage** 屬性呼叫。

## <a name="alternate-image"></a>替代映射

不需要替代的映射，但對使用者提供視覺提示非常有用。 在此情況下，建議使用暫留影像，讓使用者知道可以按一下的區域。

以兩個黃色按鈕建立替代映射。 這會顯示在下圖中。

![停留影像](images/absam01h.png)

建立替代影像的方式是將原始按鈕圖層複製到新圖層，然後將填滿色彩變更為黃色。 已保留斜面和浮凸效果。 接著會建立新的圖層並新增影像：箭號表示「播放」，而正方形表示「停止」。 然後，只要顯示新的黃色按鈕並輸入圖層，影像就會儲存為點陣圖檔案的副本。

結果就是當滑鼠停留在地圖影像所定義的區域上方時，將會顯示暫留影像，並在讀者按一下該位置時發出警示，提醒讀者，他們可以播放或停止 Windows Media Player。

## <a name="final-image"></a>最終影像

以下是外觀的最終影像。

![最終影像](images/absam01f.png)

如果您將滑鼠停留在右邊的粉紅色按鈕上方，就會看到這種影像。

![將滑鼠停留在右方按鈕上](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>藝術範例的 XML 程式碼

如需如何撰寫 XML 程式碼的詳細資料，請參閱面板 [建立指南](skin-creation-guide.md)，但為了顯示建立工作面板所需的程式碼，以下是此範例中的插圖程式碼。

預先定義的按鈕用於播放和停止功能。 您必須從 Windows 媒體錨點載入檔案或播放清單。 當 Windows Media Player 變更為面板模式時，螢幕右下角會出現一個小方塊。 此方塊稱為「錨點」。 按一下錨點可提供您所需的最小功能，以防面板無法返回 Windows Media Player 的完整模式。 使用者可以使用 [ **View** ] 功能表（如果處於完整模式），或是在面板模式下按一下錨點來切換模式。


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**美工檔案**](art-files.md)
</dt> </dl>

 

 




