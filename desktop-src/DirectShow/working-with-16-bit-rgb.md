---
description: 使用16位 RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: 使用16位 RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660d5b0223bab6c19a89e4316f7dffce56ec0545f83c72f7316b9278dfa3e4c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071792"
---
# <a name="working-with-16-bit-rgb"></a>使用16位 RGB

針對16位未壓縮的 RGB 定義了兩種格式：

-   MEDIASUBTYPE \_ 555 會針對圖元中的紅色、綠色和藍色元件使用五個位。 **文字** 中最有效的位會被忽略。
-   MEDIASUBTYPE \_ 565 針對 red 和 blue 元件使用五個位，綠色元件則使用六位。 這種格式反映了人類願景對可見頻譜之綠色部分最敏感的事實。

**RGB 565**

若要從 RGB 565 影像中將色彩元件解壓縮，請將每個圖元視為 **單字** 類型，並使用下列位元遮罩：


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



從圖元取得色彩元件，如下所示：


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



請記住，紅色和藍色通道是5位，而綠色通道為6位。 若要將這些值轉換為8位元件 (24 位或32位 RGB) ，您必須將適當的位數向左移位：


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



反轉此進程以建立 RGB 565 圖元。 假設色彩值已截斷為正確位數：


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

使用 RGB 555 基本上與 RGB 565 相同，不同之處在于位元遮罩和位移位作業不同。 若要從 RGB 555 圖元取得色彩元件，請執行下列動作：


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



若要將紅色、綠色和藍色色彩值封裝成 RGB 555 圖元，請執行下列動作：


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[未壓縮的 RGB 影片子類型](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



