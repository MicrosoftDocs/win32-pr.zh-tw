---
description: 深入瞭解：多重值資料行中的排序
title: 多重值資料行中的排序
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571534"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="863fb-103">多重值資料行中的排序</span><span class="sxs-lookup"><span data-stu-id="863fb-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="863fb-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="863fb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="863fb-105">多重值資料行中的排序</span><span class="sxs-lookup"><span data-stu-id="863fb-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="863fb-106">多重值資料行中的值是由稱為 *itagSequence* 的索引編號來識別。</span><span class="sxs-lookup"><span data-stu-id="863fb-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="863fb-107">此數位是資料行單一值的參考。</span><span class="sxs-lookup"><span data-stu-id="863fb-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="863fb-108">當您在資料行中設定、抓取或列舉新值時，會使用這個數位。</span><span class="sxs-lookup"><span data-stu-id="863fb-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="863fb-109">*ItagSequence* 適用于各種結構，包括：</span><span class="sxs-lookup"><span data-stu-id="863fb-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="863fb-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="863fb-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="863fb-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="863fb-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="863fb-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="863fb-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="863fb-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="863fb-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="863fb-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="863fb-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="863fb-115">針對多重值資料行中的每個值，此 *itagSequence* 會從1開始。</span><span class="sxs-lookup"><span data-stu-id="863fb-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="863fb-116">當新的值加入至資料行時，序號會增加。</span><span class="sxs-lookup"><span data-stu-id="863fb-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="863fb-117">在 *itagSequence* 為0的資料行中設定值，表示值會附加至已經在該資料行中的值集合。</span><span class="sxs-lookup"><span data-stu-id="863fb-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="863fb-118">使用大於目前為數據行所設定之值數目的 *itagSequence* ，將會有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="863fb-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="863fb-119">指定現有值的 *itagSequence* 將會覆寫該值，而不是插入新值。</span><span class="sxs-lookup"><span data-stu-id="863fb-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="863fb-120">將現有的值設定為 Null，將會從已在該資料行中的值集合中移除該值。</span><span class="sxs-lookup"><span data-stu-id="863fb-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="863fb-121">這會將資料行中的所有後續值向下移動一個位置，讓 *itagSequence* 後續存取這些值的數位小於先前使用的數位。</span><span class="sxs-lookup"><span data-stu-id="863fb-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="863fb-122">下圖顯示多重值資料行中的 *itagSequence* 。</span><span class="sxs-lookup"><span data-stu-id="863fb-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="863fb-123">名為 ColA 的資料行有三個專案： Val1、Val2 和 Val3，分別 *itagSequence* 為1、2和3。</span><span class="sxs-lookup"><span data-stu-id="863fb-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="863fb-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="863fb-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
