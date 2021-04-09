---
title: 強型別
description: C 是弱型別語言，也就是，編譯器允許在不同類型的變數之間進行指派和比較等作業。
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- 遠端程序呼叫 RPC，描述，資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932556"
---
# <a name="strong-typing"></a><span data-ttu-id="842c4-104">強型別</span><span class="sxs-lookup"><span data-stu-id="842c4-104">Strong Typing</span></span>

<span data-ttu-id="842c4-105">C 是弱型別語言，也就是，編譯器允許在不同類型的變數之間進行指派和比較等作業。</span><span class="sxs-lookup"><span data-stu-id="842c4-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="842c4-106">例如，C 允許將變數的值轉換成另一種類型。</span><span class="sxs-lookup"><span data-stu-id="842c4-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="842c4-107">在相同的運算式中使用不同類型變數的能力，可提升彈性和效率。</span><span class="sxs-lookup"><span data-stu-id="842c4-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="842c4-108">強型別語言會對不同類型的變數之間的作業強加限制。</span><span class="sxs-lookup"><span data-stu-id="842c4-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="842c4-109">在這些情況下，編譯器會發出錯誤，導致作業無法運作。</span><span class="sxs-lookup"><span data-stu-id="842c4-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="842c4-110">這些有關資料類型的嚴格指導方針是設計來避免可能發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="842c4-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="842c4-111">使用弱式類型語言（例如 C）進行遠端程序呼叫的困難之處在于，分散式應用程式可以在具有不同 C 編譯器和不同架構的數部不同電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="842c4-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="842c4-112">當應用程式只在一部電腦上執行時，您不需要擔心內部資料格式，因為資料是以一致的方式處理。</span><span class="sxs-lookup"><span data-stu-id="842c4-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="842c4-113">不過，在分散式運算環境中，不同的電腦可以針對其基底資料類型使用不同的定義。</span><span class="sxs-lookup"><span data-stu-id="842c4-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="842c4-114">例如，某些電腦會定義 **int** 類型，因此其內部標記法為16位，而其他電腦則使用32位。</span><span class="sxs-lookup"><span data-stu-id="842c4-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="842c4-115">一種電腦架構，稱為「位元組由小到小」，會將最少的資料位元組指派給最小的記憶體位址，最重要的位元組則指派到最高的位址。</span><span class="sxs-lookup"><span data-stu-id="842c4-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="842c4-116">另一種架構（稱為「大 endian」）會將最不重要的位元組指派給與該資料相關聯的最高記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="842c4-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="842c4-117">遠端程序呼叫需要嚴格控制參數類型。</span><span class="sxs-lookup"><span data-stu-id="842c4-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="842c4-118">為了處理透過網路的資料傳輸和轉換，MIDL 嚴格強制執行透過網路傳送之資料的類型限制。</span><span class="sxs-lookup"><span data-stu-id="842c4-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="842c4-119">基於這個理由，MIDL 包含一組定義完善的 [基底類型](base-types.md)。</span><span class="sxs-lookup"><span data-stu-id="842c4-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="842c4-120">MIDL 強制執行強型別，方法是強制使用可明確定義資料大小和類型的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="842c4-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="842c4-121">強式類型的最明顯效果是 MIDL 不允許類型為 **void \*** 的變數。</span><span class="sxs-lookup"><span data-stu-id="842c4-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="842c4-122">在下列主題中，本節討論會強制執行強式資料類型的 MIDL 語言功能：</span><span class="sxs-lookup"><span data-stu-id="842c4-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="842c4-123">基底類型</span><span class="sxs-lookup"><span data-stu-id="842c4-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="842c4-124">帶正負號和不帶正負號類型</span><span class="sxs-lookup"><span data-stu-id="842c4-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="842c4-125">寬字元類型</span><span class="sxs-lookup"><span data-stu-id="842c4-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="842c4-126">結構</span><span class="sxs-lookup"><span data-stu-id="842c4-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="842c4-127">等位</span><span class="sxs-lookup"><span data-stu-id="842c4-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="842c4-128">列舉類型</span><span class="sxs-lookup"><span data-stu-id="842c4-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="842c4-129">陣列</span><span class="sxs-lookup"><span data-stu-id="842c4-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="842c4-130">函數屬性</span><span class="sxs-lookup"><span data-stu-id="842c4-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="842c4-131">欄位屬性</span><span class="sxs-lookup"><span data-stu-id="842c4-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="842c4-132">三種指標類型</span><span class="sxs-lookup"><span data-stu-id="842c4-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="842c4-133">類型屬性</span><span class="sxs-lookup"><span data-stu-id="842c4-133">Type Attributes</span></span>](type-attributes.md)

 

 




