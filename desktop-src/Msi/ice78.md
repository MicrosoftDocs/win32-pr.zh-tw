---
description: ICE78 會確認 AdvtUISequence 資料表不存在或空白。 這是必要的，因為在廣告期間不允許任何使用者介面。
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113852"
---
# <a name="ice78"></a><span data-ttu-id="d4cc0-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="d4cc0-104">ICE78</span></span>

<span data-ttu-id="d4cc0-105">ICE78 會確認 [AdvtUISequence 資料表](advtuisequence-table.md) 不存在或空白。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="d4cc0-106">這是必要的，因為在廣告期間不允許任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="d4cc0-107">結果</span><span class="sxs-lookup"><span data-stu-id="d4cc0-107">Result</span></span>

<span data-ttu-id="d4cc0-108">如果 AdvtUISequence 資料表存在且不是空的，ICE78 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="d4cc0-109">範例</span><span class="sxs-lookup"><span data-stu-id="d4cc0-109">Example</span></span>

<span data-ttu-id="d4cc0-110">ICE78 會報告此範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="d4cc0-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="d4cc0-111">在 AdvtUISequence 資料表中找到動作 ' Action1 '。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="d4cc0-112">在廣告期間不允許任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="d4cc0-113">因此，AdvtUISequence 資料表必須是空的或不存在。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="d4cc0-114">[AdvtUISequence 資料表](advtuisequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d4cc0-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="d4cc0-115">動作</span><span class="sxs-lookup"><span data-stu-id="d4cc0-115">Action</span></span>  | <span data-ttu-id="d4cc0-116">條件</span><span class="sxs-lookup"><span data-stu-id="d4cc0-116">Condition</span></span> | <span data-ttu-id="d4cc0-117">順序</span><span class="sxs-lookup"><span data-stu-id="d4cc0-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="d4cc0-118">Action1</span><span class="sxs-lookup"><span data-stu-id="d4cc0-118">Action1</span></span> | <span data-ttu-id="d4cc0-119">true</span><span class="sxs-lookup"><span data-stu-id="d4cc0-119">TRUE</span></span>      | <span data-ttu-id="d4cc0-120">1</span><span class="sxs-lookup"><span data-stu-id="d4cc0-120">1</span></span>        |



 

<span data-ttu-id="d4cc0-121">若要修正錯誤，請從資料表中移除 "Action1"，或移除資料表。</span><span class="sxs-lookup"><span data-stu-id="d4cc0-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4cc0-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4cc0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4cc0-123">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="d4cc0-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



