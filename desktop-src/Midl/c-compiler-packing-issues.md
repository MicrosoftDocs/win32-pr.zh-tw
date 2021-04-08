---
title: C-編譯器封裝問題
description: 封裝層級會以相同方式影響 MIDL 和 Microsoft C/c + + 編譯器之類型的記憶體配置。
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL 編譯器 MIDL，C-編譯器封裝問題
- 封裝 MIDL
- 記憶體配置 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842224"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="77b65-106">C-編譯器封裝問題</span><span class="sxs-lookup"><span data-stu-id="77b65-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="77b65-107">封裝層級會以相同方式影響 MIDL 和 Microsoft C/c + + 編譯器之類型的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="77b65-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="77b65-108">在 Microsoft 組建環境中（例如 VC + + 所定義的組建環境或平臺軟體發展工具組 (SDK) ），MIDL 和 C/c + + 編譯器的預設封裝層級是相同的;32位和64位 Windows 組建環境的預設封裝層級為8。</span><span class="sxs-lookup"><span data-stu-id="77b65-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="77b65-109">自然對齊</span><span class="sxs-lookup"><span data-stu-id="77b65-109">Natural Alignment</span></span>

<span data-ttu-id="77b65-110">對於記憶體中的型別，預設對齊方式與其自然對齊方式相同。</span><span class="sxs-lookup"><span data-stu-id="77b65-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="77b65-111">基底型別（例如 short、float 和 \_ \_ int64）和指標在其標記法開始于其大小的模數位址時自然對齊。</span><span class="sxs-lookup"><span data-stu-id="77b65-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="77b65-112">所有目前支援的基底類型都有1、2、4或8的大小。</span><span class="sxs-lookup"><span data-stu-id="77b65-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="77b65-113">在32位環境中，指標的大小為4，64位的環境中則為8。</span><span class="sxs-lookup"><span data-stu-id="77b65-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="77b65-114">如果它的每個元件都是以自然方式相對於型別開頭，且沒有任何不必要的間距 (填補在元件之間) ，則會自然對齊複合類型。</span><span class="sxs-lookup"><span data-stu-id="77b65-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="77b65-115">複合元件（例如欄位或元素）會遞迴至指標或基底類型元件。</span><span class="sxs-lookup"><span data-stu-id="77b65-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="77b65-116">有一個簡單的規則，可協助您記住這項行為，也就是類型的自然對齊方式等於其元件的最大對齊。</span><span class="sxs-lookup"><span data-stu-id="77b65-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="77b65-117">在 C 或 c + + 和 IDL 等語言中，類型的對齊和記憶體大小之間有連接，如運算子 **sizeof ()** 所表示。</span><span class="sxs-lookup"><span data-stu-id="77b65-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="77b65-118">大小是對齊的倍數 (最小倍數橫跨類型) 。</span><span class="sxs-lookup"><span data-stu-id="77b65-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="77b65-119">這會在記憶體中的陣列標記法之後進行。</span><span class="sxs-lookup"><span data-stu-id="77b65-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="77b65-120">自然對齊很重要，因為存取未對齊的資料可能會在某些系統上造成例外狀況。</span><span class="sxs-lookup"><span data-stu-id="77b65-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="77b65-121">當資料不一致時，可以將資料標示為安全的操作，但這通常牽涉到某些平臺上可能會有巨大的速度。</span><span class="sxs-lookup"><span data-stu-id="77b65-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="77b65-122">在記憶體中，當放置在 *n* 的倍數的位址時，具有自然對齊 *n* 的類型物件一定會適當地對齊。</span><span class="sxs-lookup"><span data-stu-id="77b65-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="77b65-123">封裝與對齊</span><span class="sxs-lookup"><span data-stu-id="77b65-123">Packing versus Alignment</span></span>

<span data-ttu-id="77b65-124">指定大於自然對齊類型的封裝層級並不會變更類型對齊。</span><span class="sxs-lookup"><span data-stu-id="77b65-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="77b65-125">指定小於自然對齊的封裝層級，會將類型對齊減少為封裝層級。</span><span class="sxs-lookup"><span data-stu-id="77b65-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="77b65-126">如此一來，封裝的型別可能會放在記憶體中的位址，這些位址是封裝層級的倍數 (減少對齊) 而不會造成不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="77b65-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="77b65-127">這會影響簡單類型和元件類型。</span><span class="sxs-lookup"><span data-stu-id="77b65-127">This affects both simple types and component types.</span></span> <span data-ttu-id="77b65-128">針對複合類型，類型的內部配置可能會受到影響，因為較小的元件對齊可能會變更適當對齊元件所需的填補大小，進而減少類型的大小。</span><span class="sxs-lookup"><span data-stu-id="77b65-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="77b65-129">有一個簡單的規則，可協助您記住這項行為，也就是封裝類型的新對齊方式是封裝層級和其自然對齊的較小者。</span><span class="sxs-lookup"><span data-stu-id="77b65-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="77b65-130">此類型的大小為新對齊的倍數。</span><span class="sxs-lookup"><span data-stu-id="77b65-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="77b65-131">**Sizeof ()** 運算子會傳回壓縮類型的縮減大小。</span><span class="sxs-lookup"><span data-stu-id="77b65-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="77b65-132">例如，在封裝層級2中，長時間會變成2，因此可能會放在任何偶數的位址，而不只是在具有自然對齊的情況下的4個位址。</span><span class="sxs-lookup"><span data-stu-id="77b65-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="77b65-133">具有簡短和長（封裝于2）的結構，不需要自然對齊所需的短時間與下列長度之間的內部間距;因此，不只是現在的結構在2，它的大小也會從8降到6。</span><span class="sxs-lookup"><span data-stu-id="77b65-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="77b65-134">例如，假設有一個包含1位元組字元的複合類型、一個整數的4個位元組，以及一個1位元組字元：</span><span class="sxs-lookup"><span data-stu-id="77b65-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="77b65-135">此結構自然對齊4，且自然大小為12。</span><span class="sxs-lookup"><span data-stu-id="77b65-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="77b65-136">針對封裝層級4或更高版本，結構 **mystruct>)** 會對齊4，且 `sizeof(struct mystructtype)` 等於12。</span><span class="sxs-lookup"><span data-stu-id="77b65-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="77b65-137">如果位於記憶體中的位址不是4的倍數，則結構將會對齊。</span><span class="sxs-lookup"><span data-stu-id="77b65-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="77b65-138">針對封裝層級2，結構會對齊2，而其大小為8。</span><span class="sxs-lookup"><span data-stu-id="77b65-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="77b65-139">如果在記憶體中的位址不是2的倍數，則以層級2封裝的結構將會對齊。</span><span class="sxs-lookup"><span data-stu-id="77b65-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="77b65-140">針對封裝層級1，結構會對齊1，且其大小為6。</span><span class="sxs-lookup"><span data-stu-id="77b65-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="77b65-141">以層級1壓縮的結構可以放置在任何位置，而不會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="77b65-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77b65-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="77b65-142">Related topics</span></span>

<dl> <span data-ttu-id="77b65-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="77b65-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="77b65-144">/Zp</span><span class="sxs-lookup"><span data-stu-id="77b65-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="77b65-145">/pack</span><span class="sxs-lookup"><span data-stu-id="77b65-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 