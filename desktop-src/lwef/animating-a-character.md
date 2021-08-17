---
title: 製作字元動畫
description: 製作字元動畫
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b970f1cdc9de9c973d298bbe963bfa70e4de3733869292e54d5d32742c722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976778"
---
# <a name="animating-a-character"></a>製作字元動畫

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

載入字元之後，您可以使用數種 Microsoft 代理程式的方法來建立字元的動畫。 第一個使用的通常是 [**Show**](show-method.md) 方法。 **顯示** 會讓字元的框架顯示出來，並播放指派給該字元 **顯示** 狀態的動畫。

在字元的框架顯示之後，您可以使用 [**play**](play-method.md) 方法，指定動畫的名稱來播放該動畫。 動畫名稱是字元定義專用的。 當動畫播放時，其視窗的圖形會變更為符合框架中的影像。 這會導致在桌面和所有視窗（或迭置 *順序*）上方顯示的可移動圖形影像或 *sprite*。

如果字元的檔案儲存在本機，您就可以呼叫 [**Play**](play-method.md) 方法。 在其他情況下（例如，當您載入時）。從 HTTP 伺服器 ACF 字元，您必須使用 [**Get**](get-method.md) (或 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare)) 方法來先取出動畫資料。 這會導致代理程式從伺服器要求動畫檔案，並將它儲存在本機電腦上的瀏覽器緩衝區中。

「 [**說話**](speak-method.md) 」方法可讓您對字元進行程式設計，並自動對輸出進行 lip 同步處理。 本檔的輸出一節會涵蓋進一步的詳細資料。

您可以使用 [**MoveTo**](moveto-method.md) 方法將字元放在新位置。 當您呼叫 **MoveTo** 方法時，Microsoft Agent 會根據字元的目前位置自動播放適當的動畫，然後移動字元的框架。 同樣地，當您呼叫 [**GestureAt**](gestureat-method.md)時，Microsoft Agent 會根據該字元的位置和在呼叫中指定的位置，來播放適當的 gesturing 動畫。

若要隱藏字元，請呼叫 [hide](hide-method.md) 方法。 這會自動播放與該字元 **隱藏** 狀態相關聯的字元，然後隱藏字元的框架。 不過，您也可以藉由設定字元的 [**Visible**](visible-property.md) 屬性來隱藏或顯示字元。

Microsoft Agent 會以非同步方式處理所有的動畫呼叫或 *要求*。 這可讓您的應用程式程式碼在處理要求時繼續處理其他事件。 例如，對 [**Play**](play-method.md) 方法的呼叫會將動畫放在字元的佇列中，以便順序播放動畫。 不過，這表示您無法假設對其他函式的呼叫將會在程式碼中跟隨的動畫之後執行。 例如，呼叫 **Play** 或 [**MoveTo**](moveto-method.md) 之後的語句會在動畫完成之前執行。

您可以建立動畫要求的物件參考，然後在動畫開始或完成時，監視伺服器用來通知用戶端字元的 [要求](the-request-object.md) 事件，藉此將程式碼與字元佇列中的動畫同步處理。 例如，如果您想要在字元完成動畫時顯示訊息方塊，您可以在 [**RequestComplete**](requestcomplete-event.md) 事件處理副程式中放入訊息方塊呼叫，檢查是否有特定的要求識別碼。

隱藏字元時，伺服器不會播放動畫;不過，它仍會將動畫要求排入佇列並處理 (播放動畫) 並將要求狀態傳遞回用戶端。 在隱藏狀態中，字元無法變成輸入-主動。 不過，如果使用者在) 啟用語音輸入時說出 (的名稱，則伺服器會自動顯示該字元。

當您的用戶端應用程式同時載入多個字元時，Microsoft Agent 的動畫服務可讓您獨立地建立字元的動畫 [**，或**](interrupt-method.md)使用 [**Wait**](wait-method.md)、插斷或 [**停止**](stop-method.md)方法來同步處理其動畫。

Microsoft 代理程式也會自動為您播放其他動畫。 例如，如果字元的狀態未變更數秒，則代理程式會開始播放指派給該字元 **閒置** 動畫的動畫。 同樣地，當語音輸入啟用時，代理程式會在偵測到語句時播放字元的 **接聽** 動畫，然後 **聽到** 動畫。 這些伺服器管理的動畫稱為「 *狀態*」，並會在建立字元時定義。 如需詳細資訊，請參閱 [設計 Microsoft Agent 的字元](agent-states.md)。

 

 