---
description: Tablet PC 平臺支援數個 factoids，可用來增加辨識精確度。
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: 從版本1支援的 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976572"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="1cec1-103">從版本1支援的 Factoids</span><span class="sxs-lookup"><span data-stu-id="1cec1-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="1cec1-104">\[請注意， (SDK) 第1版的 Microsoft Windows XP Tablet PC Edition 軟體發展工具組中所支援的 factoids 描述，但建議您) 使用 [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) 列舉中所定義的值，以取得拉丁腳本的所有新開發 (。\]</span><span class="sxs-lookup"><span data-stu-id="1cec1-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="1cec1-105">Tablet PC 平臺支援數個 factoids，可用來增加辨識精確度。</span><span class="sxs-lookup"><span data-stu-id="1cec1-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="1cec1-106">使用 factoids 時，預期的輸入必須完全符合模擬程式的定義。</span><span class="sxs-lookup"><span data-stu-id="1cec1-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="1cec1-107">如果輸入不符合模擬程式的定義，辨識精確度就會受到影響。</span><span class="sxs-lookup"><span data-stu-id="1cec1-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="1cec1-108">例如，如果設定了 **數位** 的智慧標籤，而使用者輸入字母，則字母的辨識精確度很差。</span><span class="sxs-lookup"><span data-stu-id="1cec1-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="1cec1-109">某些 factoids （例如 **電子郵件** 和 **數位**）幾乎在各語言之間都完全相同。</span><span class="sxs-lookup"><span data-stu-id="1cec1-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="1cec1-110">其他 factoids，例如 **電話** 和 **郵遞區號**，會因語言而異。</span><span class="sxs-lookup"><span data-stu-id="1cec1-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="1cec1-111">檢查您所使用之語言的每個模擬程式格式。</span><span class="sxs-lookup"><span data-stu-id="1cec1-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="1cec1-112">您可以在本主題後面主題的表格中，找到每個語言中每個模擬的格式清單。</span><span class="sxs-lookup"><span data-stu-id="1cec1-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="1cec1-113">西方語言的 factoids 與東亞語言的 factoids 有些許但重要的區別。</span><span class="sxs-lookup"><span data-stu-id="1cec1-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="1cec1-114">適用于西方語言的 Factoids 是使用描述所需結果的運算式來執行。</span><span class="sxs-lookup"><span data-stu-id="1cec1-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="1cec1-115">辨識器接著會產生偏差，以產生符合此運算式的結果。</span><span class="sxs-lookup"><span data-stu-id="1cec1-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="1cec1-116">適用于東亞語言的 Factoids 是藉由指定可接受的 Unicode 字元範圍來執行。</span><span class="sxs-lookup"><span data-stu-id="1cec1-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="1cec1-117">例如，適用于東亞語言的 **日期** 陳述，在特定範圍內只接受 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="1cec1-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="1cec1-118">適用于西方語言的 Factoids 包含適用于英文的 Factoids (英國) 、英文 () 、法文、德文和西班牙文。</span><span class="sxs-lookup"><span data-stu-id="1cec1-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="1cec1-119">適用于東亞語言的 Factoids 包括 Factoids，適用于中文 (簡化) 、中文 (傳統) 、日文和韓文。</span><span class="sxs-lookup"><span data-stu-id="1cec1-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="1cec1-120">下列各節說明每種語言的每個模擬程式所支援的格式：</span><span class="sxs-lookup"><span data-stu-id="1cec1-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="1cec1-121">跨語言的通用 Factoids</span><span class="sxs-lookup"><span data-stu-id="1cec1-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="1cec1-122">適用于西方語言的 Factoids</span><span class="sxs-lookup"><span data-stu-id="1cec1-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="1cec1-123">適用于東亞語言的 Factoids</span><span class="sxs-lookup"><span data-stu-id="1cec1-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="1cec1-124">如果您預期輸入的輸入與這些章節的表格中所列的格式不同，請勿使用模擬。</span><span class="sxs-lookup"><span data-stu-id="1cec1-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="1cec1-125">此外，factoids 也內建于每種語言的辨識器中。</span><span class="sxs-lookup"><span data-stu-id="1cec1-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="1cec1-126">您無法從另一種語言的辨識器使用 factoids。</span><span class="sxs-lookup"><span data-stu-id="1cec1-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="1cec1-127">例如，您不能使用法文 **電話** 模擬的日文辨識器。</span><span class="sxs-lookup"><span data-stu-id="1cec1-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cec1-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="1cec1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cec1-129">**模擬常數**</span><span class="sxs-lookup"><span data-stu-id="1cec1-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="1cec1-130">[Microsoft 墨水瓶類別](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1cec1-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
