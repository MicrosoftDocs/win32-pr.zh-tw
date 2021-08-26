---
description: 在收集筆墨之後，應用程式可以管理、操作及/或將該資料傳輸到其他媒體。
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: 筆墨資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f62f566e48859ba2aea7013783b3ccc8c825b8559fdec34e24438d68b6ee65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939408"
---
# <a name="ink-data"></a>筆墨資料

在收集筆墨之後，應用程式可以管理、操作及/或將該資料傳輸到其他媒體。 選取、複製、移動、儲存、觀看及變更筆墨的動作會在 [**筆跡**](inkdisp-class.md) 物件和其包含的成員上進行，例如 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合和 [**筆劃**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。

> [!Note]  
> 使用 Real-Time 手寫筆，應用程式可以選擇以自己的格式維護資料， (例如儲存筆劃) 。

 

## <a name="ink-strokes-and-packets"></a>筆墨、筆劃和封包

[**筆墨**](inkdisp-class.md)物件是管理、操作和儲存從 [**InkCollector**](inkcollector-class.md)物件收集之輸入的基本資料類型。 **筆墨** 物件包含一個或多個 [**筆劃**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件，以及用來管理和操作這些筆觸的一般方法和屬性。 筆劃會定義為一組資料，而該資料集會在單一的向下筆、畫筆移動和畫筆序列中捕捉。 筆劃資料包含封包集合。 封包是一組 tablet 裝置在每個範例點傳送的資料。 此資料包含座標、畫筆壓力、畫筆角度，以及硬體可以傳輸的任何其他資訊。 **筆觸** 物件的 [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription)屬性描述 [**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)電腦產生的封包。

## <a name="strokes"></a>中風

您可以使用 **筆墨** 物件的 [[**筆觸**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes)] 屬性，取得 [**筆跡**](inkdisp-class.md)物件中筆劃的快照。 [**筆劃**] 屬性是在讀取 **筆觸** 屬性時 **筆跡** 物件中筆劃的參考集合。 如果後續在 **筆跡** 物件中新增或刪除筆劃，則不會更新先前取得的 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。 此外，[ **筆劃** ] 屬性是一個值，如同任何值，除非指派給變數，否則不會超出範圍。

若要讓 [**筆觸**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes)屬性與 [**Ink**](inkdisp-class.md)物件同步，請將其包裝在 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合上 [**StrokesAdded**](inkstrokes-strokesadded.md)和 [**StrokesRemoved**](inkstrokes-strokesremoved.md)事件的事件處理常式中。 引發任何事件時，處理常式應該取得 **筆劃** 屬性的新複本。 請小心不要將事件處理常式新增至在引發事件之前超出範圍的 **筆劃** 集合。

請注意，在此範例中， `theAddedStrokesIDs` 會在處理常式中使用新的筆觸屬性複本來更新 `StrokesAdded_Event` 。


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a>PacketDescription 屬性

[**筆墨**](inkdisp-class.md)物件的 [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription)屬性會定義每個封包中的一組資訊，應用程式會從 Tablet PC 裝置取得這些資訊。 這項資訊通常包含座標，但它可以包含更詳細的資訊 (根據 Tablet PC 數位板) 的功能，例如畫筆壓力或畫筆角度。 藉由在 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件上設定封包描述，再收集任何筆墨 (使用 DesiredPacketDescription 屬性) ，您可以完全控制要接收的 Tablet PC 裝置屬性。

## <a name="extended-properties"></a>擴充屬性

擴充屬性提供一種機制，可將應用程式定義的資料附加至 [**筆跡**](inkdisp-class.md) 和其他物件。 如需有關擴充屬性的詳細資訊，請參閱 [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) 集合。

## <a name="ink-rendering"></a>筆墨轉譯

轉譯 [**器物件負責**](inkrenderer-class.md) 呈現 [**筆墨**](inkdisp-class.md)。 由於有適當的 tablet 內容，轉譯 **器物件可以** 將筆墨空間座標組應到圖元、套用視圖轉換，以及在螢幕和印表機上顯示筆墨。 [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)和 [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)方法是用來呈現筆墨的主要方法。 如需在視窗中顯示筆墨的詳細資訊，請參閱轉譯 **器物件。**

## <a name="cusps"></a>Cusps

當畫筆降至繪圖介面時，通常會開始筆觸，並且在產生畫筆時結束。 在筆劃內，方向的尖峰、角度和根式變更稱為 cusps。 筆劃的端點也會被視為 cusps。 例如，大寫字母 "L" 有三個 cusps，一個在中間，一個在每一端。

輸入筆觸時，通常會使用貝塞爾 (或線條) 曲線，以平滑和呈現。 貝茲曲線可能會將 cusps 變成小迴圈。 例如，草書信件 "i" 的尖峰可能會平滑化，使其類似于草書 "e"。 為了避免這種情況，Microsoft 轉譯器有以不同方式處理 cusps 的「預先貝塞爾」階段。

Cusps 也可用來將 [**筆劃**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件細分為可讀寫單位。 例如，選取大寫 "L" 的垂直側邊可能表示只清除該端。 要清除之筆劃的部分將會是兩個 cusps 之間的部分。

 

 
