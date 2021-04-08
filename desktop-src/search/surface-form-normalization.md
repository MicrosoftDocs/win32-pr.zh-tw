---
description: 雖然單字和語言規則有很大的差異，但仍有一些考慮，例如數位、日期和時間，這些都是以一致的方式在所有斷詞工具中處理。
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: 表面形式正規化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b058be00e046ffc17ebd6c13178313267a47079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112372"
---
# <a name="surface-form-normalization"></a><span data-ttu-id="6a062-103">表面形式正規化</span><span class="sxs-lookup"><span data-stu-id="6a062-103">Surface Form Normalization</span></span>

<span data-ttu-id="6a062-104">雖然單字和語言規則有很大的差異，但仍有一些考慮，例如數位、日期和時間，這些都是以一致的方式在所有斷詞工具中處理。</span><span class="sxs-lookup"><span data-stu-id="6a062-104">Although words and linguistic rules differ dramatically, there are some considerations, such as numbers, dates, and times, that are handled consistently across all word breakers.</span></span> <span data-ttu-id="6a062-105">本主題記載可能影響斷詞工具執行的正規化考慮。</span><span class="sxs-lookup"><span data-stu-id="6a062-105">This topic documents normalization considerations that may affect your word breaker implementation.</span></span>

<span data-ttu-id="6a062-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="6a062-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6a062-107">功能</span><span class="sxs-lookup"><span data-stu-id="6a062-107">Hyphenation</span></span>](#hyphenation)
-   [<span data-ttu-id="6a062-108">所有格</span><span class="sxs-lookup"><span data-stu-id="6a062-108">Possessives</span></span>](#possessives)
-   [<span data-ttu-id="6a062-109">調</span><span class="sxs-lookup"><span data-stu-id="6a062-109">Diacritics</span></span>](#diacritics)
-   [<span data-ttu-id="6a062-110">Clitics</span><span class="sxs-lookup"><span data-stu-id="6a062-110">Clitics</span></span>](#clitics)

## <a name="hyphenation"></a><span data-ttu-id="6a062-111">功能</span><span class="sxs-lookup"><span data-stu-id="6a062-111">Hyphenation</span></span>

<span data-ttu-id="6a062-112">在複合單字或名稱的各部分之間使用連字號 (-) 。</span><span class="sxs-lookup"><span data-stu-id="6a062-112">Hyphens (-) are used between the parts of a compound word or name.</span></span> <span data-ttu-id="6a062-113">當單字在文字行的結尾時，也會在文字的音節之間使用它們。</span><span class="sxs-lookup"><span data-stu-id="6a062-113">They are also used between the syllables of a word when the word is divided at the end of a line of text.</span></span> <span data-ttu-id="6a062-114">在英文中，文字會與連字號聯結以表示內容中的特殊關聯性，但這些字組通常不會在其他內容中以連字號方式進行;例如，「逐步執行」。</span><span class="sxs-lookup"><span data-stu-id="6a062-114">In English, words are joined with hyphens to indicate a special relationship in context, but those words may not normally be hyphenated in other contexts; for example, "step-by-step."</span></span> <span data-ttu-id="6a062-115">在建立索引期間，斷詞工具應該將連字號視為單字分隔符號。</span><span class="sxs-lookup"><span data-stu-id="6a062-115">During index creation, the word breaker should treat the hyphen as a word separator.</span></span> <span data-ttu-id="6a062-116">例如，「資料基底」會儲存為「資料」和「基底」。</span><span class="sxs-lookup"><span data-stu-id="6a062-116">For example, "data-base" would be stored as "data" plus "base."</span></span> <span data-ttu-id="6a062-117">在查詢時，會以兩個替代專案取代帶字元的片語：兩個單字的變異和 true 複合。</span><span class="sxs-lookup"><span data-stu-id="6a062-117">At query time, a hyphenated phrase should be replaced with two alternatives: the two-word variant and the true compound.</span></span> <span data-ttu-id="6a062-118">例如，"data base" 會取代為 "data" 加上 "base" 和 "database"。</span><span class="sxs-lookup"><span data-stu-id="6a062-118">For example, "data-base" would be replaced by "data" plus "base" and "database."</span></span> <span data-ttu-id="6a062-119">索引和查詢時間之間的差異會增加以字元字元表示的字元組合，並可讓您在查詢中更容易符合文字。</span><span class="sxs-lookup"><span data-stu-id="6a062-119">This difference between index and query time increases the combinations of representations for hyphenated words and makes the words easier to match in a query.</span></span>

<span data-ttu-id="6a062-120">下表說明如何將連字號視為英文語言的文字分隔字元，將索引中包含的每個詞彙的相符查詢詞彙數目增加。</span><span class="sxs-lookup"><span data-stu-id="6a062-120">The following table shows how treating hyphens as word separators in the English language increases the number of matched query terms for each term included in the index.</span></span>



| <span data-ttu-id="6a062-121">索引中包含的詞彙</span><span class="sxs-lookup"><span data-stu-id="6a062-121">Terms included in the index</span></span> | <span data-ttu-id="6a062-122">查詢時間相符</span><span class="sxs-lookup"><span data-stu-id="6a062-122">Query-time matches</span></span>   |
|-----------------------------|----------------------|
| <span data-ttu-id="6a062-123">資料基底</span><span class="sxs-lookup"><span data-stu-id="6a062-123">Data base</span></span>                   | <span data-ttu-id="6a062-124">資料基底，資料基底</span><span class="sxs-lookup"><span data-stu-id="6a062-124">data base, data-base</span></span> |
| <span data-ttu-id="6a062-125">資料基底</span><span class="sxs-lookup"><span data-stu-id="6a062-125">Data-base</span></span>                   | <span data-ttu-id="6a062-126">資料基底，資料基底</span><span class="sxs-lookup"><span data-stu-id="6a062-126">data base, data-base</span></span> |
| <span data-ttu-id="6a062-127">資料庫</span><span class="sxs-lookup"><span data-stu-id="6a062-127">Database</span></span>                    | <span data-ttu-id="6a062-128">資料基底、資料庫</span><span class="sxs-lookup"><span data-stu-id="6a062-128">data-base, database</span></span>  |



 

## <a name="possessives"></a><span data-ttu-id="6a062-129">所有格</span><span class="sxs-lookup"><span data-stu-id="6a062-129">Possessives</span></span>

<span data-ttu-id="6a062-130">所有格是表示擁有權的名詞變化。</span><span class="sxs-lookup"><span data-stu-id="6a062-130">Possessives are variations in a noun that indicate possession.</span></span> <span data-ttu-id="6a062-131">英文所有格是藉由將單引號 ( ' ) 或單引號和 s ( 的) 附加到單字來表示。</span><span class="sxs-lookup"><span data-stu-id="6a062-131">English possessives are represented by appending an apostrophe (') or an apostrophe and an s ('s) to a word.</span></span> <span data-ttu-id="6a062-132">例如，若要表示擁有權，"Mary" 這個字會以 "Mary" 表示。</span><span class="sxs-lookup"><span data-stu-id="6a062-132">For example, to indicate possession, the word "Mary" is represented as "Mary's."</span></span> <span data-ttu-id="6a062-133">斷詞工具會在查詢時產生單引號和單引號形式的表單。</span><span class="sxs-lookup"><span data-stu-id="6a062-133">The word breaker generates both the apostrophe and the apostrophe-s forms at query time.</span></span> <span data-ttu-id="6a062-134">"Mary" 的查詢應該同時符合 "Mary" 和 "Mary"。</span><span class="sxs-lookup"><span data-stu-id="6a062-134">Queries for "Mary" should match both "Mary" and "Mary's."</span></span>

## <a name="diacritics"></a><span data-ttu-id="6a062-135">調</span><span class="sxs-lookup"><span data-stu-id="6a062-135">Diacritics</span></span>

<span data-ttu-id="6a062-136">將符號標記新增至字母或音素，以表示發音的特殊語音值。</span><span class="sxs-lookup"><span data-stu-id="6a062-136">Diacritics are marks added to a letter or phoneme to indicate a special phonetic value for pronunciation.</span></span> <span data-ttu-id="6a062-137">變音符號可以區分以圖形方式表示的單字;例如，英文的 "resume" 和 "resumé"。</span><span class="sxs-lookup"><span data-stu-id="6a062-137">Diacritics can distinguish words that are otherwise graphically identical; for example, "resume" and "resumé" in English.</span></span> <span data-ttu-id="6a062-138">但是，將字組儲存至索引會增加索引中唯一的單字索引鍵數目，進而降低查詢效能。</span><span class="sxs-lookup"><span data-stu-id="6a062-138">However, saving diacritics to the index increases the number of unique word keys in the index, which slows down query performance.</span></span> <span data-ttu-id="6a062-139">如果字組只在語言中使用，則該語言的斷詞工具應該在索引建立和查詢期間移除這些符號。</span><span class="sxs-lookup"><span data-stu-id="6a062-139">If diacritics are used only minimally in a language, the word breaker for that language should remove them during both index creation and querying.</span></span> <span data-ttu-id="6a062-140">例如，在處理「resumé」時，英文斷詞工具會產生「繼續」，只對查詢結果的相關性造成最大的影響。</span><span class="sxs-lookup"><span data-stu-id="6a062-140">For example, the English word breaker generates "resume" when processing "resumé," causing only minimal impact on the relevance of the query results.</span></span>

## <a name="clitics"></a><span data-ttu-id="6a062-141">Clitics</span><span class="sxs-lookup"><span data-stu-id="6a062-141">Clitics</span></span>

<span data-ttu-id="6a062-142">Clitic 是一種 unstressed 字，它本身不能獨立，並附加至壓力字以形成單一單位。</span><span class="sxs-lookup"><span data-stu-id="6a062-142">A clitic is an unstressed word that is incapable of standing on its own and attaches to a stressed word to form a single unit.</span></span> <span data-ttu-id="6a062-143">Clitics 無法輕易分類為 phonological、語法或形態。</span><span class="sxs-lookup"><span data-stu-id="6a062-143">Clitics cannot be easily classified as phonological, syntactic, or morphological.</span></span> <span data-ttu-id="6a062-144">Clitics 分為兩種類型： *proclitics* 和 *enclitics*。</span><span class="sxs-lookup"><span data-stu-id="6a062-144">Clitics come in two types: *proclitics* and *enclitics*.</span></span> <span data-ttu-id="6a062-145">Proclitics 會將自己附加到單字的開頭。</span><span class="sxs-lookup"><span data-stu-id="6a062-145">Proclitics attach themselves to the beginning of a word.</span></span> <span data-ttu-id="6a062-146">Enclitics 會將自己附加到單字的結尾。</span><span class="sxs-lookup"><span data-stu-id="6a062-146">Enclitics attach themselves to the end of a word.</span></span>

<span data-ttu-id="6a062-147">以西班牙文的語言剖析 Clitics 比較困難。</span><span class="sxs-lookup"><span data-stu-id="6a062-147">Clitics are more difficult to parse in languages such as Spanish.</span></span> <span data-ttu-id="6a062-148">根據時態，西班牙動詞命令可能會產生許多表面形式。</span><span class="sxs-lookup"><span data-stu-id="6a062-148">A Spanish verb may generate many surface forms, depending on the tense.</span></span> <span data-ttu-id="6a062-149">在建立索引期間移除 clitic，以及透過詞幹分析在查詢時產生介面表單之間，必須進行考慮。</span><span class="sxs-lookup"><span data-stu-id="6a062-149">Considerations must be made between removing the clitic during index creation and generating the surface forms through stemming at query time.</span></span> <span data-ttu-id="6a062-150">在 clitic 組合的 morphology 不明確的情況下移除 clitics，可能會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="6a062-150">Removing clitics in cases where the morphology of clitic composition is ambiguous can lead to unpredictable results.</span></span> <span data-ttu-id="6a062-151">為單字產生大量的表面形式會增加全文檢索索引的大小，而且可能會降低查詢效能。</span><span class="sxs-lookup"><span data-stu-id="6a062-151">Generating a large number of surface forms for a word increases the size of the full-text index and may slow down query performance.</span></span> <span data-ttu-id="6a062-152">建議您只產生少量的表面形式。</span><span class="sxs-lookup"><span data-stu-id="6a062-152">It is recommended that the stemmer generate only a small number of surface forms.</span></span>

 

 



