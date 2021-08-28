---
title: 使用公式元素
description: 使用公式元素
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web 研討會，公式元素
- 設計網頁、公式元素
- Vector Markup Language (VML) 、公式元素
- VML (Vector Markup Language) ，公式元素
- 向量圖形，公式元素
- 公式元素
- VML 元素，公式
- VML 圖形，公式元素
- Vector Markup Language (VML) ，定義圖形的路徑
- VML (Vector Markup Language) ，定義圖形的路徑
- 向量圖形，定義圖形的路徑
- VML 圖形，定義路徑
- 定義圖形的路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9db791533190cd2f67e1043e345954fe71de251
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885622"
---
# <a name="using-the-formulas-element"></a>使用公式元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明如何使用 `&lt;formulas&gt;` 子項目來定義圖形的可調整路徑。

您可以將 [ &lt; 公式] &gt; 子項目放在或中， `<shape>` `<shapetype>` 以定義可以改變圖形路徑的公式。 在 `&lt;formulas&gt;` 子項目內，一個 **f** 子項目會定義一個公式，因此會根據該公式來評估一個值。 例如，公式 `<v:f eqn="prod 10 4 5"/>` 會定義相當於 "10 x 4/5" 的值。

您可以在一個子項目內放置許多 **f** 子項目 `&lt;formulas&gt;` 。 公式可以參考先前在相同子項目內其他公式中定義的值 `&lt;formulas&gt;` 。 第一個公式中定義的值可以參考為 @0 ，第二個公式中定義的值可以稱為 @1 ，依此類推。

此外，您可以指定元素的 **[** 調整] 屬性屬性 `<shape>` ，例如 [形容詞 = "100，200，150"]。 在專案內 `&lt;formulas&gt;` ，您可以在重新調整清單中參考這些值。 您可以將 **形容詞** 清單中 (100) 的第一個值稱為 \# 0，第二個值 (200) 可稱為 \# 1，依此類推。

例如，若要繪製微笑的臉部，您可以輸入下列 VML 標記法：

![shape1.gif (735 個位元組) ](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   `adj="17520"` 定義值 (= 17520) 。 這個值可以參考為 \# 0。
-   第一個公式會 `<v:f eqn="sum 33030 0 #0"/>` 定義值 (= 33030 + 0- \# 0) 。 這個值可以參考為 @0 。
-   第二個公式會 `<v:f eqn="prod #0 4 3"/>` 定義值 (= \# 0 \* 4/3) 。 這個值可以參考為 @1 。
-   第三個公式會 `<v:f eqn="prod @0 1 3"/>` 定義值 (= @0 \* 1/3) 。 這個值可以參考為 @2 。
-   第四個公式會 `<v:f eqn="sum @1 0 @2"/>` 定義值 (= @1 + 0 -@2) 。 這個值可以參考為 @3 。
-   在專案內 `<path>` ，第一個 (@0) 和第四個 () 公式中定義的值 @3 會用來判斷圖形的外框。

如果您變更 **形容詞** 清單（例如），則 `adj="20000"` 參考 **形容詞** 清單的公式值也會變更，並影響微笑面，如下所示：

![shape2.gif (765 個位元組) ](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858392) 。

 

 
