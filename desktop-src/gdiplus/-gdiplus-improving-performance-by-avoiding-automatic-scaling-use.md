---
description: 如果您只將影像的左上角傳遞給 DrawImage 方法，Windows GDI + 可能會調整影像，這會降低效能。
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: 藉由避免自動調整來改善效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972876"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>藉由避免自動調整來改善效能

如果您只將影像的左上角傳遞給 **DrawImage** 方法，WINDOWS gdi + 可能會調整影像，這會降低效能。

下列對 **DrawImage** 方法的呼叫會指定 (50 30) 的左上角，但不會指定目的地矩形：


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



雖然這是最簡單的 **DrawImage** 方法版本（以所需的引數數目為限），但不一定是最有效率的。 如果目前顯示裝置上的每英寸點數，與建立映射的裝置上的點數目不同，則 GDI + 會調整影像，讓其在目前顯示裝置上的實體大小盡可能靠近其在建立裝置上的實際大小。

如果您想要避免這樣的調整，請將目的地矩形的寬度和高度傳遞給 **DrawImage** 方法。 下列範例會繪製相同的影像兩次。 在第一種情況下，不會指定目的矩形的寬度和高度，而且會自動調整影像。 在第二個案例中， (以圖元) 為單位測量的寬度和高度指定為與原始影像的寬度和高度相同。


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



下圖顯示呈現兩次的影像。

![視窗的螢幕擷取畫面，其中包含不同刻度的一個影像的兩個版本](images/scaledtexture1.png)

 

 



