---
description: 模式比對篩選準則會通知驅動程式，接受特定位移具有特定模式的框架。
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: 撰寫 PATTERNMATCH 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993084"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="0ebe0-103">撰寫 PATTERNMATCH 篩選</span><span class="sxs-lookup"><span data-stu-id="0ebe0-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="0ebe0-104">模式比對篩選準則會通知驅動程式，接受特定位移具有特定模式的框架。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="0ebe0-105">您可以指定最多四個詳細的模式比對，可以在網路監視器驅動程式評估的邏輯 AND 或語句中結合。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="0ebe0-106">若要執行模式比對，請使用下列網路監視器結構：</span><span class="sxs-lookup"><span data-stu-id="0ebe0-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="0ebe0-107">**表達**</span><span class="sxs-lookup"><span data-stu-id="0ebe0-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="0ebe0-108">**ANDEXP**</span><span class="sxs-lookup"><span data-stu-id="0ebe0-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="0ebe0-109">**PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="0ebe0-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="0ebe0-110">若要評估 **或** 語句，請結合二到四種模式，以符合 [**ANDEXP**](andexp.md)結構 (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3) 。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="0ebe0-111">若要評估和語句，請將一到四個 **ANDEXP** 結構和 [**運算式**](expression.md) 結構結合 (AndExp1 && AndExp2) 。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="0ebe0-112">模式比對定義</span><span class="sxs-lookup"><span data-stu-id="0ebe0-112">Pattern Match Definitions</span></span>

<span data-ttu-id="0ebe0-113">單一模式比對是由 [**PATTERNMATCH**](patternmatch.md) 結構所定義。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="0ebe0-114">個別的相符可以用兩種方式之一來運作。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="0ebe0-115">一般來說，驅動程式會採用位移基礎 (可以是相對於框架的位移、相對於有效通訊協定的位移基準、相對於 IPX 的相對於 IPX 的位移，或是相對於 IP) 的位移基礎， \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 然後開始計算。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="0ebe0-116">驅動程式將會從該處計算位移位元組，然後比對所找到的資料與 **PatternToMatch** 中的第一個長度位元組。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="0ebe0-117">如果兩者相同，且 \_ \_ 未設定模式比對旗標 \_ not 旗標，則此模式會通過。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="0ebe0-118">如果兩者不同，且未設定模式比對 \_ \_ 旗標 \_ ，則模式會通過。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="0ebe0-119">否則，此模式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="0ebe0-120">或：</span><span class="sxs-lookup"><span data-stu-id="0ebe0-120">Or:</span></span>

<span data-ttu-id="0ebe0-121">如果 \_ \_ 已設定模式符合旗標 \_ 埠指定的旗標 \_ ，且基礎設定為相對於 IPX 的相對於 \_ IPX 或相對於 \_ \_ \_ \_ \_ \_ \_ IP 的位移，則比較會比較複雜。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="0ebe0-122">首先，驅動程式會確認位移基礎通訊協定，然後驅動程式會驗證指定的埠是否符合框架中的埠。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="0ebe0-123">最後，驅動程式會確保 **PatternToMatch** 成員與之前相符，但位移是來自 IP 或 IPX 的結尾。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="0ebe0-124">請注意，如果基礎不是這兩種類型的其中一種，則會忽略模式比對 \_ \_ 旗標 \_ 埠 \_ 指定的旗標，且會依照上述方式評估模式。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="0ebe0-125">若要評估單一模式比對， [**運算式**](expression.md) 結構必須有一個包含單一模式相符的 **AndExp** 成員。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="0ebe0-126">建立模式比對篩選牽涉到建立 [**PATTERNMATCH**](patternmatch.md) 結構，並以邏輯方式將它們與 [**運算式**](expression.md) 和 [**ANDEXP**](andexp.md) 結構結合在一起。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="0ebe0-127">**撰寫 PATTERNMATCH 篩選**</span><span class="sxs-lookup"><span data-stu-id="0ebe0-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="0ebe0-128">在 [**ANDEXP**](andexp.md) 結構中，使用模式比對來填入陣列。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="0ebe0-129">以 **AndExp** 成員的陣列填入 [**運算式**](expression.md)結構。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="0ebe0-130">針對 capture 篩選器，請勿超過四個模式相符專案的總和。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="0ebe0-131">在 [**PATTERNMATCH**](patternmatch.md) 結構中，選取旗標類型。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="0ebe0-132">選取位移。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="0ebe0-133">列舉埠值。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="0ebe0-134">定義位移值。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-134">Define offset value.</span></span>
8.  <span data-ttu-id="0ebe0-135">定義模式長度。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="0ebe0-136">列舉模式值。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="0ebe0-137">PATTERNMATCH 範例</span><span class="sxs-lookup"><span data-stu-id="0ebe0-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="0ebe0-138">此框架表示標準位移。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-138">This frame represents a standard offset.</span></span>

![標準位移框架](images/offs-pat.png)

<span data-ttu-id="0ebe0-140">程式碼片段會實作為：</span><span class="sxs-lookup"><span data-stu-id="0ebe0-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="0ebe0-141">此框架描述對 IPX)  (埠指定的位移。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-141">This frame depicts a port-specified offset (against IPX).</span></span>

![埠指定的位移框架](images/stan-pat.png)

<span data-ttu-id="0ebe0-143">範例程式碼會實作為：</span><span class="sxs-lookup"><span data-stu-id="0ebe0-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



