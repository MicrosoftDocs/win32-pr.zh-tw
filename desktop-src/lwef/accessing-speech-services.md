---
title: " (Microsoft 代理程式伺服器介面存取語音服務) "
description: 瞭解如何使用 Microsoft Agent 伺服器介面存取語音服務。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bf5cf88141344d5328592c9e823c7365c5d5
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262700"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a><span data-ttu-id="bd3c3-104"> (Microsoft 代理程式伺服器介面存取語音服務) </span><span class="sxs-lookup"><span data-stu-id="bd3c3-104">Accessing Speech Services (Microsoft Agent Server Interface)</span></span>

<span data-ttu-id="bd3c3-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bd3c3-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bd3c3-106">雖然 Microsoft 代理程式的服務包括對語音輸入的支援，但必須安裝相容的命令和控制語音辨識引擎，才能存取代理程式的語音輸入服務。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-106">Although Microsoft Agent's services include support for speech input, a compatible command-and-control speech recognition engine must be installed to access Agent's speech input services.</span></span> <span data-ttu-id="bd3c3-107">同樣地，如果您想要使用 Microsoft Agent 的語音服務來支援合成字元的合成語音輸出，您必須為您的字元安裝相容的文字轉換語音 (TTS) 語音引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-107">Similarly, if you want to use Microsoft Agent's speech services to support synthesized speech output for a character, you must install a compatible text-to-speech (TTS) speech engine for your character.</span></span> <span data-ttu-id="bd3c3-108">由於 Microsoft 代理程式的語音服務是以 Microsoft Speech API (SAPI) 為基礎，因此您可以使用相容性支援所需語音介面的任何引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-108">Because Microsoft Agent's speech services are based on the Microsoft Speech API (SAPI), you can use any engines that compatibly support the required speech interfaces.</span></span>

<span data-ttu-id="bd3c3-109">若要在您的應用程式中啟用語音輸入支援，請定義 [**命令**](https://www.bing.com/search?q=**Command**) 物件並設定其 [**Voice**](https://www.bing.com/search?q=**Voice**) 屬性。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-109">To enable speech input support in your application, define a [**Command**](https://www.bing.com/search?q=**Command**) object and set its [**Voice**](https://www.bing.com/search?q=**Voice**) property.</span></span> <span data-ttu-id="bd3c3-110">Microsoft Agent 會自動載入語音服務，因此當使用者按下接聽鍵或撥打 [**接聽**](https://www.bing.com/search?q=**Listen**)時，就會載入語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-110">Microsoft Agent will automatically load speech services, so that when the user presses the Listening key or you call [**Listen**](https://www.bing.com/search?q=**Listen**), the speech recognition engine will be loaded.</span></span> <span data-ttu-id="bd3c3-111">依預設，字元的語言識別項會決定要載入的引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-111">By default the character's language ID will determine which engine is loaded.</span></span> <span data-ttu-id="bd3c3-112">代理程式會嘗試載入由 SAPI 傳回的第一個引擎，使其符合此語言。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-112">Agent attempts to load the first engine that SAPI returns as matching this language.</span></span> <span data-ttu-id="bd3c3-113">如果您想要載入特定的引擎，請使用 **IAgentCharacterEx：： SetSRModeID** 。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-113">Use **IAgentCharacterEx::SetSRModeID** if you want to load a specific engine.</span></span>

<span data-ttu-id="bd3c3-114">若要啟用文字到語音轉換輸出，請使用「 [**說話**](https://www.bing.com/search?q=**Speak**) 」方法。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-114">To enable text-to-speech output, use the [**Speak**](https://www.bing.com/search?q=**Speak**) method.</span></span> <span data-ttu-id="bd3c3-115">Microsoft Agent 會自動嘗試載入符合字元語言識別項的引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-115">Microsoft Agent will automatically attempt to load an engine that matches the character's language ID.</span></span> <span data-ttu-id="bd3c3-116">如果字元的定義包含特定的 TTS 引擎模式識別碼，且該引擎可供使用且符合字元的語言識別項，則代理程式會為該字元載入該引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-116">If the character's definition includes a specific TTS engine mode ID and that engine is available and matches the character's language ID, Agent loads that engine for the character.</span></span> <span data-ttu-id="bd3c3-117">如果不是，Agent 會載入由 SAPI 傳回的第一個 TTS 引擎，以符合字元的語言設定。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-117">If not, Agent loads the first TTS engine that SAPI returns as matching the character's language setting.</span></span> <span data-ttu-id="bd3c3-118">您也可以使用 **IAgentCharacterEx：： SetTTSModeID** 載入特定的引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-118">You can also use **IAgentCharacterEx::SetTTSModeID** to load a specific engine.</span></span>

<span data-ttu-id="bd3c3-119">一般而言，Microsoft Agent 會在接聽模式起始時載入語音辨識引擎，並在第一次呼叫 [**說話**](https://www.bing.com/search?q=**Speak**) 時載入文字轉換語音引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-119">Typically, Microsoft Agent loads a speech recognition engine when the Listening mode is initiated and loads a text-to-speech engine when [**Speak**](https://www.bing.com/search?q=**Speak**) is first called.</span></span> <span data-ttu-id="bd3c3-120">但是，如果您想要預先載入語音引擎，您可以藉由查詢與語音介面相關的屬性來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-120">However, if you want to preload the speech engine, you can do this by querying the properties related to the speech interfaces.</span></span> <span data-ttu-id="bd3c3-121">例如，呼叫 **IAgentCharacterEx：： GetSRModeID** 或 **IAgentCharacterEx：： GetTTSModeID** 將會嘗試載入該類型的引擎。</span><span class="sxs-lookup"><span data-stu-id="bd3c3-121">For example, calling **IAgentCharacterEx::GetSRModeID** or **IAgentCharacterEx::GetTTSModeID** will attempt to load that type of engine.</span></span>

 

 




