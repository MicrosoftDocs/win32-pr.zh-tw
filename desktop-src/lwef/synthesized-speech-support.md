---
title: 合成語音支援
description: 合成語音支援
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a89610a912cf601724bc9a2153cba8343e6feb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021423"
---
# <a name="synthesized-speech-support"></a><span data-ttu-id="b46bc-103">合成語音支援</span><span class="sxs-lookup"><span data-stu-id="b46bc-103">Synthesized Speech Support</span></span>

<span data-ttu-id="b46bc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b46bc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b46bc-105">如果您使用合成的語音，則您的字元可以說出幾乎所有的功能，以提供最大的彈性。</span><span class="sxs-lookup"><span data-stu-id="b46bc-105">If you use synthesized speech, your character has the ability to say almost anything, which provides the greatest flexibility.</span></span> <span data-ttu-id="b46bc-106">有了錄製的音訊之後，您可以為字元提供特定或唯一的聲音。</span><span class="sxs-lookup"><span data-stu-id="b46bc-106">With recorded audio, you can give the character a specific or unique voice.</span></span> <span data-ttu-id="b46bc-107">若要指定輸出，請將說出的文字提供為 [**說話**](speak-method.md) 方法的參數。</span><span class="sxs-lookup"><span data-stu-id="b46bc-107">To specify output, provide the spoken text as a parameter of the [**Speak**](speak-method.md) method.</span></span>

<span data-ttu-id="b46bc-108">因為 Microsoft 代理程式的架構使用 Microsoft SAPI 來進行合成語音輸出，所以您可以使用符合此規格的任何引擎，並支援使用 [**ITTSNotifySinkW**](ittsnotifysinkw.md)介面的 [**視覺**](https://www.bing.com/search?q=**Visual**)方法 (IPA) 輸出的國際注音字母。</span><span class="sxs-lookup"><span data-stu-id="b46bc-108">Because Microsoft Agent's architecture uses Microsoft SAPI for synthesized speech output, you can use any engine that conforms to this specification, and supports International Phonetic Alphabet (IPA) output using the [**Visual**](https://www.bing.com/search?q=**Visual**) method of the [**ITTSNotifySinkW**](ittsnotifysinkw.md) interface.</span></span> <span data-ttu-id="b46bc-109">如需有關引擎所需的詳細資訊，請參閱 [語音引擎支援需求](requirements-for-text-to-speech-engines.md)。</span><span class="sxs-lookup"><span data-stu-id="b46bc-109">For further information on the engine requires, see [Speech Engine Support Requirements](requirements-for-text-to-speech-engines.md).</span></span>

<span data-ttu-id="b46bc-110">字元的語言識別項設定會決定其 TTS 輸出。</span><span class="sxs-lookup"><span data-stu-id="b46bc-110">A character's language ID setting determines its TTS output.</span></span> <span data-ttu-id="b46bc-111">如果用戶端未指定字元的語言識別項，則字元的語言識別項會設定為使用者預設語言識別項。</span><span class="sxs-lookup"><span data-stu-id="b46bc-111">If a client does not specify a language ID for the character, the character's language ID is set to the user default language ID.</span></span> <span data-ttu-id="b46bc-112">如果字元的定義包含特定的引擎，而且可以載入該引擎並且符合字元的語言設定，則會使用該引擎。</span><span class="sxs-lookup"><span data-stu-id="b46bc-112">If the character's definition includes a specific engine and that engine can be loaded and it matches the character's language setting, that engine will be used.</span></span> <span data-ttu-id="b46bc-113">否則，Microsoft Agent 會列舉其他可用的引擎，並根據該順序中的語言、性別和年齡 (要求最符合的 SAPI) 。</span><span class="sxs-lookup"><span data-stu-id="b46bc-113">Otherwise, Microsoft Agent enumerates the other available engines and requests a SAPI best match based on language, gender, and age (in that order).</span></span> <span data-ttu-id="b46bc-114">如果沒有任何相符的引擎可供使用，就不會有該用戶端使用字元的 TTS 輸出。</span><span class="sxs-lookup"><span data-stu-id="b46bc-114">If there is no matching engine available, there is no TTS output for that client's use of the character.</span></span> <span data-ttu-id="b46bc-115">代理程式會嘗試在第一個 [**說話**](speak-method.md) 呼叫上載入 TTS 引擎，或在您查詢或成功設定其模式識別碼時載入。</span><span class="sxs-lookup"><span data-stu-id="b46bc-115">Agent attempts to load the TTS engine on the first [**Speak**](speak-method.md) call or when you query or successfully set its mode ID.</span></span>

<span data-ttu-id="b46bc-116">用戶端應用程式也可以使用 [**TTSModeID**](ttsmodeid-property.md) 屬性) ，指定其字元 (的 TTS 引擎。</span><span class="sxs-lookup"><span data-stu-id="b46bc-116">A client application can also specify a TTS engine for its character (using the [**TTSModeID**](ttsmodeid-property.md) property).</span></span> <span data-ttu-id="b46bc-117">這會覆寫伺服器嘗試根據字元慣用的 TTS 模式識別碼或字元的目前語言識別項設定，自動尋找相符的引擎。</span><span class="sxs-lookup"><span data-stu-id="b46bc-117">This overrides the server's attempt to automatically find a matching engine based on the character's preferred TTS mode ID or the character's current language ID setting.</span></span> <span data-ttu-id="b46bc-118">但是，如果該引擎未安裝 (或無法) 載入，則呼叫會失敗 (並在控制項) 中引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="b46bc-118">However, if that engine is not installed (or cannot otherwise be loaded), the call will fail (and raise an error in the control).</span></span> <span data-ttu-id="b46bc-119">然後伺服器會嘗試根據語言識別項、編譯的字元 TTS 設定和可用的 TTS 引擎載入另一個引擎。</span><span class="sxs-lookup"><span data-stu-id="b46bc-119">The server then attempts to load another engine based on the language ID, compiled character TTS setting, and available TTS engines.</span></span> <span data-ttu-id="b46bc-120">如果仍然沒有相符的情況，則不會提供 TTS 給該用戶端，但該字元仍然可以說出其字組氣球。</span><span class="sxs-lookup"><span data-stu-id="b46bc-120">If there is still no match, TTS is not available for that client, but the character can still speak into its word balloon.</span></span>

<span data-ttu-id="b46bc-121">只有任何用戶端所使用的 TTS 引擎仍會繼續載入。</span><span class="sxs-lookup"><span data-stu-id="b46bc-121">Only the TTS engines in use by any client remain loaded.</span></span> <span data-ttu-id="b46bc-122">例如，如果某個字元具有特定引擎的定義喜好設定，但該引擎可供使用，但您的用戶端應用程式已指定不同的引擎 (，方法是設定不同于引擎的字元語言識別項，或指定不同的模式識別碼) ，只有應用程式所指定的引擎會保持載入。</span><span class="sxs-lookup"><span data-stu-id="b46bc-122">For example, if a character has a defined preference for a specific engine and that engine is available, but your client application has specified a different engine (by setting a character's language ID differently from the engine or specifying a different mode ID), only the engine specified by your application remains loaded.</span></span> <span data-ttu-id="b46bc-123">除非有另一個用戶端使用字元的已編譯引擎設定) ，否則會卸載符合為 TTS 設定之字元定義喜好設定的引擎 (。</span><span class="sxs-lookup"><span data-stu-id="b46bc-123">The engine matching the character's defined preference for a TTS setting is unloaded (unless another client is using the character's compiled engine setting).</span></span>

 

 




