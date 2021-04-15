---
description: 已編制索引的頂點混色可延伸 Direct3D 中的頂點混合支援，以允許使用矩陣進行混合。
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: " (Direct3D 9) 的索引頂點混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467440"
---
# <a name="indexed-vertex-blending-direct3d-9"></a> (Direct3D 9) 的索引頂點混合

已編制索引的頂點混色可延伸 Direct3D 中的頂點混合支援，以允許使用矩陣進行混合。 這些矩陣是使用矩陣索引來參考的。 這些索引是以每個頂點為基礎提供，並參考最多256個矩陣的調色板。 每個索引都是8位，而且每個頂點最多可有四個索引，以允許每個頂點混合四個矩陣。 索引會封裝成 DWORD。 因為索引是以每個頂點為基礎來指定，最多12個矩陣可能會影響單一三角形，而調色板中的任何矩陣都可能影響一個繪製呼叫的頂點。 這種方法有下列優點。

-   它可讓更多的矩陣影響單一三角形。
-   它可讓您在相同的繪製呼叫中傳遞更多混合的三角形。
-   它讓頂點與三角形索引無關。 這可讓漸進式網格與頂點混色一起使用。

這種方法的其中一個缺點是，它無法在頂點處理之前進行鑲嵌式時，與曲線表面的基本專案搭配使用。

下圖會示範四個矩陣如何影響頂點。 每個頂點最多可有4個索引，因此四個矩陣可依頂點進行混合。 此圖表會使用以0、2、5和6為索引的矩陣。

![使用256可用矩陣的4個索引頂點混合圖](images/dword1.png)

下圖會示範最多12個矩陣如何影響三角形。 使用以每個頂點指定的索引，最多12個矩陣可能會影響三角形。

![使用 12 256 可用矩陣的索引頂點混合圖](images/dword2.png)

下列方程式會決定矩陣如何影響頂點的一般案例。

![索引頂點混合的方程式](images/indexedvblend.png)

V <sub>模型</sub> 是輸入模型空間頂點的位置。 Index0..Index3 是封裝成 DWORD 的每個頂點矩陣索引。 M \[ \] 是取得索引的世界矩陣陣列。 b ₀ .。。b ₂是 blend 加權。 V<sub>世界</sub> 是輸出世界空間頂點的位置。

如需索引頂點混合的詳細資訊，請參閱 [使用索引頂點混合 (Direct3D 9) ](using-indexed-vertex-blending.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[幾何混合](geometry-blending.md)
</dt> </dl>

 

 



