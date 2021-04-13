---
title: VML 群組元素
description: VML 群組元素
ms.assetid: 536c2380-2583-4fe8-a92e-c539de209a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c128fddb5f070c9dbb6bbbd92c172cd58f5bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375632"
---
# <a name="vml-group-element"></a>VML 群組元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義可以用來收集圖形的群組。

此元素支援與圖形相同的屬性，但下列專案除外：

-   **隱藏**
-   **type**
-   **形容詞**
-   **path**
-   **spid**
-   **透明度**
-   **chromakey**
-   **撫摸**
-   **strokecolor**
-   **strokeweight**
-   **已**
-   **fillcolor**
-   **Spt**
-   **ruleinitiator**
-   **ruleproxy**
-   **connectortype**
-   **bwmode**
-   **bwpure**
-   **bwnormal**
-   **forcedash**
-   **oleicon**
-   **preferrelative**
-   **Ole**

只有下列子項目可以與 **群組** 一起使用。

-   **群組**
-   **Shapetype**
-   **形狀**
-   **鎖定**

**範例**

下列範例顯示如何定義群組。


```HTML
<!-- Include the VML behavior -->
<style>v\: * { behavior: url(#default#VML);display:inline-block }</style>

<!-- Declare the VML namespace -->
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v"/>

<v:group id="group1" style="left:10px;top:10px;width:50px;height:50px;"
  coordorigin="0,0" coordsize="6000,6000">

<v:shape id="_x0000_s2051"
  style='position:relative;left:234.75pt;top:208.875pt;width:235.25pt;height:128.875pt'
  coordsize="3765,2060"
  path="m1285,251l1126,469,580,1009,,1285,25,1412,93,1547,194,1673,1017,2026,2312,2060,3209,1756,3765,1388,3278,680,3059,319,2976,,1285,251,1285,251xe"
  fillcolor="#bcbcd6" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

 <v:shape id="_x0000_s2052" style='position:relative;left:314.625pt;
  top:140.5pt;width:104pt;height:102pt' coordsize="1663,1633"
  path="m0,1355l177,1498,353,1582,840,1633,1378,1498,1663,1295,1545,456,1260,10,1025,,656,260,253,874,,1355,,1355xe"
  fillcolor="#99ebff" stroked="f">
  <v:path arrowok="t"/>
 </v:shape>

</v:group>
```





 

 