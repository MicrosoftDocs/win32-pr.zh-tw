---
title: 一般的三映射來源
description: 一般的三映射來源
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372483"
---
# <a name="normal-tertiary-image-source"></a>一般的三映射來源

您必須為按鈕的第三個狀態定義一般影像的位置，才能 PlayPauseStop 按鈕函式。 這會是使用者按下 [PlayPauseStop] 按鈕以開始串流處理實況廣播之後看到的影像。

若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。 然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。

例如，若要定義第三個影像來源的一般影像，如果您的映射在推送的點陣圖內，請輸入：


```C++
Pushed @ 286,0

```



第三個狀態不能有已停用的映射。 系統會假設第三個影像的寬度和高度與主要和次要影像相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**按鈕**](buttons.md)
</dt> </dl>

 

 




