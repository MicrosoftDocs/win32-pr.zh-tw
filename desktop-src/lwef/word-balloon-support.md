---
title: 文字提示支援
description: 文字提示支援
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183268"
---
# <a name="word-balloon-support"></a><span data-ttu-id="23c36-103">文字提示支援</span><span class="sxs-lookup"><span data-stu-id="23c36-103">Word Balloon Support</span></span>

<span data-ttu-id="23c36-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="23c36-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="23c36-105">語音輸出也可以顯示成卡通單字球形的格式文字輸出。</span><span class="sxs-lookup"><span data-stu-id="23c36-105">Spoken output can also appear as textual output in the form of a cartoon word balloon.</span></span> <span data-ttu-id="23c36-106">這可以用來補充字元的語音輸出，或在您使用 [**說話**](speak-method.md) 方法時作為音訊輸出的替代方法。</span><span class="sxs-lookup"><span data-stu-id="23c36-106">This can be used to supplement the spoken output of a character or as an alternative to audio output when you use the [**Speak**](speak-method.md) method.</span></span>

![是主要字組氣球](images/f3ballon.gif)

<span data-ttu-id="23c36-108">您也可以使用「字提示字元」來傳達使用「 [**思考**](think-method.md) 」方法「思考」的字元。</span><span class="sxs-lookup"><span data-stu-id="23c36-108">You can also use a word balloon to communicate what a character is "thinking" using the [**Think**](think-method.md) method.</span></span> <span data-ttu-id="23c36-109">這會顯示您在仍然「想像」的氣球中提供的文字。</span><span class="sxs-lookup"><span data-stu-id="23c36-109">This displays the text you supply in a still "thought" balloon.</span></span> <span data-ttu-id="23c36-110">「 **思考** 」方法也與「 [**說話**](speak-method.md) 」方法不同，因為它不會產生任何音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="23c36-110">The **Think** method also differs from the [**Speak**](speak-method.md) method in that it produces no audio output.</span></span>

<span data-ttu-id="23c36-111">文字球標僅支援從字元（而不是使用者輸入）加上標題的通訊。</span><span class="sxs-lookup"><span data-stu-id="23c36-111">Word balloons support only captioned communication from the character, not user input.</span></span> <span data-ttu-id="23c36-112">因此，文字氣球不支援輸入控制項。</span><span class="sxs-lookup"><span data-stu-id="23c36-112">Therefore, the word balloon does not support input controls.</span></span> <span data-ttu-id="23c36-113">不過，您可以使用程式設計語言中的介面或 Microsoft Agent 提供的其他輸入服務（例如快顯功能表），輕鬆地為字元提供使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="23c36-113">However, you can easily provide user input for a character, using interfaces from your programming language or the other input services provided by Microsoft Agent, such as the pop-up menu.</span></span>

<span data-ttu-id="23c36-114">當您定義字元時，可以指定是否要包含文字提示支援。</span><span class="sxs-lookup"><span data-stu-id="23c36-114">When you define a character, you can specify whether to include word balloon support.</span></span> <span data-ttu-id="23c36-115">但是，如果您使用包含文字提示支援的字元，就無法停用支援。</span><span class="sxs-lookup"><span data-stu-id="23c36-115">However, if you use a character that includes word balloon support, you cannot disable the support.</span></span>

 

 




