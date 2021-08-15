---
title: 執行轉譯
description: 執行轉譯
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- 視覺效果，計時事件
- 自訂視覺效果，計時事件
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 視覺效果，RenderWindow 函式
- 自訂視覺效果，RenderWindow 函式
- 轉譯函數，參數
- RenderWindow 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af44299c8a8e34c8f63844dc7d2c143f1d85e0b622c50dd246ea12571d94af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390688"
---
# <a name="implementing-render"></a>執行轉譯

要考慮視覺化程式設計，最簡單的方式就是建立計時事件的處理常式。 在特定間隔中，Windows Media Player 會取得所播放音訊資料的快照集，並將快照集資料提供給目前載入的視覺效果。 這類似于事件驅動程式設計，而且是 Microsoft Windows 程式設計模型的一部分。 您會撰寫程式碼，並等候特定事件呼叫它。

如果您的程式碼是 [IWMPEffects：： Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) 函式的執行，以便在無視窗模式中轉譯，則會收到下列參數：

*TimedLevel*

這是定義您的程式碼將分析之音訊資料的結構。 此結構是由兩個數組所組成。 第一個陣列是以頻率資訊為基礎，其中包含將音訊頻譜的快照分割成1024部分。 陣列中的每個資料格都包含0到255的值。 第一個儲存格從 20 Hz 和最後一個 22050 Hz 開始。 陣列以二維表示身歷聲音訊。 第二個數組是以波形資訊為基礎，而且對應到音訊電源，也就是最強的波浪值，值愈大。 波形陣列是以極短時間間隔拍攝之音訊電力最後1024磁區的細微快照。 這個陣列也是兩個代表身歷聲音訊的維度。

*HDC*

這是 Microsoft Windows 的裝置內容控制碼。 這會提供一種方式來識別要 Windows 的繪圖介面。 您不需要加以建立，只需要將它用於特定的繪圖函式呼叫。

*矩形*

這是定義繪圖介面大小的 Microsoft Windows 矩形。 這是具有四個屬性的簡單矩形： **left**、 **right**、 **top** 和 **底端**。 實際的值是由 Windows Media Player 提供，因此您可以決定使用者或外觀開發人員如何調整您將繪製的視窗大小。 它也會決定要呈現其效果的 HDC 上的位置。

如果您的程式碼是 **IWMPEffects2：： RenderWindowed** 函式的執行，以便在視窗中轉譯，則會收到下列參數：

*TimedLevel*

這是 **轉譯函數所接收的相同** 資訊。

*fRequiredRender*

*FRequiredRender* 參數會通知您，您的視覺效果必須自行重新繪製，例如，當另一個視窗拖曳至另一個視窗時。 當此值為 false 時，如果目前的媒體專案已停止或暫停，您可以放心地跳過轉譯程式碼。 這可讓您避免不必要地耗用 CPU 迴圈。

外掛程式 Wizard 所產生的範例外掛程式不會提供 **RenderWindowed** 的自訂執行。 相反地，範例外掛程式程式碼會從 [IWMPEffects2：： Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)中 Windows Media Player 所提供的父視窗抓取裝置內容，然後以 RECT 結構的形式抓取父視窗的維度，然後呼叫 **，以使用** 來自 **RenderWindowed** 的裝置內容、RECT 和計時層級指標進行轉譯。

下列各節提供 **有關執行轉譯** 的詳細資訊：

-   [使用計時層級](using-timed-levels.md)
-   [使用裝置內容](using-device-contexts.md)
-   [使用矩形](using-rectangles.md)
-   [範例轉譯程式碼](sample-render-code.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行您的程式碼**](implementing-your-code.md)
</dt> </dl>

 

 




