---
title: 點擊 RGB 色彩
description: 點擊 RGB 色彩
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Windows Media Player 行動外觀、按鈕色彩
- 外觀，按鈕色彩
- 外觀、按鈕的參考
- 外觀、色彩中的按鈕
- 外觀的色彩參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965184"
---
# <a name="hit-rgb-color"></a>點擊 RGB 色彩

如果您使用的是 [PushHit]、[ToggleHit] 和 [2PushHit])  (的 [區域] 按鈕，您必須定義 Windows Media Player 將用來決定按鈕點擊區域的色彩。 這個值必須使用以逗號分隔的三個正整數來指定。 這些整數代表點陣圖色彩的紅色、綠色和藍色量，範圍從0到255。

> [!Note]  
> 在 Windows Media Player 10 行動裝置版或更新版本的面板中，按鈕類型已被取代。

 

您可以針對這些值使用任何色彩，但請確定您定義的每個區域按鈕在區域影像檔中都有唯一的色彩，而您在這裡定義的色彩值，會符合區域影像中使用的實際色彩。

下表顯示您可能想要使用的一些典型色彩。



| 值       | 描述 |
|-------------|-------------|
| 0、0、0       | 黑色       |
| 255255255 | 白色       |
| 255、0、0     | 紅色         |
| 0255，0     | 綠色       |
| 0、0255     | 藍色        |



 

如果您未使用區域按鈕，則必須輸入下列內容：


```C++
0,0,0

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**按鈕**](buttons.md)
</dt> </dl>

 

 




