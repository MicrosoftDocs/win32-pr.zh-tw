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
# <a name="speech-input-events"></a><span data-ttu-id="333b3-103">語音輸入事件</span><span class="sxs-lookup"><span data-stu-id="333b3-103">Speech Input Events</span></span>

<span data-ttu-id="333b3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="333b3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="333b3-105">此外，在 [**命令**](command-event.md) 事件通知中，代理程式也會在伺服器開啟或關閉接聽模式時，使用 [**ListenStart**](listenstart-event.md) 和 [**ListenComplete**](listencomplete-event.md) 事件 ([**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md)) 來通知輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="333b3-105">In addition, to the [**Command**](command-event.md) event notification, Agent also notifies the input-active client when the server turns the Listening mode on or off, using the [**ListenStart**](listenstart-event.md) and [**ListenComplete**](listencomplete-event.md) events ([**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md)).</span></span> <span data-ttu-id="333b3-106">不過，如果使用者按下接聽模式鍵，而且沒有相符的語音辨識引擎可供輸入-主動用戶端的最上層字元使用，則伺服器會啟動接聽熱鍵模式超時，但不會為字元的作用中用戶端產生 **ListenStart** 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-106">However, if the user presses the Listening mode key and there is no matching speech recognition engine available for the topmost character of the input-active client, the server starts the Listening hotkey mode time-out, but does not generate a **ListenStart** event for the active client of the character.</span></span> <span data-ttu-id="333b3-107">如果在超時時間完成之前，使用者會使用「語音辨識引擎」支援來啟用另一個字元，伺服器會嘗試啟用語音輸入並產生 **ListenStart** 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-107">If, before the time-out completes, the user activates another character with speech recognition engine support, the server attempts to activate speech input and generates the **ListenStart** event.</span></span>

<span data-ttu-id="333b3-108">同樣地，如果用戶端嘗試使用 [**接聽**](listen-method.md) 方法開啟接聽模式，且沒有相符的語音辨識引擎可用，則呼叫會失敗，而且伺服器不會產生 [**ListenStart**](listenstart-event.md)事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-108">Similarly, if a client attempts to turn on the Listening mode using the [**Listen**](listen-method.md) method and there is no matching speech recognition engine available, the call fails and the server does not generate a [**ListenStart**](listenstart-event.md)event.</span></span> <span data-ttu-id="333b3-109">在 Microsoft Agent 控制項中， **接聽** 方法會傳回 **False**，但呼叫不會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="333b3-109">In the Microsoft Agent control, the **Listen** method returns **False**, but the call does not raise an error.</span></span>

<span data-ttu-id="333b3-110">當接聽金鑰模式為開啟，且使用者切換到使用不同語音辨識引擎的字元時，伺服器會切換至並啟動該引擎，並觸發 [**ListenComplete**](listencomplete-event.md) ，然後觸發 [**ListenStart**](listenstart-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-110">When the Listening key mode is on and the user switches to a character that uses a different speech recognition engine, the server switches to and activates that engine and triggers a [**ListenComplete**](listencomplete-event.md) and then a [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="333b3-111">如果啟動的字元沒有可用的語音辨識引擎 (因為未安裝一個，或沒有符合啟動的字元語言識別項設定) ，伺服器將會觸發先前所啟用之字元的 **ListenComplete** 事件，並將 **原因** 參數中的值傳回。</span><span class="sxs-lookup"><span data-stu-id="333b3-111">If the activated character does not have an available speech recognition engine (because one is not installed or none match the activated character's language ID setting), the server will trigger the **ListenComplete** event for the previously activated character and passes back a value in the **Cause** parameter.</span></span> <span data-ttu-id="333b3-112">但是，伺服器不會針對沒有語音辨識支援的用戶端產生 **ListenStart** 或 **ListenComplete** 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-112">However, the server does not generate **ListenStart** or **ListenComplete** events for the clients that do not have speech recognition support.</span></span>

<span data-ttu-id="333b3-113">如果用戶端成功呼叫 [**接聽**](listen-method.md) 方法，且沒有語音辨識引擎支援的字元在接聽模式超時時間完成之前變成輸入-主動，然後使用者切換回原始用戶端的字元，伺服器將會產生該用戶端的 [**ListenStart**](listenstart-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-113">If a client successfully calls the [**Listen**](listen-method.md) method and a character without speech recognition engine support becomes input-active before the Listening mode time-out completes, and then the user switches back to the character of the original client, the server will generate a [**ListenStart**](listenstart-event.md) event for that client.</span></span>

<span data-ttu-id="333b3-114">如果輸入-主動用戶端在接聽模式下變更 [**SRModeID**](srmodeid-property.md) 來切換語音辨識引擎，則伺服器會切換至並啟動該引擎，而不會重新觸發 [**ListenStart**](listenstart-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-114">If the input-active client switches speech recognition engines by changing [**SRModeID**](srmodeid-property.md) while in Listening mode, the server switches to and activates that engine without re-triggering the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="333b3-115">但是，如果指定的引擎無法使用，呼叫就會失敗 (在控制項) 中引發錯誤，而且伺服器也會呼叫 [**ListenComplete**](listencomplete-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="333b3-115">However, if the specified engine is not available, the call fails (raises an error in the control) and the server also calls the [**ListenComplete**](listencomplete-event.md) event.</span></span>

 

 




