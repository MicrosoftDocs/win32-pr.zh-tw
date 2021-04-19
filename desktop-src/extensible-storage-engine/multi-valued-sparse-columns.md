---
description: 深入瞭解：多重值的稀疏資料行
title: 多重值的稀疏資料行
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996759"
---
# <a name="multi-valued-sparse-columns"></a><span data-ttu-id="bea86-103">多重值的稀疏資料行</span><span class="sxs-lookup"><span data-stu-id="bea86-103">Multi-Valued Sparse Columns</span></span>


<span data-ttu-id="bea86-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bea86-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="multi-valued-sparse-columns"></a><span data-ttu-id="bea86-105">多重值的稀疏資料行</span><span class="sxs-lookup"><span data-stu-id="bea86-105">Multi-Valued Sparse Columns</span></span>

<span data-ttu-id="bea86-106">稀疏資料行可以是固定或可變的長度，而且是唯一的，因為它們如果是 Null 或保留為預設值，就不會佔用記錄中的空間。</span><span class="sxs-lookup"><span data-stu-id="bea86-106">Sparse columns may be fixed or variable length, and are unique in that they do not take up space in a record if they are NULL or left to their default value.</span></span> <span data-ttu-id="bea86-107">稀疏資料行（也稱為標記資料行）可以在單一記錄中包含一個以上的值。</span><span class="sxs-lookup"><span data-stu-id="bea86-107">Sparse columns, also referred to as tagged columns, can contain more than one value in a single record.</span></span> <span data-ttu-id="bea86-108">標記的資料行可以是 [JET_coltyp](./jet-coltyp.md) 常數中所述的任何資料行類型。</span><span class="sxs-lookup"><span data-stu-id="bea86-108">Tagged columns can be any of the columns types described in the [JET_coltyp](./jet-coltyp.md) constants.</span></span> <span data-ttu-id="bea86-109">當您將資料行加入至資料表時，會在呼叫[JetAddColumn](./jetaddcolumn-function.md)的[JET_COLUMNDEF](./jet-columndef-structure.md)結構中設定 JET_bitColumnTagged 旗標，或在[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)或[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)的呼叫中使用的[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構中設定旗標，來建立資料行。</span><span class="sxs-lookup"><span data-stu-id="bea86-109">They are created when the column is added to the table by setting the JET_bitColumnTagged flag in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md), or in the [JET_COLUMNCREATE](./jet-columncreate-structure.md) structure used in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="bea86-110">JET_coltypLongText 和 JET_coltypLongBinary 類型的資料行會自動建立為已標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="bea86-110">Columns of type JET_coltypLongText and JET_coltypLongBinary are automatically created as tagged columns.</span></span>

<span data-ttu-id="bea86-111">只有標記的資料行可以在記錄中包含多個值，固定或可變長度的資料行可能不包含多個值。</span><span class="sxs-lookup"><span data-stu-id="bea86-111">Only tagged columns can contain multiple values in a record, fixed or variable length columns may not contain multiple values.</span></span> <span data-ttu-id="bea86-112">有兩種類型的多重值資料行：</span><span class="sxs-lookup"><span data-stu-id="bea86-112">There are two types of multi-valued columns:</span></span>

  - <span data-ttu-id="bea86-113">標記的資料行預設為多重值。</span><span class="sxs-lookup"><span data-stu-id="bea86-113">Tagged columns are multi-valued by default.</span></span> <span data-ttu-id="bea86-114">當第二個值加入至資料行時，它會自動變成多重值。</span><span class="sxs-lookup"><span data-stu-id="bea86-114">When a second value is added to the column, it automatically becomes multi-valued.</span></span>

  - <span data-ttu-id="bea86-115">在[JetAddColumn](./jetaddcolumn-function.md)的呼叫中，以[JET_COLUMNDEF](./jet-columndef-structure.md)結構中的 JET_bitColumnMultiValued 選項建立的標記資料行。</span><span class="sxs-lookup"><span data-stu-id="bea86-115">Tagged columns that are created with the JET_bitColumnMultiValued option in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="bea86-116">JET_bitColumnMultiValued 選項會變更資料行的索引方式。</span><span class="sxs-lookup"><span data-stu-id="bea86-116">The JET_bitColumnMultiValued option changes the way that the column is indexed.</span></span> <span data-ttu-id="bea86-117">具有 JET_bitColumnMultiValued 選項的多重值資料行，會比標記的多重值資料行更廣泛地進行索引。</span><span class="sxs-lookup"><span data-stu-id="bea86-117">Multi-valued columns with the JET_bitColumnMultiValued option are indexed more extensively than tagged multi-valued columns.</span></span> <span data-ttu-id="bea86-118">這些資料行會針對多重值資料行中的所有值編制索引，而標記的多重值資料行則只會針對多重值資料行中的第一個值編制索引。</span><span class="sxs-lookup"><span data-stu-id="bea86-118">These columns are indexed over all values in the multi-valued column, whereas tagged multi-valued columns are only indexed over the first value in the multi-valued column.</span></span> <span data-ttu-id="bea86-119">例如，假設有一個多重值資料行，其中 JET_bitColumnMultiValued 選項已設定，而且它是索引中的第一個多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="bea86-119">For example, consider a multi-valued column where the JET_bitColumnMultiValued option is set and it is the first multi-valued column in an index.</span></span> <span data-ttu-id="bea86-120">此資料行包含三個值： A、B 和 C。此資料行的索引包含所有三個值的專案： A、B 和 C。如果未設定 JET_bitColumnMultiValued 選項，則這個資料行上的索引只會包含索引中的第一個值（A）。</span><span class="sxs-lookup"><span data-stu-id="bea86-120">This column contains three values: A, B, and C. An index over this column contains entries for all three values, A, B, and C. If the JET_bitColumnMultiValued option was not set, the index over this column only contains the first value, A, in the index.</span></span>
