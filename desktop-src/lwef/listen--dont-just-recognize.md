---
title: 聆聽，不只是辨識
description: 聆聽，不只是辨識
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e972a8c98460e58d0f7080d7de7641fb856c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675448"
---
# <a name="listen-dont-just-recognize"></a><span data-ttu-id="b1cc1-103">聆聽，不只是辨識</span><span class="sxs-lookup"><span data-stu-id="b1cc1-103">Listen, Dont Just Recognize</span></span>

<span data-ttu-id="b1cc1-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b1cc1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b1cc1-105">成功的通訊牽涉到比字詞更多的識別。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-105">Successful communication involves more than recognition of words.</span></span> <span data-ttu-id="b1cc1-106">對話的程式意指交換提示，以指示輪流學習和理解。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-106">The process of dialogue implies exchanging cues to signal turn-taking and understanding.</span></span> <span data-ttu-id="b1cc1-107">字元可以藉由提供提示（如 head 傾斜、節點或訪談）來指出語音引擎處於接聽狀態的時間，以及辨識某個物件時，可以改善對話介面。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-107">Characters can improve conversational interfaces by providing cues like head tilts, nods, or shakes to indicate when the speech engine is in the listening state and when something is recognized.</span></span> <span data-ttu-id="b1cc1-108">例如，當使用者在偵測到語句時，當使用者按下對話接聽按鍵和指派給 **聽力** 狀態的動畫時，Microsoft Agent 會播放指派給 **接聽** 狀態的動畫。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-108">For example, Microsoft Agent plays animations assigned to the **Listening** state when a user presses the push-to-talk listening key and animations assigned to the **Hearing** state when an utterance is detected.</span></span> <span data-ttu-id="b1cc1-109">定義您自己的字元時，請務必建立適當的動畫並指派給這些狀態。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-109">When defining your own character, make sure you create and assign appropriate animations to these states.</span></span> <span data-ttu-id="b1cc1-110">如需設計字元的詳細資訊，請參閱 [設計 Microsoft Agent 的字元](designing-characters-for-microsoft-agent.md)。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-110">For more information on designing characters, see [Designing Characters for Microsoft Agent](designing-characters-for-microsoft-agent.md).</span></span>

<span data-ttu-id="b1cc1-111">除了非口頭提示之外，交談也牽涉到交談方之間的一般內容。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-111">In addition to non-verbal cues, a conversation involves a common context between the conversing parties.</span></span> <span data-ttu-id="b1cc1-112">同樣地，具有字元的語音輸入案例更可能在正確建立內容時成功。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-112">Similarly, speech input scenarios with characters are more likely to succeed when the context is well established.</span></span> <span data-ttu-id="b1cc1-113">建立內容可讓您更清楚地解讀類似發音的片語，例如「簽入郵件」和「檢查我的郵件」。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-113">Establishing the context enables you to better interpret similar-sounding phrases like "check's in the mail" and "check my mail."</span></span> <span data-ttu-id="b1cc1-114">您也可以藉由重申目前的內容（例如，您的應用程式所執行的最後一個動作），讓使用者能夠查詢內容，方法是提供命令（例如「說明」或「我的位置」）。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-114">You may also want to enable the user to query the context by providing a command, such as "Help" or "Where am I," to which you respond by restating the current context, such as the last action your application performed.</span></span>

<span data-ttu-id="b1cc1-115">Microsoft Agent 提供的介面可讓您存取最符合的專案，以及語音辨識引擎所傳回的兩個最佳替代方案。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-115">Microsoft Agent provides interfaces that enable you access the best match and the two next best alternatives returned by the speech recognition engine.</span></span> <span data-ttu-id="b1cc1-116">此外，您可以存取所有相符專案的信賴分數。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-116">In addition, you can access confidence scores for all matches.</span></span> <span data-ttu-id="b1cc1-117">您可以使用此資訊來更清楚地判斷所說的內容。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-117">You can use this information to better determine what was spoken.</span></span> <span data-ttu-id="b1cc1-118">例如，如果最符合專案的信賴分數和第一個替代專案是關閉的，則可能表示語音引擎在辨識兩者之間的差異時遇到問題。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-118">For example, if the confidence scores of the best match and first alternative are close, it may indicate that the speech engine had difficulty discerning the difference between them.</span></span> <span data-ttu-id="b1cc1-119">在這種情況下，您可能會想要要求使用者重複或重新表述要求，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-119">In such a case, you may want to ask the user to repeat or rephrase the request in an effort to improve performance.</span></span> <span data-ttu-id="b1cc1-120">但是，如果最符合專案和第一個或第二個替代方案傳回相同的命令，它就會增強正確辨識的指示。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-120">However, if the best match and first or second alternatives return the same command, it strengthens the indication of the correct recognition.</span></span>

<span data-ttu-id="b1cc1-121">交談或對話的本質暗示應該要有語音輸入的回應。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-121">The nature of a conversation or dialogue implies that there should be a response to spoken input.</span></span> <span data-ttu-id="b1cc1-122">因此，使用者的輸入應該一律使用指出已執行動作或遇到問題的口頭或視覺回饋來回應，或提供適當的回復。</span><span class="sxs-lookup"><span data-stu-id="b1cc1-122">Therefore, a user's input should always be responded to with verbal or visual feedback that indicates an action was performed or a problem was encountered, or provides an appropriate reply.</span></span>

 

 




