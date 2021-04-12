---
description: 說明如何使用輸入範圍來進行辨識。
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: 輸入範圍和 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195118"
---
# <a name="input-scopes-and-factoids"></a><span data-ttu-id="523b0-103">輸入範圍和 Factoids</span><span class="sxs-lookup"><span data-stu-id="523b0-103">Input Scopes and Factoids</span></span>

<span data-ttu-id="523b0-104">輸入範圍是一組已定義的單字、數位、標點符號和語法排序，可在指定的語言模型內使用。</span><span class="sxs-lookup"><span data-stu-id="523b0-104">An input scope is a defined set of words, numbers, punctuation, and syntactical orderings that are allowed within a given language model.</span></span> <span data-ttu-id="523b0-105">應用程式可以使用輸入範圍，將辨識器所使用的語言模型限制為特定的內容。</span><span class="sxs-lookup"><span data-stu-id="523b0-105">Input scopes can be used by applications to restrict the language model used by the recognizer to a specific context.</span></span> <span data-ttu-id="523b0-106">例如，的輸入範圍是 \_ 電子郵件 SMTPEMAILADDRESS 會藉 \_ 由指示特定欄位為電子郵件地址，來影響辨識結果。</span><span class="sxs-lookup"><span data-stu-id="523b0-106">For example, an input scope of IS\_EMAIL\_SMTPEMAILADDRESS influences the recognition results by indicating that a specific field is an email address.</span></span> <span data-ttu-id="523b0-107">因此，此欄位可能包含字元（例如 " @" and " \_ "），而且不能包含 " \* " 和空格等字元。</span><span class="sxs-lookup"><span data-stu-id="523b0-107">Thus, the field is likely to contain characters such as "@" and "\_", and it may not contain characters such as "\*" and spaces.</span></span>

> [!Note]  
> <span data-ttu-id="523b0-108">其他 Microsoft 技術也會使用輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="523b0-108">Other Microsoft technologies also use input scopes.</span></span> <span data-ttu-id="523b0-109">本文著重于使用內容來改善 Tablet PC 應用程式手寫辨識引擎的精確度。</span><span class="sxs-lookup"><span data-stu-id="523b0-109">This article focuses on using context to improve accuracy of handwriting recognition engines for Tablet PC applications.</span></span>

 

<span data-ttu-id="523b0-110">舊版 Tablet PC 技術 API 使用 factoids 來定義內容。</span><span class="sxs-lookup"><span data-stu-id="523b0-110">Previous versions of the Tablet PC Technology API used factoids to define context.</span></span> <span data-ttu-id="523b0-111">針對實際用途，模擬程式與輸入範圍的內容相同。</span><span class="sxs-lookup"><span data-stu-id="523b0-111">For practical purposes, a factoid is the same thing as an input scope.</span></span> <span data-ttu-id="523b0-112">第一個版本的 Tablet PC SDK 平臺定義了一 [**組智慧標籤物件中**](factoid-constants.md) 的一組模擬值。</span><span class="sxs-lookup"><span data-stu-id="523b0-112">Version one of the Tablet PC SDK platform defined a set of factoid values in the [**Factoid**](factoid-constants.md) object.</span></span> <span data-ttu-id="523b0-113">使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件進行辨識時，這些值可用來設定內容和影響辨識結果。</span><span class="sxs-lookup"><span data-stu-id="523b0-113">These values were used to set context and influence recognition results when using the [**RecognizerContext**](inkrecognizercontext-class.md) object for recognition.</span></span> <span data-ttu-id="523b0-114">針對從 Windows XP Tablet PC Edition 2005 開始的拉丁腳本辨識器，您仍然可以使用 **RecognizerCoNtext** 物件的 [[**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)] 屬性來設定內容，但您應該傳入輸入範圍、片語清單或手寫的正則運算式值，而不是其中一個版本的模擬值。</span><span class="sxs-lookup"><span data-stu-id="523b0-114">For recognizers of Latin script starting with Windows XP Tablet PC Edition 2005, you still use the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the **RecognizerContext** object to set context, but you should pass in an input scope, phrase list, or handwriting regular expression value instead of one of the version one factoid values.</span></span> <span data-ttu-id="523b0-115">東亞字元的 Microsoft 辨識器不支援使用輸入範圍的列舉值。</span><span class="sxs-lookup"><span data-stu-id="523b0-115">The Microsoft recognizers of East Asian characters do not support using the input scope enumerated values.</span></span> <span data-ttu-id="523b0-116">您應該繼續使用適用于東亞字元辨識器的模擬值。</span><span class="sxs-lookup"><span data-stu-id="523b0-116">You should continue to use factoid values for recognizers of East Asian characters.</span></span>

