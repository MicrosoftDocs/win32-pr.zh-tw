---
title: 使用自然變化
description: 使用自然變化
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092233"
---
# <a name="use-natural-variation"></a><span data-ttu-id="737d4-103">使用自然變化</span><span class="sxs-lookup"><span data-stu-id="737d4-103">Use Natural Variation</span></span>

<span data-ttu-id="737d4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="737d4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="737d4-105">雖然應用程式的傳統介面（例如功能表和對話方塊）中的簡報一致性可讓介面更容易預測，但是會改變字元介面中的動畫和讀出的輸出。</span><span class="sxs-lookup"><span data-stu-id="737d4-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="737d4-106">適當地改變字元的回應可提供更自然的介面。</span><span class="sxs-lookup"><span data-stu-id="737d4-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="737d4-107">如果字元一律以相同的方式處理使用者;例如，一律說出相同的單字，使用者很可能會將人物視為乏味、disinterested 或甚至是。</span><span class="sxs-lookup"><span data-stu-id="737d4-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="737d4-108">人們通訊很少牽涉到精確的重複作業。</span><span class="sxs-lookup"><span data-stu-id="737d4-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="737d4-109">即使在類似的情況下重複某項功能，我們也可能變更用語、手勢或臉部運算式。</span><span class="sxs-lookup"><span data-stu-id="737d4-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="737d4-110">Microsoft 代理程式可讓您針對某個字元建立某種變化。</span><span class="sxs-lookup"><span data-stu-id="737d4-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="737d4-111">定義字元的動畫時，您可以在任何動畫框架上使用分支機率，以在動畫播放時變更動畫。</span><span class="sxs-lookup"><span data-stu-id="737d4-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="737d4-112">您也可以將多個動畫指派給每個狀態。</span><span class="sxs-lookup"><span data-stu-id="737d4-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="737d4-113">Microsoft Agent 會在每次啟動狀態時隨機播放其中一個指派的動畫。</span><span class="sxs-lookup"><span data-stu-id="737d4-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="737d4-114">針對語音輸出，您也可以在輸出文字中包含分隔號字元，以自動改變說出的文字。</span><span class="sxs-lookup"><span data-stu-id="737d4-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="737d4-115">例如，在處理此文字作為 [**說話**](speak-method.md) 方法的一部分時，Microsoft Agent 會隨機選取下列其中一個語句：</span><span class="sxs-lookup"><span data-stu-id="737d4-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="737d4-116">「我可以這麼說。 \|我可以說， \|我可以說其他東西」。</span><span class="sxs-lookup"><span data-stu-id="737d4-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 




