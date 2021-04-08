---
title: 查詢的範圍
description: 查詢的範圍取決於您系結至的物件。
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- ADSI 的查詢範圍
- 查詢 ADSI、範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac51fc261cb418db0018acd996c248766896a25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671124"
---
# <a name="scope-of-query"></a><span data-ttu-id="d0522-105">查詢的範圍</span><span class="sxs-lookup"><span data-stu-id="d0522-105">Scope of Query</span></span>

<span data-ttu-id="d0522-106">查詢的範圍取決於您系結至的物件。</span><span class="sxs-lookup"><span data-stu-id="d0522-106">The scope of a query is determined by the object to which you bind.</span></span> <span data-ttu-id="d0522-107">如果您不確定物件在企業內的位置，您需要盡可能以最寬的方式進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="d0522-107">If you are unsure where the object is located within the enterprise then you will need to do as wide a search as possible.</span></span> <span data-ttu-id="d0522-108">但是，如果您知道物件將包含在特定網域內（例如，使用者所連接的網域，或特定群組（例如「經理」群組），則您應該設定搜尋範圍以反映此情況。</span><span class="sxs-lookup"><span data-stu-id="d0522-108">However, if you know that the object will be contained within a specific domain, such as the domain that the user is connected to, or within a specific group, such as the Managers group, then you should set the scope of the search to reflect the circumstance.</span></span> <span data-ttu-id="d0522-109">為了達到最佳效能，您應該嘗試將範圍設為目標，以搜尋可能的最小物件數目。</span><span class="sxs-lookup"><span data-stu-id="d0522-109">For the best performance, you should try to target the scope to search the smallest number of objects possible.</span></span>

<span data-ttu-id="d0522-110">當您不確定物件位於企業中的位置時，您可以系結至通用類別目錄服務。</span><span class="sxs-lookup"><span data-stu-id="d0522-110">When you are not sure where an object will be located in the enterprise, you can bind to the global catalog service.</span></span> <span data-ttu-id="d0522-111">通用類別目錄服務包含目錄中每個物件的清單，以及每個物件屬性的一小部分。</span><span class="sxs-lookup"><span data-stu-id="d0522-111">The global catalog service contains a list of every object in the directory and a small subset of each object's attributes.</span></span> <span data-ttu-id="d0522-112">在通用類別目錄中找到物件之後，您可以從通用類別目錄中取出它的辨別名稱，並使用它來系結至物件，以執行其他作業。</span><span class="sxs-lookup"><span data-stu-id="d0522-112">After you find the object in the global catalog, you can retrieve its distinguished name from the global catalog and use it to bind to the object to perform other operations.</span></span>

<span data-ttu-id="d0522-113">決定要系結的物件之後，您可以進一步將查詢限制為下列其中一個範圍：基底查詢、單一層級查詢或子樹搜尋，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d0522-113">After you decide which object to bind to, you can further restrict the query to one of the following scopes: a base query, a one-level query, or a subtree search, as shown in the following illustration.</span></span>

![在基底、一層或子樹搜尋的根目錄中的物件](images/netds6.png)

## <a name="base"></a><span data-ttu-id="d0522-115">基本</span><span class="sxs-lookup"><span data-stu-id="d0522-115">Base</span></span>

<span data-ttu-id="d0522-116">基底查詢會將搜尋限制為僅限基底物件。</span><span class="sxs-lookup"><span data-stu-id="d0522-116">A base query limits the search to only the base object.</span></span> <span data-ttu-id="d0522-117">傳回的物件數目上限一律為一個。</span><span class="sxs-lookup"><span data-stu-id="d0522-117">The maximum number of objects returned is always one.</span></span> <span data-ttu-id="d0522-118">您可以使用此搜尋來確認物件是否存在。</span><span class="sxs-lookup"><span data-stu-id="d0522-118">This search can be used to verify the existence of an object.</span></span> <span data-ttu-id="d0522-119">例如，如果您有物件的辨別名稱，而且必須根據路徑確認物件是否存在，您可以使用一層級的搜尋。</span><span class="sxs-lookup"><span data-stu-id="d0522-119">For example, if you have an object's distinguished name and you must verify the object's existence based on the path, you can use a one-level search.</span></span> <span data-ttu-id="d0522-120">如果搜尋失敗，您可以假設物件可能已重新命名或移至不同的位置，或您已獲得物件的不正確資料。</span><span class="sxs-lookup"><span data-stu-id="d0522-120">If the search fails, you can assume that the object may have been renamed or moved to a different location, or that you were given incorrect data about the object.</span></span> <span data-ttu-id="d0522-121">請注意，如果您想要重新流覽物件，您應該儲存 GUID，而不是分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="d0522-121">Be aware that you should store the GUID instead of the distinguished name if you want to revisit an object.</span></span> <span data-ttu-id="d0522-122">這允許在目錄階層中重新命名或移動物件，而不會中斷保存的連結。</span><span class="sxs-lookup"><span data-stu-id="d0522-122">This allows the object to be renamed or moved in the directory hierarchy without breaking the persisted link.</span></span>

