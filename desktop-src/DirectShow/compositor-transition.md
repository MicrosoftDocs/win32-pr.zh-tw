---
description: 組合器轉換
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: 組合器轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550730"
---
# <a name="compositor-transition"></a>組合器轉換

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

組合器轉換會在背景將 subrectangle 從前景合成至指定的矩形，而不會改變背景的其餘部分。 使用這項轉換來建立分割畫面或圖片圖片效果。

下圖顯示組合器轉換：

![組合器轉換](images/trans-compositor.png)

類別識別碼 (CLSID) ： {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

CLSID 變數名稱： CLSID \_ DxtCompositor

易記名稱： "DxtCompositor"

屬性



| 屬性   | 類型 | 預設 | 描述                                                    |
|------------|------|---------|----------------------------------------------------------------|
| 高度     | long | 0       | 目標矩形的高度（以圖元為單位）。                     |
| OffsetX    | long | 0       | 目標矩形的水準位移（以圖元為單位）。          |
| OffsetY    | long | 0       | 目標矩形的垂直位移（以圖元為單位）。            |
| SrcHeight  | long | 0       | 來源的 subrectangle 高度（以圖元為單位）。       |
| SrcOffsetX | long | 0       | Subrectangle 在來源上的 x 座標（以圖元為單位）。 |
| SrcOffsetY | long | 0       | Subrectangle 在來源上的 y 座標（以圖元為單位）。 |
| SrcWidth   | long | 0       | 來源上的 subrectangle 寬度（以圖元為單位）。        |
| 寬度      | long | 0       | 目標矩形的寬度（以圖元為單位）。                      |



 

下圖說明這些屬性：

![組合器屬性](images/compmeasure.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換和效果](transitions-and-effects.md)
</dt> </dl>

 

 



