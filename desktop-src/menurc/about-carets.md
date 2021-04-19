---
title: 關於游標
description: 本主題討論游標。
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- 資源，游標
- 游標，移除
- 閃爍線
- 閃爍的區塊
- 閃爍的點陣圖
- 游標，可見度
- 游標，閃爍時間
- 閃爍時間
- 游標，職位
- 移除游標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969102"
---
# <a name="about-carets"></a>關於游標

系統會為每個訊息佇列提供一個插入號。 只有當視窗具有鍵盤焦點或作用中時，才會建立插入號。 在失去鍵盤焦點或變成非使用中之前，視窗應該會終結插入號。 如需鍵盤輸入的詳細資訊，請參閱 [鍵盤輸入](/windows/desktop/inputdev/keyboard-input)。

您可以使用 [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) 函式來指定插入號的參數。 系統會將插入號的位置、寬度和高度所指定的矩形內的圖元色彩反轉，藉以形成插入號。 寬度和高度是以邏輯單元指定;因此，插入點的外觀會受限於視窗的對應模式。

本節將討論下列主題。

-   [插入號可見度](#caret-visibility)
-   [插入號閃爍時間](#caret-blink-time)
-   [插入號位置](#caret-position)
-   [移除插入號](#removing-a-caret)

## <a name="caret-visibility"></a>插入號可見度

在定義插入號之後，請使用 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 函式讓插入號變成可見。 當插入號出現時，它會自動開始閃爍。 為了顯示實線的插入號，系統會反轉矩形中的每個圖元;為了顯示灰色的插入號，系統會反轉每個其他圖元;為了顯示點陣圖插入號，系統只會反轉點陣圖的白色位。

## <a name="caret-blink-time"></a>插入號閃爍時間

反轉插入號所需的經過時間（以毫秒為單位）稱為 *閃爍時間*。 只要擁有訊息佇列的執行緒有訊息抽取處理訊息，插入號就會閃爍。

使用者可以使用主控台設定插入號的閃爍時間，而應用程式應該遵守使用者所選擇的設定。 應用程式可以使用 [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) 函數來判斷插入號的閃爍時間。 如果您要撰寫可讓使用者調整閃爍時間的應用程式（例如主控台小程式），請使用 [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) 函數將閃爍時間的速率設定為指定的毫秒數。

*Flash time* 是顯示、反轉和還原插入號的顯示所需的經過時間（以毫秒為單位）。 插入號的閃爍時間與閃爍時間最多兩倍。

## <a name="caret-position"></a>插入號位置

您可以使用 [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) 函數來判斷插入號的位置。 在用戶端座標中的位置會複製到 **GetCaretPos** 中參數所指定的結構。 應用程式可以使用 [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) 函數，在視窗中移動插入號。 只有當視窗已經擁有插入點時，才可以移動插入號。 **SetCaretPos** 可以移動插入號（不論是否為可見）。

## <a name="removing-a-caret"></a>移除插入號

您可以藉由隱藏插入號來暫時移除它，也可以藉由終結插入號來永久移除插入號。 若要隱藏插入號，請使用 [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) 函數。 當您的應用程式必須在處理訊息時重繪畫面，但必須讓插入號離開時，這會很有用。 當應用程式完成繪圖時，可以使用 [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) 函式再次顯示插入號。 隱藏插入號不會終結其形狀或使插入點失效。 隱藏插入號是累計的;也就是，如果應用程式呼叫 **HideCaret** 五次，它也必須呼叫 **ShowCaret** 五次，插入號才會再次出現。

若要從畫面中移除插入號並終結其圖形，請使用 [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) 函式。 只有當目前工作的相關視窗擁有插入號時， **DestroyCaret** 才會終結插入號。

 

 