---
title: 使用 Handles 元素
description: 使用 Handles 元素
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- 網路研討會，控制碼元素
- 設計網頁、控制碼元素
- Vector Markup Language (VML) 、handles 元素
- VML (Vector Markup Language) ，handles 元素
- 向量圖形、handles 元素
- handles 元素
- VML 元素、控制碼
- VML 圖形、handles 元素
- Vector Markup Language (VML) ，將文字附加至圖形
- VML (Vector Markup Language) ，將文字附加至圖形
- 向量圖形，將文字附加至圖形
- VML 圖形，附加文字
- 將文字附加至圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023534"
---
# <a name="using-the-handles-element"></a>使用 Handles 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明如何使用 `<handles>` 元素將文字附加至圖形。

您可以將子專案放 `<handles>` 在或中， `<shape>` `<shapetype>` 以定義可以改變圖形上的 **形容詞** 值的使用者介面元素。

例如，如下列 VML 標記法所示，您可以 (黃色方塊提供調整控點) 使用者可以直接拖曳以調整形狀。

注意：在 Microsoft Office 應用程式中查看此 VML 圖形時，可使用這些控制碼，而圖形會 manipulable。

![shape1.gif (564 個位元組) ](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





請注意，前一個 VML 標記法和下列兩者之間唯一的差異是 **形容詞** 值。

![shape2.gif (1361 個位元組) ](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858393) 。

 

 