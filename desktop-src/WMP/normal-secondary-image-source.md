---
title: 一般次要影像來源
description: 一般次要影像來源
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player行動外觀，按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f6aeb48ceabc873d4aeb0db910db896712fe16377aa0f67b76205ad8a39c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573728"
---
# <a name="normal-secondary-image-source"></a>一般次要影像來源

視按鈕功能而定，您可能需要為按鈕的次要狀態定義正常影像的位置。 這會是使用者第一次推送 PlayPause 函式按鈕時所看到的影像。

若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。 然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。

例如，若要定義次要影像來源的一般影像，如果您的映射位於推播點陣圖內，請輸入：


```C++
Pushed @ 210,0

```



次要狀態不能有已停用的映射。 次要影像會假設為與主要映射相同的寬度和高度。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**按鈕**](buttons.md)
</dt> </dl>

 

 




