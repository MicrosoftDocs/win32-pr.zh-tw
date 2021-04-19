---
description: 深入瞭解：版本、自動遞增和託管資料行
title: 版本、自動遞增和託管資料行
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974121"
---
# <a name="version-auto-increment-and-escrow-columns"></a><span data-ttu-id="b7a6d-103">版本、自動遞增和託管資料行</span><span class="sxs-lookup"><span data-stu-id="b7a6d-103">Version, Auto-Increment and Escrow Columns</span></span>


<span data-ttu-id="b7a6d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b7a6d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="version-auto-increment-and-escrow-columns"></a><span data-ttu-id="b7a6d-105">版本、自動遞增和託管資料行</span><span class="sxs-lookup"><span data-stu-id="b7a6d-105">Version, Auto-Increment and Escrow Columns</span></span>

<span data-ttu-id="b7a6d-106">ESE 提供具有特殊功能的版本、自動遞增及擁有的更新資料行類型。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-106">ESE provides version, auto-increment, and escrow update column types that have special abilities.</span></span> <span data-ttu-id="b7a6d-107">在 [JetAddColumn](./jetaddcolumn-function.md)呼叫中所使用 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員中設定的資料行選項，指出資料行是否為此處所述的其中一種特殊類型。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-107">The column options set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md) indicate whether the column is one of the specialized types noted here.</span></span>

### <a name="version-jet_bitcolumnversion"></a><span data-ttu-id="b7a6d-108">版本 (JET_bitColumnVersion) </span><span class="sxs-lookup"><span data-stu-id="b7a6d-108">Version (JET_bitColumnVersion)</span></span>

<span data-ttu-id="b7a6d-109">[版本資料行] 選項（僅適用于 JET_coltypLong 資料行）表示資料行包含記錄的版本資訊，可用來判斷是否需要重新整理指定記錄的記憶體中複本。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-109">The version column option, applied only to JET_coltypLong columns, indicates that the column contains version information about the record that can be used to determine if an in-memory copy of a given record needs to be refreshed.</span></span> <span data-ttu-id="b7a6d-110">當應用程式透過 [JetUpdate](./jetupdate-function.md)修改資料行時，ESE 會自動遞增版本資料行。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-110">Version columns are automatically incremented by ESE when the column is modified by the application via [JetUpdate](./jetupdate-function.md).</span></span>

### <a name="auto-increment-jet_bitcolumnautoincrement"></a><span data-ttu-id="b7a6d-111">自動遞增 (JET_bitColumnAutoincrement) </span><span class="sxs-lookup"><span data-stu-id="b7a6d-111">Auto-Increment (JET_bitColumnAutoincrement)</span></span>

<span data-ttu-id="b7a6d-112">當新的記錄插入資料表時，自動遞增資料行會自動由 ESE 遞增。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-112">Auto increment columns are automatically incremented by ESE when a new record is inserted into the table.</span></span> <span data-ttu-id="b7a6d-113">自動遞增資料行中包含的值對資料表中的每一筆記錄而言是唯一的，而且不保證是連續的。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-113">The value contained in the auto-increment column is unique for every record in the table and is not guaranteed to be continuous.</span></span> <span data-ttu-id="b7a6d-114">這些值不會回收，但在某些情況下可以重複使用。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-114">These values are not recycled, but can be reused in certain cases.</span></span> <span data-ttu-id="b7a6d-115">只有 JET_coltypLong 和 JET_coltypLongLong 類型的資料行可以是自動遞增資料行。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-115">Only columns of type JET_coltypLong and JET_coltypLongLong may be auto increment columns.</span></span>

### <a name="escrow-jet_bitcolumnescrowupdate"></a><span data-ttu-id="b7a6d-116">JET_bitColumnEscrowUpdate) 的 (</span><span class="sxs-lookup"><span data-stu-id="b7a6d-116">Escrow (JET_bitColumnEscrowUpdate)</span></span>

<span data-ttu-id="b7a6d-117">您可以在 [JetEscrowUpdate](./jetescrowupdate-function.md)的呼叫中修改可修改的「託管」資料行。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-117">Escrow columns can be modified in the call to [JetEscrowUpdate](./jetescrowupdate-function.md).</span></span> <span data-ttu-id="b7a6d-118">進行中的更新是不會受到寫入衝突影響的數值差異作業。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-118">Updates in escrow are numeric delta operations that do not suffer from write conflicts.</span></span> <span data-ttu-id="b7a6d-119">這表示，任何數目的會話都可以透過 [JetEscrowUpdate](./jetescrowupdate-function.md) 並行更新記錄中的已系建資料行，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-119">What this means is that any number of sessions can concurrently update an escrow column in a record via [JetEscrowUpdate](./jetescrowupdate-function.md) without conflicts.</span></span> <span data-ttu-id="b7a6d-120">請注意，任何其他更新作業可能仍會導致與進行中的更新作業發生寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-120">Note that any other update operation may still result in a write conflict with an escrow update operation.</span></span> <span data-ttu-id="b7a6d-121">您只能對具有預設值 JET_coltypLong 類型的資料行進行保管更新。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-121">Escrow updates can only be made to columns of type JET_coltypLong that have a default value.</span></span> <span data-ttu-id="b7a6d-122">您也必須先將這些資料行加入至資料表，然後再載入資料列。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-122">These columns must also be added to a table before it is loaded with rows.</span></span> <span data-ttu-id="b7a6d-123">最後，包含「已建立」更新資料行的資料列可能會設定為支援「資料列完成」回呼 (JET_bitColumnFinalize) 或在參考計數達到零 (JET_bitColumnDeleteOnZero) 時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-123">Finally, rows containing an escrow update column may be configured to support a row finalization callback (JET_bitColumnFinalize) or to be automatically deleted if the ref count reaches zero (JET_bitColumnDeleteOnZero).</span></span> <span data-ttu-id="b7a6d-124">如需詳細資訊，請參閱 [JET_COLUMNDEF](./jet-columndef-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="b7a6d-124">For more information, see the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>
