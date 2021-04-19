---
description: 手寫辨識引擎（或辨識器）是處理筆墨並將筆墨轉換成文字的軟體。
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: 使用內容改善精確度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985603"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="db912-103">使用內容改善精確度</span><span class="sxs-lookup"><span data-stu-id="db912-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="db912-104">手寫辨識引擎（或辨識器）是處理筆墨並將筆墨轉換成文字的軟體。</span><span class="sxs-lookup"><span data-stu-id="db912-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="db912-105">內容是相關的應用程式特定資訊，您提供給辨識器以改善辨識精確度。</span><span class="sxs-lookup"><span data-stu-id="db912-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="db912-106">換句話說，內容是關於輸入的任何資訊片段，可協助辨識器正確處理欄位中的筆跡。</span><span class="sxs-lookup"><span data-stu-id="db912-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="db912-107">本節說明您可以利用 Tablet PC 應用程式中內容的不同方式，特別強調未啟用筆墨的應用程式的慣用程式設計技巧。</span><span class="sxs-lookup"><span data-stu-id="db912-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="db912-108">Windows Vista 軟體發展工具組的 Tablet PC 技術章節中有一些地方 (SDK) 在 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件和其 [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) 和 [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) 屬性方面使用「內容」一詞。</span><span class="sxs-lookup"><span data-stu-id="db912-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="db912-109">請勿將「內容」的其他使用方式與本節中的定義混淆。</span><span class="sxs-lookup"><span data-stu-id="db912-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 



