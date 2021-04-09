---
title: 元組索引的運作方式
description: 元組索引是用來優化有0個或更多字串中間詞搜尋字串的搜尋，以及0或1個最終搜尋字串。 如果沒有任何一般索引可在該屬性上使用，它們也可以用來將初始搜尋字串的搜尋優化。
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- 元組索引編制
- 搜尋 Active Directory Active Directory，優化
- Active Directory，搜尋優化 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681654"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="a1b34-107">元組索引的運作方式</span><span class="sxs-lookup"><span data-stu-id="a1b34-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="a1b34-108">元組索引是用來優化有0個或更多 [字串中間詞搜尋字串](search-string-types.md) 的搜尋，以及0或1個最終搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="a1b34-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="a1b34-109">如果沒有任何一般索引可在該屬性上使用，它們也可以用來將初始搜尋字串的搜尋優化。</span><span class="sxs-lookup"><span data-stu-id="a1b34-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="a1b34-110">您可以在 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) 屬性中，設定與值32對應的 bit 5，來開啟屬性的元組索引編制。</span><span class="sxs-lookup"><span data-stu-id="a1b34-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="a1b34-111">這個屬性是在代表需要元組索引之屬性的架構物件中所設定。</span><span class="sxs-lookup"><span data-stu-id="a1b34-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="a1b34-112">開啟元組索引的效能影響，是針對該屬性所設定的任何字串值，將會擴充到元組索引中的大量片段。</span><span class="sxs-lookup"><span data-stu-id="a1b34-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="a1b34-113">當屬性展開時，它會在目錄資訊樹狀目錄中耗用較大量的磁碟空間，而且更新速度也會變慢。</span><span class="sxs-lookup"><span data-stu-id="a1b34-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="a1b34-114">元組索引是設計來加速搜尋表單 `*string*` 。</span><span class="sxs-lookup"><span data-stu-id="a1b34-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="a1b34-115">加速可能很大，因為這種形式的搜尋無法以任何其他方式進行優化，而且在其未優化的表單中，它會強制 Active Directory 伺服器在搜尋範圍中的每個物件上執行查詢。</span><span class="sxs-lookup"><span data-stu-id="a1b34-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="a1b34-116">因此，基底搜尋只會搜尋一個物件（這會使用較少的資源），而立即的子系搜尋則只會搜尋物件的子系， (可以使用較少的資源或更多資源（視容器) 大小而定），而子樹搜尋將會逐步解說基底物件下的整個子樹，因為子樹大小的關係</span><span class="sxs-lookup"><span data-stu-id="a1b34-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="a1b34-117">元組索引會藉由將字串分成 *元組* 來運作。</span><span class="sxs-lookup"><span data-stu-id="a1b34-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="a1b34-118">例如，字串 "Active Directory" 會分成下列元組：</span><span class="sxs-lookup"><span data-stu-id="a1b34-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="a1b34-119">當擴充元組索引的字串時，目錄將會在32767個字元停止。</span><span class="sxs-lookup"><span data-stu-id="a1b34-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="a1b34-120">元組索引會包含每一個元組的專案。</span><span class="sxs-lookup"><span data-stu-id="a1b34-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="a1b34-121">因此，如果使用者搜尋 `*cto*` ，Active Directory 伺服器將會在索引中尋找 "cto" 的所有相符專案，在此情況下，請尋找具有 (元組索引) 屬性值為 "Directory" 之記錄的指標。</span><span class="sxs-lookup"><span data-stu-id="a1b34-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="a1b34-122">如果 `*cto*` 上一個範例中 (的搜尋字串) 特定，則搜尋將會相當有效率，因為它可大幅減少 Active Directory 伺服器必須檢查以執行查詢的物件數目。</span><span class="sxs-lookup"><span data-stu-id="a1b34-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 