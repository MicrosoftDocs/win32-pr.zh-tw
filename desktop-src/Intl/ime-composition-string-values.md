---
description: 這些值會搭配 ImmGetCompositionString 和 WM \_ IME \_ 組合使用。
ms.assetid: 14087598-8041-4e02-a168-f5538a437be0
title: IME 組合字元串值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5b3935329e56f015cdb08a764e1660142a067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848191"
---
# <a name="ime-composition-string-values"></a><span data-ttu-id="fa39a-103">IME 組合字元串值</span><span class="sxs-lookup"><span data-stu-id="fa39a-103">IME Composition String Values</span></span>

<span data-ttu-id="fa39a-104">這些值會搭配 [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) 和 [**WM \_ IME \_ 組合**](wm-ime-composition.md)使用。</span><span class="sxs-lookup"><span data-stu-id="fa39a-104">These values are used with [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) and [**WM\_IME\_COMPOSITION**](wm-ime-composition.md).</span></span>



| <span data-ttu-id="fa39a-105">值</span><span class="sxs-lookup"><span data-stu-id="fa39a-105">Value</span></span>                 | <span data-ttu-id="fa39a-106">描述</span><span class="sxs-lookup"><span data-stu-id="fa39a-106">Description</span></span>                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa39a-107">GC \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="fa39a-107">GCS\_COMPATTR</span></span>         | <span data-ttu-id="fa39a-108">取得或更新組合字元串的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa39a-108">Retrieve or update the attribute of the composition string.</span></span>                                |
| <span data-ttu-id="fa39a-109">GC \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="fa39a-109">GCS\_COMPCLAUSE</span></span>       | <span data-ttu-id="fa39a-110">取得或更新組合字元串的子句資訊。</span><span class="sxs-lookup"><span data-stu-id="fa39a-110">Retrieve or update clause information of the composition string.</span></span>                           |
| <span data-ttu-id="fa39a-111">GC \_ COMPREADATTR</span><span class="sxs-lookup"><span data-stu-id="fa39a-111">GCS\_COMPREADATTR</span></span>     | <span data-ttu-id="fa39a-112">取得或更新目前組合之讀取字串的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa39a-112">Retrieve or update the attributes of the reading string of the current composition.</span></span>        |
| <span data-ttu-id="fa39a-113">GC \_ COMPREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="fa39a-113">GCS\_COMPREADCLAUSE</span></span>   | <span data-ttu-id="fa39a-114">取得或更新撰寫字串之讀取字串的子句資訊。</span><span class="sxs-lookup"><span data-stu-id="fa39a-114">Retrieve or update the clause information of the reading string of the composition string.</span></span> |
| <span data-ttu-id="fa39a-115">GC \_ COMPREADSTR</span><span class="sxs-lookup"><span data-stu-id="fa39a-115">GCS\_COMPREADSTR</span></span>      | <span data-ttu-id="fa39a-116">取得或更新目前組合的讀取字串。</span><span class="sxs-lookup"><span data-stu-id="fa39a-116">Retrieve or update the reading string of the current composition.</span></span>                          |
| <span data-ttu-id="fa39a-117">GC \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="fa39a-117">GCS\_COMPSTR</span></span>          | <span data-ttu-id="fa39a-118">取出或更新目前的組合字元串。</span><span class="sxs-lookup"><span data-stu-id="fa39a-118">Retrieve or update the current composition string.</span></span>                                         |
| <span data-ttu-id="fa39a-119">GC \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="fa39a-119">GCS\_CURSORPOS</span></span>        | <span data-ttu-id="fa39a-120">取得或更新組合字元串中的游標位置。</span><span class="sxs-lookup"><span data-stu-id="fa39a-120">Retrieve or update the cursor position in composition string.</span></span>                              |
| <span data-ttu-id="fa39a-121">GC \_ DELTASTART</span><span class="sxs-lookup"><span data-stu-id="fa39a-121">GCS\_DELTASTART</span></span>       | <span data-ttu-id="fa39a-122">取得或更新組合字元串中任何變更的開始位置。</span><span class="sxs-lookup"><span data-stu-id="fa39a-122">Retrieve or update the starting position of any changes in composition string.</span></span>             |
| <span data-ttu-id="fa39a-123">GC \_ RESULTCLAUSE</span><span class="sxs-lookup"><span data-stu-id="fa39a-123">GCS\_RESULTCLAUSE</span></span>     | <span data-ttu-id="fa39a-124">取得或更新結果字串的子句資訊。</span><span class="sxs-lookup"><span data-stu-id="fa39a-124">Retrieve or update clause information of the result string.</span></span>                                |
| <span data-ttu-id="fa39a-125">GC \_ RESULTREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="fa39a-125">GCS\_RESULTREADCLAUSE</span></span> | <span data-ttu-id="fa39a-126">取得或更新讀取字串的子句資訊。</span><span class="sxs-lookup"><span data-stu-id="fa39a-126">Retrieve or update clause information of the reading string.</span></span>                               |
| <span data-ttu-id="fa39a-127">GC \_ RESULTREADSTR</span><span class="sxs-lookup"><span data-stu-id="fa39a-127">GCS\_RESULTREADSTR</span></span>    | <span data-ttu-id="fa39a-128">取出或更新讀取字串。</span><span class="sxs-lookup"><span data-stu-id="fa39a-128">Retrieve or update the reading string.</span></span>                                                     |
| <span data-ttu-id="fa39a-129">GC \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="fa39a-129">GCS\_RESULTSTR</span></span>        | <span data-ttu-id="fa39a-130">取得或更新組合結果的字串。</span><span class="sxs-lookup"><span data-stu-id="fa39a-130">Retrieve or update the string of the composition result.</span></span>                                   |



 

 

 



