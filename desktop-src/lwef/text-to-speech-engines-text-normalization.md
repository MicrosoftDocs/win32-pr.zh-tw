---
title: 文字轉換語音引擎文字正規化
description: 文字轉換語音引擎文字正規化
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965979"
---
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="2324d-103">文字轉換語音引擎文字正規化</span><span class="sxs-lookup"><span data-stu-id="2324d-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="2324d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2324d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="2324d-105">正規化是識別數位、縮寫、縮寫和 idiomatics，並視需要將它們轉換成全文檢索的程式（通常是根據句子的內容）。</span><span class="sxs-lookup"><span data-stu-id="2324d-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="2324d-106">例如，使用 L&H TruVoice 美式英文 TTS 引擎（句子：</span><span class="sxs-lookup"><span data-stu-id="2324d-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="2324d-107">1952年2月6日的王 George VI 壞掉。</span><span class="sxs-lookup"><span data-stu-id="2324d-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="2324d-108">將在 **正常內容** 下讀取，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2324d-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="2324d-109">19 52 年2月6日壞掉的王 George V</span><span class="sxs-lookup"><span data-stu-id="2324d-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="2324d-110">但是在 [ **電子郵件內容**] 下，它將會讀取如下：</span><span class="sxs-lookup"><span data-stu-id="2324d-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="2324d-111">王 George，壞掉于 19 52 年2月6日。</span><span class="sxs-lookup"><span data-stu-id="2324d-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="2324d-112">您可以在代理程式程式設計檔 [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md)中找到使用 **內容** 聲控標籤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2324d-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




