---
description: 您可以藉由指定原始影像左上角、右上角和左下角的目的地點，來旋轉、反映及扭曲影像。
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: 旋轉、反映及扭曲影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943942"
---
# <a name="rotating-reflecting-and-skewing-images"></a>旋轉、反映及扭曲影像

您可以藉由指定原始影像左上角、右上角和左下角的目的地點，來旋轉、反映及扭曲影像。 三個目的地點決定將原始矩形影像對應至平行四邊形的仿射轉換。  (原始影像的右下角會對應到平行四邊形的第四個角落，這是從三個指定的目的點計算而來。 ) 

例如，假設原始影像是左上角的矩形，位於 (0、0) 、右上角 (100、0) 和左下角，位於 (0，50) 。 現在假設我們將這三個點對應到目的地點，如下所示。



| 原始點       | 目的地點 |
|----------------------|-------------------|
| 左上 (0、0)     | (200, 20)         |
| 右上角的 (100，0)  | (110, 100)        |
| 左下 (0、50)    | (250, 30)         |



 

下圖顯示原始影像和對應至平行四邊形的影像。 原始影像已扭曲、反映、旋轉和轉譯。 沿著原始影像上邊緣的 X 軸會對應到 (200、20) 和 (110，100) 執行的行。 沿著原始影像左邊緣的 y 軸，會對應至透過 (200、20) 和 (250，30) 執行的線條。

![圖例顯示座標軸原點的彩色條紋，以及扭曲和不同位置、旋轉和大小的相同條紋](images/stripes1.png)

下列範例會產生上圖所示的影像。


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



下圖顯示套用至照片影像的類似轉換。

![顯示相同相片兩次的圖例;第二個是反轉、扭曲，而且有不同的大小、旋轉和位置](images/transformedclimber.png)

下圖顯示套用至中繼檔的類似轉換。

![顯示圖形和文字的圖例，然後以不同的位置、旋轉和大小進行反轉、扭曲及調整大小](images/transformedmetafile.png)

 

 



