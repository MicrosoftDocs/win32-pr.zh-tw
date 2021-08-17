---
description: 此區段會列出 GetROP2 和 SetROP2 函式所使用的二元點陣作業程式碼。 點陣作業碼定義 GDI 如何將所選畫筆的位與目的地點陣圖中的位結合。
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: 二元點陣運算
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462c07165d7f377f2a536722bf2f728446c308503108474cbb6a585cee6f68e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105807"
---
# <a name="binary-raster-operations"></a>二元點陣運算

此區段會列出 [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) 和 [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) 函式所使用的二元點陣作業程式碼。 點陣作業碼定義 GDI 如何將所選畫筆的位與目的地點陣圖中的位結合。

每個點陣作業程式碼都代表一個布耳運算，其中所選畫筆和目的點陣圖中的圖元值會合並。 以下是這些作業中使用的兩個運算元。



| 運算元 | 意義            |
|---------|--------------------|
| P       | 選取的畫筆       |
| D       | 目的地點陣圖 |



 

這些作業中使用的布林運算子如下所示。



| 運算子 | 意義                    |
|----------|----------------------------|
| a        | 位元 AND                |
| n        | 位 NOT (反向)       |
| o        | 位元 OR                 |
| x        | 位互斥 OR (XOR)  |



 

所有布林值作業都會以反轉波蘭文標記法呈現。 例如，下列作業會以畫筆的圖元值與所選筆刷的組合來取代目的地點陣圖中的圖元值：


```C++
DPo 
```



每個點陣作業程式碼都是一個32位的整數，其高序位單字是布耳運算索引，而其低序位字是作業程式碼。 16位作業索引是零擴充的8位值，表示在兩個參數上的布耳運算所產生的所有可能結果 (在此案例中，) 的畫筆和目的地值。 例如，下列清單會顯示 DPo 和 DPan 作業的作業索引。



| P   | D   | DPo | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

下列清單概述繪圖模式以及它們所代表的布耳運算。



| 點陣運算 | 布耳運算 |
|------------------|-------------------|
| R2 \_ 黑色        | 0                 |
| R2 \_ COPYPEN      | P                 |
| R2 \_ MASKNOTPEN   | DPna              |
| R2 \_ MASKPEN      | Dpa               |
| R2 \_ MASKPENNOT   | PDna              |
| R2 \_ MERGENOTPEN  | DPno              |
| R2 \_ MERGEPEN     | DPo               |
| R2 \_ MERGEPENNOT  | PDno              |
| R2 \_ NOP          | D                 |
| R2 \_ 未          | DN                |
| R2 \_ NOTCOPYPEN   | Pn                |
| R2 \_ NOTMASKPEN   | DPan              |
| R2 \_ NOTMERGEPEN  | DPon              |
| R2 \_ NOTXORPEN    | DPxn              |
| R2 \_ 白色        | 1                 |
| R2 \_ XORPEN       | DPx               |



 

若為單色裝置，GDI 會將零值對應至黑色，並將值1對應至白色。 如果應用程式嘗試使用可用的二進位點陣運算在白色目的地上繪製黑色畫筆，則會發生下列結果。



| 點陣運算 | 結果             |
|------------------|--------------------|
| R2 \_ 黑色        | 可見的黑色線條 |
| R2 \_ COPYPEN      | 可見的黑色線條 |
| R2 \_ MASKNOTPEN   | 沒有可見的行    |
| R2 \_ MASKPEN      | 可見的黑色線條 |
| R2 \_ MASKPENNOT   | 可見的黑色線條 |
| R2 \_ MERGENOTPEN  | 沒有可見的行    |
| R2 \_ MERGEPEN     | 可見的黑色線條 |
| R2 \_ MERGEPENNOT  | 可見的黑色線條 |
| R2 \_ NOP          | 沒有可見的行    |
| R2 \_ 未          | 可見的黑色線條 |
| R2 \_ NOTCOPYPEN   | 沒有可見的行    |
| R2 \_ NOTMASKPEN   | 沒有可見的行    |
| R2 \_ NOTMERGEPEN  | 可見的黑色線條 |
| R2 \_ NOTXORPEN    | 可見的黑色線條 |
| R2 \_ 白色        | 沒有可見的行    |
| R2 \_ XORPEN       | 沒有可見的行    |



 

針對色彩裝置，GDI 會使用 RGB 值來表示畫筆和目的地的色彩。 RGB 色彩值是包含紅色、綠色和藍色色彩欄位的長整數，每個都指定指定色彩的濃度。 濃度的範圍是從0到255。 這些值會以長整數的三個低序位位元組封裝。 畫筆的色彩一律是純色，但目的地的色彩可能是任何二或三種色彩的混合。 如果應用程式嘗試使用可用的二進位點陣運算，在藍色目的地繪製白色畫筆，則會發生下列結果。



| 點陣運算 | 結果                 |
|------------------|------------------------|
| R2 \_ 黑色        | 可見的黑色線條     |
| R2 \_ COPYPEN      | 可見的白色線條     |
| R2 \_ MASKNOTPEN   | 可見的黑色線條     |
| R2 \_ MASKPEN      | 不可見的藍線    |
| R2 \_ MASKPENNOT   | 可見的紅色/綠線 |
| R2 \_ MERGENOTPEN  | 不可見的藍線    |
| R2 \_ MERGEPEN     | 可見的白色線條     |
| R2 \_ MERGEPENNOT  | 可見的白色線條     |
| R2 \_ NOP          | 不可見的藍線    |
| R2 \_ 未          | 可見的紅色/綠線 |
| R2 \_ NOTCOPYPEN   | 可見的黑色線條     |
| R2 \_ NOTMASKPEN   | 可見的紅色/綠線 |
| R2 \_ NOTMERGEPEN  | 可見的黑色線條     |
| R2 \_ NOTXORPEN    | 不可見的藍線    |
| R2 \_ 白色        | 可見的白色線條     |
| R2 \_ XORPEN       | 可見的紅色/綠線 |



 

 

 



