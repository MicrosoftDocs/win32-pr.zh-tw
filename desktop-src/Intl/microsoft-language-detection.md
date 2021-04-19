---
description: ELS 語言偵測服務稱為 Microsoft 語言偵測。 這項服務會使用 Microsoft 專利技術，讓應用程式能夠偵測撰寫特定文字的語言。
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft 語言偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974339"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="ad90a-104">Microsoft 語言偵測</span><span class="sxs-lookup"><span data-stu-id="ad90a-104">Microsoft Language Detection</span></span>

<span data-ttu-id="ad90a-105">ELS 語言偵測服務稱為 Microsoft 語言偵測。</span><span class="sxs-lookup"><span data-stu-id="ad90a-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="ad90a-106">這項服務會使用 Microsoft 專利技術，讓應用程式能夠偵測撰寫特定文字的語言。</span><span class="sxs-lookup"><span data-stu-id="ad90a-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="ad90a-107">輸入至 Microsoft 語言偵測</span><span class="sxs-lookup"><span data-stu-id="ad90a-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="ad90a-108">Microsoft 語言偵測服務的輸入為 UTF-16 (正規化格式的 C) 文字。</span><span class="sxs-lookup"><span data-stu-id="ad90a-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="ad90a-109">服務必須判斷此文字的語言。</span><span class="sxs-lookup"><span data-stu-id="ad90a-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="ad90a-110">Microsoft 語言偵測的輸出</span><span class="sxs-lookup"><span data-stu-id="ad90a-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="ad90a-111">Microsoft 語言偵測服務會抓取雙值終止、登錄格式的 UTF-16 字串清單（以其名稱表示），並以 null 字元分隔符號分隔。</span><span class="sxs-lookup"><span data-stu-id="ad90a-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="ad90a-112">清單會依相關性排序。</span><span class="sxs-lookup"><span data-stu-id="ad90a-112">The list is sorted by relevance.</span></span> <span data-ttu-id="ad90a-113">針對大部分的語言，則會使用中性名稱。</span><span class="sxs-lookup"><span data-stu-id="ad90a-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="ad90a-114">不過，在某些情況下（例如，Cyrl、sr-iov Latn、zh Zh-hant 和 zh Hans），則會使用完整名稱。</span><span class="sxs-lookup"><span data-stu-id="ad90a-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="ad90a-115">Microsoft 語言偵測操作</span><span class="sxs-lookup"><span data-stu-id="ad90a-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="ad90a-116">Microsoft 語言偵測服務會檢查應用程式所提供之文字的 Unicode 腳本。</span><span class="sxs-lookup"><span data-stu-id="ad90a-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="ad90a-117">它會根據所偵測到的腳本來分割文字，然後決定撰寫每個區段的語言。</span><span class="sxs-lookup"><span data-stu-id="ad90a-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="ad90a-118">如果腳本指出單一語言，語言的輸出清單中一定會有該語言。</span><span class="sxs-lookup"><span data-stu-id="ad90a-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="ad90a-119">此服務會使用專利演算法來判斷每個支援語言的相關性。</span><span class="sxs-lookup"><span data-stu-id="ad90a-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="ad90a-120">Microsoft 語言偵測 GUID</span><span class="sxs-lookup"><span data-stu-id="ad90a-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="ad90a-121">Microsoft 語言偵測服務的 GUID 是在 Elssrvc 中宣告，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="ad90a-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="ad90a-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad90a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad90a-123">關於擴充的語言服務</span><span class="sxs-lookup"><span data-stu-id="ad90a-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



