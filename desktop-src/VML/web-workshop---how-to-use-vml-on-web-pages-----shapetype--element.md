---
title: 使用 Shapetype 元素
description: 使用 Shapetype 元素
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- 網路研討會，shapetype 元素
- 設計網頁、shapetype 元素
- Vector Markup Language (VML) 、shapetype 元素
- VML (Vector Markup Language) ，shapetype 元素
- 向量圖形，shapetype 元素
- shapetype 元素
- VML 元素，shapetype
- VML 圖形，shapetype 元素
- Vector Markup Language (VML) ，定義經常使用的圖形
- 使用 VML (Vector Markup Language) ，定義常用的圖形
- 向量圖形，定義常用的圖形
- 定義經常使用的圖形
- 使用定義常用的 VML 圖形
- Vector Markup Language (VML) ，具現化圖形的複本
- VML (Vector Markup Language) ，具現化圖形的複本
- 向量圖形，具現化圖形的複本
- 將圖形的複本具現化
- VML 圖形，具現化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d815d9f5f911e1a34d558496881ae606819d328a501c635ff463a84f2926ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512643"
---
# <a name="using-the-shapetype-element"></a>使用 Shapetype 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明如何使用 `<shapetype>` 元素來定義您自己的常用圖形，然後從 shapetype 中具現化或建立圖形。

如果您想要繪製具有相同或類似屬性的許多圖形，如果您必須為每個圖形重複輸入相同的屬性屬性，就會很繁瑣。 VML 提供 `<shapetype>` 元素，讓您可以定義圖形的原型。 然後，您可以使用專案 `<shape>` ，從相同的 shapetype 具現化許多圖形複本。

您可以遵循下列三個步驟來定義 shapetype，然後從 shapetype 將圖形具現化：

1.  輸入 `<shapetype>` 元素，並指定 id 屬性來為它命名。
2.  使用屬性屬性或子項目來描述 shapetype。
3.  藉由輸入元素將圖形具現化 `<shape>` ，並將圖形的型別屬性（attribute）參考到 shapetype 的 id 屬性（attribute）。

例如，您輸入下列幾行來建立名為 "MyShape" 的 shapetype：


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



然後，您可以藉由設定某些屬性屬性來改變 shapetype，例如 `fillcolor="red" strokecolor="blue"` 。 或者，您可以使用 shapetype 內的子項目，例如， `<path>` `<fill>` `<stroke>` (我們將在稍後的主題中討論這些子項目) 。


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



然後，您可以藉由指定將圖形從 shapetype "MyShape" 具現化， `type="#MyShape"` 如下列 VML 標記法所示。 此圖形會繼承 shapetype "MyShape" 的所有屬性，並顯示在其包含的方塊中，大小為 100 80。


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



您可以藉由指定 `type="#MyShape"` 和覆寫某些屬性（例如 `fillcolor="maroon"` ，如下列 VML 標記法所示），從 Shapetype "MyShape" 具現化另一個圖形。 此圖形會繼承 shapetype "MyShape" 中的所有屬性（除了 fillcolor 屬性以外），並顯示在其包含的方塊中，大小為 70 90。


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



以下是上述範例的完整 VML 標記法：

![type1 \-1.gif (477 個位元組) ](images/type1-1.gif)![type1 \-2.gif (471 個位元組) ](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





如您所知，當圖形從 shapetype 具現化時，它會從 shapetype 繼承所有的屬性屬性。 您可以藉由重新定義元素內的屬性來覆寫部分或全部繼承的屬性 `<shape>` 。 請注意，繼承只是一個層級。 這是因為只有 `<shape>` 元素可以參考專案 `<shapetype>` 。 `<shapetype>`元素無法參考另一個專案 `<shapetype>` 。

此外，shapetype 不屬於任何群組。 因此，專案 `<shapetype>` 可以本身或元素內出現 `<group>` 。 您可以在不同的群組中有許多參考相同 shapetype 的圖形。 如果 shapetype 出現在群組內，則在另一個群組中生活的圖形仍可參考此 shapetype。

例如，在下列 VML 表示中，Rect1 和 Rect2 是在 GroupA 中，而 Rect3 則是在 GroupB 中。 這三個矩形都會從 MyShape shapetype 具現化。


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858387) 。

 

 