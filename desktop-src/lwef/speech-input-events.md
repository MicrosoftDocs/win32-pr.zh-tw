---
title: 語音輸入事件
description: 語音輸入事件
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0dc75bb010286b7645c206d192913017472829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022118"
---
# <a name="speech-input-events"></a>語音輸入事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

此外，在 [**命令**](command-event.md) 事件通知中，代理程式也會在伺服器開啟或關閉接聽模式時，使用 [**ListenStart**](listenstart-event.md) 和 [**ListenComplete**](listencomplete-event.md) 事件 ([**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md)) 來通知輸入-主動用戶端。 不過，如果使用者按下接聽模式鍵，而且沒有相符的語音辨識引擎可供輸入-主動用戶端的最上層字元使用，則伺服器會啟動接聽熱鍵模式超時，但不會為字元的作用中用戶端產生 **ListenStart** 事件。 如果在超時時間完成之前，使用者會使用「語音辨識引擎」支援來啟用另一個字元，伺服器會嘗試啟用語音輸入並產生 **ListenStart** 事件。

同樣地，如果用戶端嘗試使用 [**接聽**](listen-method.md) 方法開啟接聽模式，且沒有相符的語音辨識引擎可用，則呼叫會失敗，而且伺服器不會產生 [**ListenStart**](listenstart-event.md)事件。 在 Microsoft Agent 控制項中， **接聽** 方法會傳回 **False**，但呼叫不會引發錯誤。

當接聽金鑰模式為開啟，且使用者切換到使用不同語音辨識引擎的字元時，伺服器會切換至並啟動該引擎，並觸發 [**ListenComplete**](listencomplete-event.md) ，然後觸發 [**ListenStart**](listenstart-event.md) 事件。 如果啟動的字元沒有可用的語音辨識引擎 (因為未安裝一個，或沒有符合啟動的字元語言識別項設定) ，伺服器將會觸發先前所啟用之字元的 **ListenComplete** 事件，並將 **原因** 參數中的值傳回。 但是，伺服器不會針對沒有語音辨識支援的用戶端產生 **ListenStart** 或 **ListenComplete** 事件。

如果用戶端成功呼叫 [**接聽**](listen-method.md) 方法，且沒有語音辨識引擎支援的字元在接聽模式超時時間完成之前變成輸入-主動，然後使用者切換回原始用戶端的字元，伺服器將會產生該用戶端的 [**ListenStart**](listenstart-event.md) 事件。

如果輸入-主動用戶端在接聽模式下變更 [**SRModeID**](srmodeid-property.md) 來切換語音辨識引擎，則伺服器會切換至並啟動該引擎，而不會重新觸發 [**ListenStart**](listenstart-event.md) 事件。 但是，如果指定的引擎無法使用，呼叫就會失敗 (在控制項) 中引發錯誤，而且伺服器也會呼叫 [**ListenComplete**](listencomplete-event.md) 事件。

 

 




