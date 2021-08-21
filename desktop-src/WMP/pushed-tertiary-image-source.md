---
title: 推送的第三個映射來源
description: 推送的第三個映射來源
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Windows Media Player行動外觀，按鈕影像來源
- 外觀，按鈕影像來源
- 外觀、按鈕的參考
- 外觀、影像來源中的按鈕
- 外觀、按鈕的影像來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649730c877f9f5063737c16638b2c27d5e25a7d5578c2c7bce75f9f4fb24b71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118834207"
---
# <a name="pushed-tertiary-image-source"></a>推送的第三個映射來源

PlayPauseStop 按鈕函式需要您針對按鈕的第三個狀態定義推播影像的位置。 這會是使用者在串流處理實況廣播時，會看到的影像（當他們推送 PlayPauseStop 按鈕時）。

若要定義此影像，您必須輸入映射類型，後面接著一個空格和 @ 符號以及另一個空格。 然後，您必須輸入兩個正整數，以定義您想要在繪圖來源的點陣圖類型內使用之影像的左上座標 (（以圖元為單位）) 。

例如，若要定義第三個影像來源的推播映射，如果您的映射在推送的點陣圖內，請輸入：


```C++
Pushed @ 324,0

```



第三個狀態不能有已停用的映射。 系統會假設第三個影像的寬度和高度與主要和次要影像相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**按鈕**](buttons.md)
</dt> </dl>

 

 




