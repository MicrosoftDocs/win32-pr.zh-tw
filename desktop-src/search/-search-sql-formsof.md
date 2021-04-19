---
description: FORMSOF 字詞會使用單字的其他語言形式來執行符合專案。
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF 字詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000240"
---
# <a name="formsof-term"></a><span data-ttu-id="0cf74-103">FORMSOF 字詞</span><span class="sxs-lookup"><span data-stu-id="0cf74-103">FORMSOF Term</span></span>

<span data-ttu-id="0cf74-104">FORMSOF 字詞會使用單字的其他語言形式來執行符合專案。</span><span class="sxs-lookup"><span data-stu-id="0cf74-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="0cf74-105">以下是 FORMSOF 字詞語法：</span><span class="sxs-lookup"><span data-stu-id="0cf74-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="0cf74-106">世代類型會指定 Microsoft Windows Search 如何選擇替代字組表單。</span><span class="sxs-lookup"><span data-stu-id="0cf74-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="0cf74-107">**字形變化** 值會選擇相符字組的替代變化表單。</span><span class="sxs-lookup"><span data-stu-id="0cf74-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="0cf74-108">如果單字是動詞，則會使用替代時態。</span><span class="sxs-lookup"><span data-stu-id="0cf74-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="0cf74-109">如果單字是名詞，則會使用單數、複數和所有格形式來偵測相符專案。</span><span class="sxs-lookup"><span data-stu-id="0cf74-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="0cf74-110">Match \_ 單字值是一或多個單字，以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="0cf74-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="0cf74-111">範例</span><span class="sxs-lookup"><span data-stu-id="0cf74-111">Examples</span></span>

<span data-ttu-id="0cf74-112">下列範例會搜尋 "run" 這個字的字形變化相符專案。</span><span class="sxs-lookup"><span data-stu-id="0cf74-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="0cf74-113">此範例符合包含 "run"、"run" 或 "run" 的檔。</span><span class="sxs-lookup"><span data-stu-id="0cf74-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="0cf74-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cf74-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0cf74-115">**參考**</span><span class="sxs-lookup"><span data-stu-id="0cf74-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0cf74-116">FREETEXT 述詞</span><span class="sxs-lookup"><span data-stu-id="0cf74-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="0cf74-117">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="0cf74-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



