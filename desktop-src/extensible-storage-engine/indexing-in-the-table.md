---
description: 深入瞭解：資料表中的索引編制
title: 資料表中的索引編制
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026343"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="af63b-103">資料表中的索引編制</span><span class="sxs-lookup"><span data-stu-id="af63b-103">Indexing in the Table</span></span>


<span data-ttu-id="af63b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="af63b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="af63b-105">資料表中的索引編制</span><span class="sxs-lookup"><span data-stu-id="af63b-105">Indexing in the Table</span></span>

<span data-ttu-id="af63b-106">索引是一組索引鍵資料行，可定義資料表中記錄的持續順序。</span><span class="sxs-lookup"><span data-stu-id="af63b-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="af63b-107">記錄是主要索引中的索引項目。</span><span class="sxs-lookup"><span data-stu-id="af63b-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="af63b-108">您可以定義一個主要索引和多個次要索引，以在資料表中建立不同的資料順序。</span><span class="sxs-lookup"><span data-stu-id="af63b-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="af63b-109">雖然可以定義多個索引，但記錄實際上是以主要索引所指定的順序儲存在 B + 樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="af63b-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="af63b-110">主要索引一律是叢集索引，而且也必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="af63b-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="af63b-111">主要索引必須在第一個資料表更新之前宣告，以保留索引順序。</span><span class="sxs-lookup"><span data-stu-id="af63b-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="af63b-112">當應用程式未定義任何主要索引時，資料會依照記錄新增至資料表的順序儲存。</span><span class="sxs-lookup"><span data-stu-id="af63b-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="af63b-113">這個特殊索引稱為「連續索引」。</span><span class="sxs-lookup"><span data-stu-id="af63b-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="af63b-114">不同的 B + 樹狀結構是用來根據次要索引來排序記錄。</span><span class="sxs-lookup"><span data-stu-id="af63b-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="af63b-115">次要索引中的索引項目會包含根據主要索引所儲存之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="af63b-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="af63b-116">主要索引中記錄的索引項目目必須是唯一的，因為次要索引會使用記錄的主鍵指向記錄。</span><span class="sxs-lookup"><span data-stu-id="af63b-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="af63b-117">次要索引不一定有唯一性條件約束。</span><span class="sxs-lookup"><span data-stu-id="af63b-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="af63b-118">如需詳細資訊，請參閱 [資料庫總覽](./database-overview.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="af63b-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
