---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374590"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="65df8-103">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="65df8-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="65df8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="65df8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="65df8-105">引擎必須透過 [**AudioStop**](https://www.bing.com/search?q=**AudioStop**)、 [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)和 [**視覺效果**](https://www.bing.com/search?q=**Visual**)來呼叫。</span><span class="sxs-lookup"><span data-stu-id="65df8-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="65df8-106">**視覺效果** 回呼必須提供 IPA 音素。</span><span class="sxs-lookup"><span data-stu-id="65df8-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="65df8-107"> (國際注音字母 \[ IPA \] 是一種通用的標記法，用來描述說話通訊的語音內容。</span><span class="sxs-lookup"><span data-stu-id="65df8-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="65df8-108">所有 speakable 音素在 IPA 中都有標記法。</span><span class="sxs-lookup"><span data-stu-id="65df8-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="65df8-109">IPA 的詳細資料位於語音 SDK 4.0 下載的 Microsoft 語音 API 規格 \[ 部分 \] [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) 。 ) </span><span class="sxs-lookup"><span data-stu-id="65df8-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="65df8-110">雖然 [**視覺效果**](https://www.bing.com/search?q=**Visual**) 通知相當豐富，但 Microsoft 代理程式只會使用 **cIPAPhoneme** 值，在字元說話時將嘴動畫。</span><span class="sxs-lookup"><span data-stu-id="65df8-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="65df8-111">任何 Microsoft 代理程式相容引擎都必須提供 **視覺** 通知的緊密同步處理串流，以反映所產生之語句的語音內容。</span><span class="sxs-lookup"><span data-stu-id="65df8-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="65df8-112">在這種情況下，「相對及時的通知」並不足夠，因為喇叭的 hearers 對於嘴位置和聲場內容之間的差異相當敏感。</span><span class="sxs-lookup"><span data-stu-id="65df8-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="65df8-113">**視覺效果** 通知必須立即傳回。</span><span class="sxs-lookup"><span data-stu-id="65df8-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