## <a name="one-level"></a><span data-ttu-id="d0522-123">一層</span><span class="sxs-lookup"><span data-stu-id="d0522-123">One Level</span></span>

<span data-ttu-id="d0522-124">單一層級的搜尋僅限於基底物件的直屬子系，但會排除基底物件本身。</span><span class="sxs-lookup"><span data-stu-id="d0522-124">A one-level search is restricted to the immediate children of a base object, but excludes the base object itself.</span></span> <span data-ttu-id="d0522-125">這項設定可以針對父物件的直屬子物件，執行目標搜尋。</span><span class="sxs-lookup"><span data-stu-id="d0522-125">This setting can perform a targeted search for immediate child objects of a parent object.</span></span> <span data-ttu-id="d0522-126">例如，如果您有一個名為 P1 的父物件，且其直屬子系為： C1、C2、C3，則在單一層級搜尋中，評估準則時應包含 C1、C2 和 C3，但 P1 不是搜尋的一部分。</span><span class="sxs-lookup"><span data-stu-id="d0522-126">For example, if you have a parent object called P1, and its immediate children are: C1, C2, C3, then in a one-level search, C1, C2, and C3 should be included when evaluating the criteria, but P1 would not be part of the search.</span></span> <span data-ttu-id="d0522-127">您可以使用一層級的搜尋來列舉物件的所有子系。</span><span class="sxs-lookup"><span data-stu-id="d0522-127">A one-level search can be used to enumerate all children of an object.</span></span> <span data-ttu-id="d0522-128">事實上，在某些 ADSI 提供者中， [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 列舉會轉譯為一層級的搜尋。</span><span class="sxs-lookup"><span data-stu-id="d0522-128">In fact, in some ADSI providers, [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) enumeration translates to a one-level search.</span></span>

## <a name="subtree"></a><span data-ttu-id="d0522-129">樹狀子目錄</span><span class="sxs-lookup"><span data-stu-id="d0522-129">Subtree</span></span>

<span data-ttu-id="d0522-130">子樹搜尋（也稱為深層搜尋）包含基底物件下的所有物件，但基底物件本身除外。</span><span class="sxs-lookup"><span data-stu-id="d0522-130">A subtree search, also known as a deep search, includes all the objects beneath the base object, excluding the base object itself.</span></span> <span data-ttu-id="d0522-131">此搜尋可能會產生其他伺服器的參考。</span><span class="sxs-lookup"><span data-stu-id="d0522-131">This search may generate referrals to other servers.</span></span> <span data-ttu-id="d0522-132">此搜尋具有最大的範圍，而且可能會傳回大型結果集。</span><span class="sxs-lookup"><span data-stu-id="d0522-132">This search has the greatest scope and may return a large result set.</span></span> <span data-ttu-id="d0522-133">可能的話，請搜尋至少一個索引屬性，並設定 (的 [參考] 設定。如需詳細資訊，請參閱 [效能和處理大型結果集](performance-and-handling-large-result-sets.md)) 符合您的搜尋需求。</span><span class="sxs-lookup"><span data-stu-id="d0522-133">If possible, search on at least one indexed attribute and set the referrals settings (for more information, see [Performance and Handling Large Result Sets](performance-and-handling-large-result-sets.md)) to match your search requirements.</span></span> <span data-ttu-id="d0522-134">此外，也建議您以非同步方式執行子樹搜尋的結果，並將其分頁，以降低伺服器額外負荷和網路效能。</span><span class="sxs-lookup"><span data-stu-id="d0522-134">It is also suggested that the results of a subtree search be performed asynchronously and paged to reduce the server overhead and network effectiveness.</span></span> <span data-ttu-id="d0522-135">子樹搜尋通常用來搜尋指定範圍的物件。</span><span class="sxs-lookup"><span data-stu-id="d0522-135">A subtree search is normally used to search objects for a given scope.</span></span> <span data-ttu-id="d0522-136">例如，搜尋帳戶將于30天內到期的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="d0522-136">For example, search for all users with accounts that will expire in 30 days or less.</span></span>

 

 




