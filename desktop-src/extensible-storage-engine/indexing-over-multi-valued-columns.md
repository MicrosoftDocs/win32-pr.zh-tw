---
description: 深入瞭解：編制多值資料行的索引
title: 編制多值資料行的索引
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: aea24e8423b704b7e0345898bcb6ae4b6d7c057b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974545"
---
# <a name="indexing-over-multi-valued-columns"></a><span data-ttu-id="96e21-103">編制多值資料行的索引</span><span class="sxs-lookup"><span data-stu-id="96e21-103">Indexing over Multi-Valued Columns</span></span>


<span data-ttu-id="96e21-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="96e21-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-over-multi-valued-columns"></a><span data-ttu-id="96e21-105">編制多值資料行的索引</span><span class="sxs-lookup"><span data-stu-id="96e21-105">Indexing over Multi-Valued Columns</span></span>

<span data-ttu-id="96e21-106">多值資料行的索引只會對索引中的第一個多重值資料行執行。</span><span class="sxs-lookup"><span data-stu-id="96e21-106">Indexing over multi-valued columns is only performed over the first multi-valued column in the index.</span></span> <span data-ttu-id="96e21-107">第一個多重值資料行會展開，以便將資料行中的每個值編制索引。</span><span class="sxs-lookup"><span data-stu-id="96e21-107">The first multi-valued column is expanded so that every value in the column is indexed.</span></span> <span data-ttu-id="96e21-108">所有其他多重值資料行只會在資料行中的第一個值進行索引。</span><span class="sxs-lookup"><span data-stu-id="96e21-108">All other multi-valued columns are indexed only over the first value in the column.</span></span> <span data-ttu-id="96e21-109">例如，索引是在資料行 A 和資料行 B 上定義，而這兩個數據行都是多重值。</span><span class="sxs-lookup"><span data-stu-id="96e21-109">For example, an index is defined over Column A, and Column B, where both of these columns are multi-valued.</span></span> <span data-ttu-id="96e21-110">在給定的記錄中，資料行 A 的值為紅色、藍色，而資料行 B 的值為1、2和3。</span><span class="sxs-lookup"><span data-stu-id="96e21-110">In a given record, Column A has the values red, and blue, and Column B has the values 1, 2, and 3.</span></span> <span data-ttu-id="96e21-111">產生的索引會提供紅色-1 和藍1的專案。</span><span class="sxs-lookup"><span data-stu-id="96e21-111">The resulting index would give entries for red-1 and blue-1.</span></span> <span data-ttu-id="96e21-112">第二個數據行 B 的值則不會展開。</span><span class="sxs-lookup"><span data-stu-id="96e21-112">The values in the second column, Column B, are not expanded.</span></span> <span data-ttu-id="96e21-113">請注意，即使每個標記的資料行都可能是多重值的標記資料行（透過 JET_bitColumnMultiValued 明確標示為多重值），還是會以這種方式展開。</span><span class="sxs-lookup"><span data-stu-id="96e21-113">Note that even though every tagged column may be multi-valued only tagged columns that are explicitly flagged as multi-valued via JET_bitColumnMultiValued are expanded in this way.</span></span> <span data-ttu-id="96e21-114">此外，因為主要索引項目包含記錄，所以不允許在多重值資料行上具有主要索引，因為這樣會導致索引中的多個位置在記錄中必須存在。</span><span class="sxs-lookup"><span data-stu-id="96e21-114">Also, due to the fact that primary index entries contain records, it is not permitted to have a primary index over a multi-valued column because that would result in multiple locations in the index in which the record would have to reside.</span></span> <span data-ttu-id="96e21-115">如需詳細資訊，請參閱 [標記的、固定和變數資料行](./tagged-fixed-and-variable-columns.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="96e21-115">For more information, see the [Tagged, Fixed and Variable Columns](./tagged-fixed-and-variable-columns.md) topic.</span></span>

<span data-ttu-id="96e21-116">從 Windows Vista 開始，使用者可以選擇在使用 [JetCreateIndex](./jetcreateindex-function.md) 或 [JetCreateIndex2](./jetcreateindex2-function.md) 建立索引時，使用 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構來設定 JET_bitIndexCrossProduct 選項。</span><span class="sxs-lookup"><span data-stu-id="96e21-116">Starting in Windows Vista, users have the option to set the JET_bitIndexCrossProduct option when the index is created with [JetCreateIndex](./jetcreateindex-function.md) or [JetCreateIndex2](./jetcreateindex2-function.md) using the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span> <span data-ttu-id="96e21-117">在索引上設定此選項時，會展開索引中的所有多重值索引鍵資料行，並針對這些資料行中的每個值，在索引中建立交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="96e21-117">When this option is set on an index, all multi-valued key columns in the index are expanded, and a cross product is created in the index for every value in those columns.</span></span> <span data-ttu-id="96e21-118">上述範例現在會產生紅-1、red-2、red-3、blue-1、藍2、藍3的專案。</span><span class="sxs-lookup"><span data-stu-id="96e21-118">The example above now yields entries for red-1, red-2, red-3, blue-1, blue-2, blue-3.</span></span> <span data-ttu-id="96e21-119">同樣地，每個索引鍵資料行都必須明確宣告為多重值，才能透過 JET_bitColumnMultiValued 在索引中展開。</span><span class="sxs-lookup"><span data-stu-id="96e21-119">Again, each key column must be explicitly declared to be multi-valued via JET_bitColumnMultiValued to be expanded in the index.</span></span>
