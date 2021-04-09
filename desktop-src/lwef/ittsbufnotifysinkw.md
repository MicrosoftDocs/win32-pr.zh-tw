---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932516"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="bbb1e-103">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="bbb1e-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="bbb1e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bbb1e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bbb1e-105">引擎必須透過 **書簽** 來呼叫。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="bbb1e-106">在語音輸出的前置處理期間，Microsoft 代理程式程式碼會在「單字」之間插入書簽，並使用這些書簽的抵達來推動文字球中的文字步調。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="bbb1e-107">雖然在語句結束之前，在一段時間內，不需要任何超過這些書簽的抵達，但必須以相當及時的方式傳回書簽，才能支援 Microsoft Agent。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="bbb1e-108">請注意，某些語言（例如日文）沒有 "word" 的嚴格概念。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="bbb1e-109">Microsoft 代理程式的「 [**說話**](speak-method.md) 」方法會將「單字」定義為已連接的符號字串，而這些符號的意義和發音都是隔離的。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="bbb1e-110">Microsoft Agent 會使用相當簡單的剖析程式碼來判斷「單字」是什麼：它會尋找以空白字元分隔的符號。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="bbb1e-111">因此，英文字串 "101 Dalmatians"： "a"、"101" 和 "Dalmatians" 中有三個「單字」。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="bbb1e-112">Microsoft Agent Map 標記中包含的文字會被視為單一「單字」以供顯示之用。</span><span class="sxs-lookup"><span data-stu-id="bbb1e-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




