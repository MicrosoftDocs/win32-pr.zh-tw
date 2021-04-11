---
title: 推送的次要影像來源
description: 推送的次要影像來源
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player 行動外觀、按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021523"
---
# <a name="pushed-secondary-image-source"></a>推送的次要影像來源

視按鈕功能而定，您可能需要為按鈕的次要狀態定義推送影像的位置。 這會是使用者在第二次推送 PlayPause 函式按鈕時看到的影像。

若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。 然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的影像類型內使用的影像（以圖元為單位） (（以圖元為單位）) 。

例如，若要定義次要影像來源的已推播映射，如果您的映射在推送的點陣圖內，請輸入：


```C++
Pushed @ 248,0

```



次要狀態不能有已停用的映射。 次要影像會假設為與主要映射相同的寬度和高度。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**按鈕**](buttons.md)
</dt> </dl>

 

 




