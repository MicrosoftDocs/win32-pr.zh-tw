---
title: 將圖形分組
description: 本文描述如何在 VML 中將圖形分組，這是 Windows Internet Explorer 9 的已淘汰功能。
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- 網路研討會，群組圖形
- 設計網頁、群組圖形
- Vector Markup Language (VML) 、群組圖形
- VML (Vector Markup Language) 、群組圖案
- 向量圖形，群組圖形
- VML 圖形，群組
- 將圖形分組
- Vector Markup Language (VML) 、group 元素
- VML (Vector Markup Language) ，group 元素
- 向量圖形、群組元素
- 群組元素
- VML 元素、群組
- Vector Markup Language (VML) 、本機座標空間
- VML (Vector Markup Language) ，區域座標空間
- 向量圖形，區域座標空間
- 本機座標空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc9ac6da1d38bb6b30f685ebfd0f5a1d9d6026620a0e0c65366ee021668240a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056956"
---
# <a name="grouping-shapes"></a>將圖形分組

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

如您所學到的，您可以使用 VML 輕鬆地繪製個別的圖案。 在本節中，我們將說明將圖形群組在一起的優點，以及如何將圖形分組。

如果您有許多需要調整、移動或旋轉的圖形，您會發現為每個圖形個別設定屬性是很繁瑣的。 此外，您也會引發錯誤的邊際。 如果您可以將圖形分組，然後設定整個群組的屬性，就會比較好。

在 VML 中，您可以使用專案 `<group>` 將許多圖形群組在一起，讓它們可以轉換成一個單位。 例如，如下列 VML 標記法所示，您可以輕鬆地將兩個圖形群組在一起。


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



當將圖形分組時，它們會使用群組的 [區域座標空間](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) 。 因此，群組內的圖形可以進行調整，並一起移動。 您將會在 [使用本機座標空間] 主題中看到更多範例。

在群組內，您可以依需要擁有任意數量的圖形或群組。 當群組位於另一個群組內時，它稱為「嵌套群組」。 嵌套層級沒有任何限制。

例如，下列程式程式碼會示範3層級的嵌套群組。 Shape3 和 Shape4 在 GroupC 中。 Shape2 和 GroupC 在 GroupB 中。 Shape1 和 GroupB 在 GroupA 中。


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858388) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="summary"></a>摘要

您可以使用專案 `<group>` 將許多圖形群組在一起，讓它們可以轉換成一個單位。

 

 