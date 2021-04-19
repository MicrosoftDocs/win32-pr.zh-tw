---
description: 深入瞭解：搜尋索引中的記錄
title: 搜尋索引中的記錄
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971834"
---
# <a name="searching-records-in-the-index"></a><span data-ttu-id="70ced-103">搜尋索引中的記錄</span><span class="sxs-lookup"><span data-stu-id="70ced-103">Searching Records in the Index</span></span>


<span data-ttu-id="70ced-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="70ced-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="searching-records-in-the-index"></a><span data-ttu-id="70ced-105">搜尋索引中的記錄</span><span class="sxs-lookup"><span data-stu-id="70ced-105">Searching Records in the Index</span></span>

<span data-ttu-id="70ced-106">系統會建立搜尋索引鍵，以搜尋索引中的單一專案或一組專案。</span><span class="sxs-lookup"><span data-stu-id="70ced-106">Search keys are created to search for a single entry or a set of entries in an index.</span></span> <span data-ttu-id="70ced-107">搜尋索引鍵只能針對索引中的索引鍵資料行而建立，而且可能包含一或多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="70ced-107">Search keys may only be constructed for the key columns in the index, and may contain one or more column values.</span></span> <span data-ttu-id="70ced-108">搜尋索引鍵的建立方式為單一呼叫或一系列的 [JetMakeKey](./jetmakekey-function.md)呼叫，並且可使用 JET_bitRetrieveCopy 以 [JetRetrieveKey](./jetretrievekey-function.md) 抓取。</span><span class="sxs-lookup"><span data-stu-id="70ced-108">The search key is constructed with a single call or a series of calls to [JetMakeKey](./jetmakekey-function.md), and may be retrieved with [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy.</span></span> <span data-ttu-id="70ced-109">在建立搜尋索引鍵之後，您可以使用它將資料指標移至索引中的記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-109">After the search key is constructed it can be used to move the cursor to the record in the index.</span></span>

<span data-ttu-id="70ced-110">有三種方法可在資料表中尋找記錄：</span><span class="sxs-lookup"><span data-stu-id="70ced-110">There are three methods of finding records in a table:</span></span>

1.  <span data-ttu-id="70ced-111">搜尋單一索引項目。</span><span class="sxs-lookup"><span data-stu-id="70ced-111">Search for a single index entry.</span></span> <span data-ttu-id="70ced-112">若要這樣做，請使用 [JetMakeKey](./jetmakekey-function.md)建立搜尋金鑰，然後使用 [JetSeek](./jetseek-function.md)移至該記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-112">To do this, create the search key with [JetMakeKey](./jetmakekey-function.md), and then move to that record with [JetSeek](./jetseek-function.md).</span></span>

2.  <span data-ttu-id="70ced-113">依記錄搜尋索引記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-113">Search the index record-by-record.</span></span> <span data-ttu-id="70ced-114">您可以呼叫 [JetMove](./jetmove-function.md)，一次一筆記錄一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-114">Records can be traversed one record at a time by calling [JetMove](./jetmove-function.md).</span></span> <span data-ttu-id="70ced-115">您可以在 [JetMove](./jetmove-function.md)的 [*魚尾紋*] 參數中指定 JET_MoveFirst，將資料指標移至索引中的第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-115">The cursor can be moved to the first record in the index by specifying JET_MoveFirst in the *cRow* parameter of [JetMove](./jetmove-function.md).</span></span> <span data-ttu-id="70ced-116">同樣地，資料指標可以向前、向後或移至索引中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="70ced-116">In the same way, the cursor can be moved forward, backward, or to the last entry in the index.</span></span>

3.  <span data-ttu-id="70ced-117">搜尋一組記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-117">Search through a set of records.</span></span> <span data-ttu-id="70ced-118">若要這樣做，請設定要搜尋的索引項目範圍，然後依序移動記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-118">To do this, set a range of index entries to search, then move through the records sequentially.</span></span> <span data-ttu-id="70ced-119">For more information, see [Searching Through a Set of Records]() section of this topic.</span><span class="sxs-lookup"><span data-stu-id="70ced-119">For more information, see [Searching Through a Set of Records]() section of this topic.</span></span>

### <a name="searching-through-a-set-of-records"></a><span data-ttu-id="70ced-120">搜尋一組記錄</span><span class="sxs-lookup"><span data-stu-id="70ced-120">Searching Through a Set of Records</span></span>

<span data-ttu-id="70ced-121">這裡的圖表顯示資料指標，會在呼叫 [JetSeek](./jetseek-function.md) 和 [JetSetIndexRange](./jetsetindexrange-function.md)的呼叫所定義的索引項目範圍內移動。</span><span class="sxs-lookup"><span data-stu-id="70ced-121">The diagram here shows the cursor moving through a range of index entries defined by calls to [JetSeek](./jetseek-function.md) and [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="70ced-122">使用下列程式來搜尋索引中的一組記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-122">Use the following procedure to search through a set of records in an index.</span></span>

### <a name="to-search-a-set-of-records-in-an-index"></a><span data-ttu-id="70ced-123">搜尋索引中的一組記錄</span><span class="sxs-lookup"><span data-stu-id="70ced-123">To search a set of records in an index</span></span>

1.  <span data-ttu-id="70ced-124">針對要使用 [JetMakeKey](./jetmakekey-function.md)搜尋的記錄集內的第一筆記錄，建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="70ced-124">Create the search key for the first record in the set of records to be searched with [JetMakeKey](./jetmakekey-function.md).</span></span>

2.  <span data-ttu-id="70ced-125">使用 [JetSeek](./jetseek-function.md)將游標移至搜尋索引鍵中指定的記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-125">Move the cursor to the record indicated in the search key with [JetSeek](./jetseek-function.md).</span></span>

3.  <span data-ttu-id="70ced-126">使用 [JetMakeKey](./jetmakekey-function.md)為範圍中的最後一個索引項目建立另一個搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="70ced-126">Create another search key for the last index entry in the range with [JetMakeKey](./jetmakekey-function.md).</span></span>

4.  <span data-ttu-id="70ced-127">使用在步驟3中建立的索引鍵，設定 [JetSetIndexRange](./jetsetindexrange-function.md) 的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="70ced-127">Set the index range with [JetSetIndexRange](./jetsetindexrange-function.md) using the key created in step 3.</span></span>

5.  <span data-ttu-id="70ced-128">呼叫 [JetMove](./jetmove-function.md) 以依序在索引範圍中的每筆記錄移動，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="70ced-128">Call [JetMove](./jetmove-function.md) to move sequentially through each record in the index range as shown in the following diagram.</span></span>

<span data-ttu-id="70ced-129">![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")</span><span class="sxs-lookup"><span data-stu-id="70ced-129">![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")</span></span>

<span data-ttu-id="70ced-130">圖中的資料指標只能移動至 [JetSetIndexRange](./jetsetindexrange-function.md)呼叫中所設定的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="70ced-130">The cursor in the diagram here may only move through the range of indices set in the call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="70ced-131">如果應用程式嘗試將資料指標移到索引範圍之外，ESE 會從呼叫 [JetMove](./jetmove-function.md)傳回 Jet_errNoCurrentRecord 錯誤。</span><span class="sxs-lookup"><span data-stu-id="70ced-131">If the application attempts to move the cursor beyond the index range, ESE returns a Jet_errNoCurrentRecord error from the call to [JetMove](./jetmove-function.md).</span></span> <span data-ttu-id="70ced-132">請注意，除了移至下一個或上一個記錄之外，任何與此資料指標的導覽類型都會取消索引範圍。</span><span class="sxs-lookup"><span data-stu-id="70ced-132">Note that any type of navigation with this cursor other than moving to the next or previous record will cancel the index range.</span></span> <span data-ttu-id="70ced-133">如需詳細資訊，請參閱 [JetSetIndexRange](./jetsetindexrange-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="70ced-133">See [JetSetIndexRange](./jetsetindexrange-function.md) for more information.</span></span>

<span data-ttu-id="70ced-134">在 [JetMakeKey](./jetmakekey-function.md)的 *pvData* 參數中輸入的資料類型，必須符合針對資料行所指定的資料類型和屬性。</span><span class="sxs-lookup"><span data-stu-id="70ced-134">The type of data entered in the *pvData* parameter for [JetMakeKey](./jetmakekey-function.md) must match the type of data and properties specified for the column.</span></span> <span data-ttu-id="70ced-135">例如，在資料行 JET_coltypText 類型的 *pvData* 參數中指定 "Ben 莎莎" 來呼叫 [JetMakeKey](./jetmakekey-function.md)是有效的資料類型相符。</span><span class="sxs-lookup"><span data-stu-id="70ced-135">For example, calling [JetMakeKey](./jetmakekey-function.md) with "Ben Miller" specified in the *pvData* parameter for a column type JET_coltypText is a valid data type match.</span></span> <span data-ttu-id="70ced-136">如果您想要建立搜尋索引鍵，以在索引中的名稱 "Ben 莎莎" 和 "Max Stevens" 之間搜尋，請呼叫 [JetSeek](./jetseek-function.md)，將資料指標移至名稱為 "ben 莎莎" 的記錄。</span><span class="sxs-lookup"><span data-stu-id="70ced-136">If you want to create a search key to search between the names "Ben Miller" and "Max Stevens" in an index, move the cursor to the record with the name "Ben Miller" by calling [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="70ced-137">第二次呼叫 [JetMakeKey](./jetmakekey-function.md) ，並指定包含 "Max Stevens" 名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="70ced-137">Call [JetMakeKey](./jetmakekey-function.md) a second time and specify a pointer to a string containing the name "Max Stevens".</span></span> <span data-ttu-id="70ced-138">索引範圍設定為限制資料指標在呼叫 [JetSetIndexRange](./jetsetindexrange-function.md)時，于名稱 "Ben 莎莎" 和 "Max Stevens" 之間移動。</span><span class="sxs-lookup"><span data-stu-id="70ced-138">The index range is set to limit the cursor to move between the names "Ben Miller" and "Max Stevens" in the call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>
