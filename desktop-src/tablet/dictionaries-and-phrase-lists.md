---
description: 特定辨識器的語言模型所使用的詞典或可能的單字清單包含在一或多個字典中。
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: 字典和片語清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984673"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="ad313-103">字典和片語清單</span><span class="sxs-lookup"><span data-stu-id="ad313-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="ad313-104">特定辨識器的語言模型所使用的詞典或可能的單字清單包含在一或多個字典中。</span><span class="sxs-lookup"><span data-stu-id="ad313-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="ad313-105">辨識器會在編譯辨識相符專案時搜尋系統上所有可用的字典。</span><span class="sxs-lookup"><span data-stu-id="ad313-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="ad313-106">您可以使用 Microsoft Speech Api (SAPI) 來修改部分字典。</span><span class="sxs-lookup"><span data-stu-id="ad313-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="ad313-107">片語清單提供另一種方式來修改辨識器的詞彙。</span><span class="sxs-lookup"><span data-stu-id="ad313-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="ad313-108">將文字新增至片語清單會延伸詞彙;新增文字，然後將辨識器限制為只使用片語清單 (而不是片語清單和字典) 限制詞彙。</span><span class="sxs-lookup"><span data-stu-id="ad313-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="ad313-109">舊版的 Tablet PC 技術 Api 依賴單字清單的概念。</span><span class="sxs-lookup"><span data-stu-id="ad313-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="ad313-110">單字清單與片語清單幾乎完全相同，而且在使用啟用筆墨的應用程式中直接使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件時，會使用相同的用途。</span><span class="sxs-lookup"><span data-stu-id="ad313-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="ad313-111">如需有關使用單字清單之位置和時機的詳細資訊，請參閱 [設定 Ink-Enabled 控制項的內容](setting-context-for-ink-enabled-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="ad313-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="ad313-112">當您要用來延伸詞典的清單大小超過100000個單字時，建議您使用字典，而不是使用單字清單或片語清單。</span><span class="sxs-lookup"><span data-stu-id="ad313-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