<span data-ttu-id="523b0-117">輸入範圍和 factoids 是文字層級替代項的限制;即使設定了 **強制** 旗標，字元替代字元也可能在指定的輸入範圍之外。</span><span class="sxs-lookup"><span data-stu-id="523b0-117">Input scopes and factoids are restrictions on the word level alternates; the character alternates may be outside the input scope specified even when the **COERCE** flag is set.</span></span>

<span data-ttu-id="523b0-118">當 **強制** 旗標設定了限制性的條件約束時，辨識器可能會產生兩個都符合筆墨的答案，並符合此條件約束。</span><span class="sxs-lookup"><span data-stu-id="523b0-118">When the **COERCE** flag is set with a restrictive factoid, it may happen that the recognizer cannot produce an answer that both matches the ink and satisfies the factoid.</span></span> <span data-ttu-id="523b0-119">辨識器的語言不符合筆墨的語言 (例如，美國英文辨識器和中文筆墨字元) 的另一個情況是，辨識器可能不會產生任何滿意的答案。</span><span class="sxs-lookup"><span data-stu-id="523b0-119">Another scenario where recognizer may not produce any satisfactory answer is when the language of the recognizer does not match the language of the ink (for example the US English recognizer and Chinese ink characters).</span></span>

<span data-ttu-id="523b0-120">當手寫辨識器無法辨識指定單字或字元的筆墨時，它可能會傳回空的替代清單或替代清單，其中第一個選擇是以程式碼點 0xffff (未定義的字元) 。</span><span class="sxs-lookup"><span data-stu-id="523b0-120">When the handwriting recognizer cannot recognize the ink for a given word or character, it may either return an empty alternate list or an alternate list where the first choice is code point 0xffff (undefined character).</span></span> <span data-ttu-id="523b0-121">這特別適用于盒裝的指南輸入模式，其中每個具有筆墨的方塊都預期會有非空白的替代清單。</span><span class="sxs-lookup"><span data-stu-id="523b0-121">This is especially useful in boxed guide input modes, where each box with ink is expected to have a non-empty list of alternates.</span></span> <span data-ttu-id="523b0-122">然後，應用程式就可以用它選擇的任何方式來顯示這個未定義的字元 (例如「???」) 。</span><span class="sxs-lookup"><span data-stu-id="523b0-122">The application can then display this undefined character in any manner it chooses (for example as "???").</span></span>

> [!Note]  
> <span data-ttu-id="523b0-123">針對回溯相容性，模擬程式值會繼續與拉丁腳本的辨識器搭配運作。</span><span class="sxs-lookup"><span data-stu-id="523b0-123">The factoid values continue to work with recognizers of Latin script for backward compatibility.</span></span>

 

<span data-ttu-id="523b0-124">如需 factoids 的詳細資訊，請參閱 [設定 Ink-Enabled 控制項的內容](setting-context-for-ink-enabled-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="523b0-124">For more information about factoids, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="523b0-125">如需東亞 factoids 的詳細資訊，請參閱 [第1版所支援的 factoids](supported-factoids-from-version-1.md)。</span><span class="sxs-lookup"><span data-stu-id="523b0-125">For information about East Asian factoids, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

 



