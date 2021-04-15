---
description: 深入瞭解：標記、固定和變數資料行
title: 標記、固定和變數資料行
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469021"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="0139c-103">標記、固定和變數資料行</span><span class="sxs-lookup"><span data-stu-id="0139c-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="0139c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0139c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="0139c-105">標記、固定和變數資料行</span><span class="sxs-lookup"><span data-stu-id="0139c-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="0139c-106">標記、固定和可變長度的資料行是 ESE 所支援的主要資料行類型。</span><span class="sxs-lookup"><span data-stu-id="0139c-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="0139c-107">標記的資料行不存在於記錄中，除非資料儲存在資料行中，而且可能是固定或可變長度。</span><span class="sxs-lookup"><span data-stu-id="0139c-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="0139c-108">標記的資料行也可以在單一記錄中包含一個以上的值。</span><span class="sxs-lookup"><span data-stu-id="0139c-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="0139c-109">固定資料行在每個資料列中都採用相同的空間量，且需要1個位來表示 Null 值。</span><span class="sxs-lookup"><span data-stu-id="0139c-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="0139c-110">變數長度資料行需要2個位元組來表示大小和 Null 值，而且會佔用每一筆記錄中的可變空間量。</span><span class="sxs-lookup"><span data-stu-id="0139c-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="0139c-111">如需已標記和固定資料行的詳細資訊，請參閱 Jet_bitColumnTagged，以及 [JetAddColumn](./jetaddcolumn-function.md)呼叫中所使用 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員中的 Jet_bitColumnFixed 選項。</span><span class="sxs-lookup"><span data-stu-id="0139c-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="0139c-112">可變長度的資料行是由 [JetAddColumn](./jetaddcolumn-function.md)呼叫中的 *coltyp* 參數所設定的資料行類型所決定。</span><span class="sxs-lookup"><span data-stu-id="0139c-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="0139c-113">根據是否已設定 Jet_bitColumnFixed 選項，下列資料行類型可以是固定或可變長度：</span><span class="sxs-lookup"><span data-stu-id="0139c-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="0139c-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="0139c-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="0139c-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="0139c-115">JET_coltypText</span></span>

  - <span data-ttu-id="0139c-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="0139c-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="0139c-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="0139c-117">JET_coltypLongText</span></span>

<span data-ttu-id="0139c-118">一般而言，記錄中的資料會先與固定範圍、變數範圍下一，以及最後儲存的標記範圍一起儲存。</span><span class="sxs-lookup"><span data-stu-id="0139c-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="0139c-119">下圖顯示如何將記錄儲存在資料表中。</span><span class="sxs-lookup"><span data-stu-id="0139c-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="0139c-120">如圖所示，標記的範圍可能包含具有多個值的資料行。</span><span class="sxs-lookup"><span data-stu-id="0139c-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="0139c-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="0139c-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
