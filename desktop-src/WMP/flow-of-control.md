---
title: 控制項 Flow
description: 控制項 Flow
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- 視覺效果，程式流程
- 自訂視覺效果，程式流程
- 視覺效果，控制流程
- 自訂視覺效果，控制流程
- 視覺效果，計時事件
- 自訂視覺效果，計時事件
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 視覺效果，RenderWindow 函式
- 自訂視覺效果，RenderWindow 函式
- 轉譯函式，視覺效果程式流程
- RenderWindow 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332d9c907e7c25f81d01bc8adf48c6d4d91a7b17763a1b0daf0007a8534ac4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934737"
---
# <a name="flow-of-control"></a>控制項 Flow

音訊資料會透過檔案或資料流程持續進入 Windows Media Player。 這項資料會傳遞至您的視覺效果。 您可以在定義的介面上繪製，並將該介面傳回 Windows Media Player。 此交換會在一秒內發生數次，而且對使用者而言，結果會是可即時移至音樂的滿意動畫。

以下是視覺效果程式流程的特定順序：

1.  在時間間隔內，Windows Media Player 會取得現正播放之音訊的快照。
2.  Windows Media Player 透過轉譯函數和 **RenderWindowed** 函式，將該快照集的資料提供給 **您的視覺** 效果。
3.  您必須撰寫將在呼叫 **轉譯和** **RenderWindowed** 時執行的程式碼。 當轉譯無視窗時，您的程式碼會使用 Windows Media Player 所定義的裝置內容，或使用您在呈現視窗時所建立的視窗來繪製。
4.  在目前面板指定的區域中，Windows Media Player 會顯示程式碼所繪製的內容。
5.  此程式會一秒重複幾次，以建立會對音樂計時的圖形動畫。 當音樂停止播放時，視覺效果就會停止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開發人員總覽**](developer-overview.md)
</dt> </dl>

 

 




