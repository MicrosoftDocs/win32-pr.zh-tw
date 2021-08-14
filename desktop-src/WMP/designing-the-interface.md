---
title: 設計介面
description: 設計介面
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Windows Media Player行動外觀，使用者介面
- 外觀，使用者介面
- 建立外觀，使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b11dee2a6236f2a279756644a88d69e267c5da93240b5e12c19c32d86e30a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749857"
---
# <a name="designing-the-interface"></a>設計介面

一旦選擇了函數之後，就可以設計介面。 已選擇簡單的介面來符合功能。 這些控制項的符號是從標準的 VCR 控制項所選擇。

下圖顯示介面看起來的樣子。

![範例介面](images/ceswmful.png)

-   **[PlayPause] 或 [PlayPauseStop] 按鈕。** 使用者將最常使用此按鈕，因此您可能會考慮使用較大的按鈕。 右上角可讓使用者快速找到適當的位置。 實心箭號可用來指出播放和兩個垂直線 (此處未顯示) 將用來表示暫停。
    > [!Note]  
    > 只有在建立 Windows Media Player 10 行動裝置版或更新版本的面板時，才能使用 [PlayPauseStop] 按鈕。

     

-   **停止按鈕。** 為了讓您輕鬆找到，它會放在左上角。 使用正方形表示停止。 如果您要建立 Windows Media Player 10 行動裝置版或更新版本的面板，[PlayPauseStop] 按鈕已經提供此功能。
-   **Next 和上一頁按鈕。** 因為它們不會經常使用，所以會放在左側。 下一步是在上一個按鈕的上方，因為人們很可能想要在播放清單中向前移動。 使用雙箭號，因為它們在函式中類似于向前快轉控制項。
-   **磁片區的跟蹤。** 這是放在畫面底部，而且是一個簡單的線條，其頂端有一個 thumb 按鈕。
-   **[字幕] 文字方塊。** 這會放置在 [PlayPause] 或 [PlayPauseStop] 按鈕底下，讓您很容易看到。

您可能會想要先將其繪製，並試驗每個使用者介面元素的位置。 此處所示的設計是為了簡單且便於使用而選擇的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀指南**](skin-guide.md)
</dt> </dl>

 

 




