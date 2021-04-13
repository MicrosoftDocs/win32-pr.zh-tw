---
title: Input-Active 用戶端
description: Input-Active 用戶端
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3223ddc7bb412b333d628f93cc56b27efd0abb7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301504"
---
# <a name="input-active-client"></a><span data-ttu-id="ff45f-103">Input-Active 用戶端</span><span class="sxs-lookup"><span data-stu-id="ff45f-103">Input-Active Client</span></span>

<span data-ttu-id="ff45f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ff45f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ff45f-105">因為多個用戶端應用程式可以共用相同的字元，而且因為多個用戶端可以同時使用不同的字元，所以伺服器會將一個用戶端指定為 *輸入主動* 用戶端，並只將滑鼠和語音輸入傳送至該用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff45f-105">Because multiple client applications can share the same character and because multiple clients can use different characters at the same time, the server designates one client as the *input-active* client and sends mouse and voice input only to that client application.</span></span> <span data-ttu-id="ff45f-106">這可維護使用者輸入的有條理管理，讓適當的用戶端回應輸入。</span><span class="sxs-lookup"><span data-stu-id="ff45f-106">This maintains the orderly management of user input, so that an appropriate client responds to the input.</span></span>

<span data-ttu-id="ff45f-107">一般而言，使用者互動會決定哪個用戶端應用程式會變成輸入主動。</span><span class="sxs-lookup"><span data-stu-id="ff45f-107">Typically, user interaction determines which client application becomes input-active.</span></span> <span data-ttu-id="ff45f-108">例如，如果使用者按一下某個字元，該字元的用戶端應用程式就會變成輸入-主動。</span><span class="sxs-lookup"><span data-stu-id="ff45f-108">For example, if the user clicks a character, that character's client application becomes input-active.</span></span> <span data-ttu-id="ff45f-109">同樣地，如果使用者說出字元的名稱，它就會變成輸入-主動。</span><span class="sxs-lookup"><span data-stu-id="ff45f-109">Similarly, if a user speaks the name of a character, it becomes input-active.</span></span> <span data-ttu-id="ff45f-110">此外，當伺服器處理字元的 [**Show**](show-method.md) 方法時，該字元的用戶端就會變成輸入-主動。</span><span class="sxs-lookup"><span data-stu-id="ff45f-110">Also, when the server processes a character's [**Show**](show-method.md) method, the client of that character becomes input-active.</span></span>

<span data-ttu-id="ff45f-111">隱藏字元時，該字元的用戶端將不再是該字元的輸入作用。</span><span class="sxs-lookup"><span data-stu-id="ff45f-111">When a character is hidden, the client of that character will no longer be input-active for that character.</span></span> <span data-ttu-id="ff45f-112">伺服器會自動讓任何剩餘字元 (的作用中用戶端) 輸入-主動。</span><span class="sxs-lookup"><span data-stu-id="ff45f-112">The server automatically makes the active client of any remaining character(s) input-active.</span></span> <span data-ttu-id="ff45f-113">當所有的字元都隱藏時，就不會有任何用戶端處於輸入作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="ff45f-113">When all characters are hidden, no client is input-active.</span></span> <span data-ttu-id="ff45f-114">不過，在這種情況下，如果使用者按下接聽的熱鍵，則代理程式會繼續接聽其命令 (使用符合最後一個輸入-主動用戶端) 最上層字元的語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="ff45f-114">However, in this situation, if the user presses the Listening hotkey, Agent will continue to listen for its commands (using the speech recognition engine matching the topmost character of the last input-active client).</span></span>

<span data-ttu-id="ff45f-115">如果有多個用戶端共用相同的字元，伺服器會將其作用中 *客戶* 端指定為輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="ff45f-115">If multiple clients are sharing the same character, the server will designate its *active client* as input-active client.</span></span> <span data-ttu-id="ff45f-116">現用字元是用戶端順序的最上層。</span><span class="sxs-lookup"><span data-stu-id="ff45f-116">The active character is the topmost in the client order.</span></span> <span data-ttu-id="ff45f-117">您可以使用 [**啟動**](activate-method.md) 方法將用戶端設定為作用中或非使用中的用戶端。</span><span class="sxs-lookup"><span data-stu-id="ff45f-117">You can set your client to be the active or not-active client using the [**Activate**](activate-method.md) method.</span></span> <span data-ttu-id="ff45f-118">您也可以使用 **啟動** 方法，明確地將用戶端輸入設為主動;但為了避免中斷其他用戶端的字元，您應該只在用戶端應用程式為使用中時才這樣做。</span><span class="sxs-lookup"><span data-stu-id="ff45f-118">You can also use the **Activate** method to explicitly make your client input-active; but to avoid disrupting other clients of the character, you should do so only when your client application is active.</span></span> <span data-ttu-id="ff45f-119">例如，如果使用者按一下應用程式的視窗，啟動您的應用程式，您可以呼叫 **Activate** 方法來接收和處理導向字元的滑鼠和語音輸入。</span><span class="sxs-lookup"><span data-stu-id="ff45f-119">For example, if the user clicks your application's window, activating your application, you can call the **Activate** method to receive and process mouse and speech input directed to the character.</span></span>

 

 




