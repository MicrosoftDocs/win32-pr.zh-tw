---
title: 大型整數
description: 大型整數函式和結構最初提供32位 Windows 上64位值的支援。
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- 大型整數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106984942"
---
# <a name="large-integers"></a><span data-ttu-id="b0017-104">大型整數</span><span class="sxs-lookup"><span data-stu-id="b0017-104">Large Integers</span></span>

<span data-ttu-id="b0017-105">大型整數函式和結構最初提供32位 Windows 上64位值的支援。</span><span class="sxs-lookup"><span data-stu-id="b0017-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="b0017-106">現在，您的 C 編譯器可能會以原生方式支援64位的整數。</span><span class="sxs-lookup"><span data-stu-id="b0017-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="b0017-107">例如，Microsoft Visual C++ 支援 [**\_ \_ int64**](/windows/desktop/Midl/--int64)大小的整數類型。</span><span class="sxs-lookup"><span data-stu-id="b0017-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="b0017-108">如需詳細資訊，請參閱 C 編譯器隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="b0017-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="b0017-109">如需64位 Windows 上64位整數的詳細資訊，請參閱 [新的資料類型](/windows/desktop/WinProg64/the-new-data-types)。</span><span class="sxs-lookup"><span data-stu-id="b0017-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="b0017-110">大型整數運算</span><span class="sxs-lookup"><span data-stu-id="b0017-110">Large Integer Operations</span></span>

<span data-ttu-id="b0017-111">應用程式可以使用 [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) 和 [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) 函數，將帶正負號或不帶正負號的32位整數（產生64位結果）相乘。</span><span class="sxs-lookup"><span data-stu-id="b0017-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="b0017-112">應用程式可以使用 [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)、 [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)和 [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) 函式，將64位值中的位轉換成左方或右方。</span><span class="sxs-lookup"><span data-stu-id="b0017-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="b0017-113">這些函式提供邏輯和算術移位。</span><span class="sxs-lookup"><span data-stu-id="b0017-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="b0017-114">應用程式也可以使用 [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) 函數，在單一作業中將32位值相乘和相除。</span><span class="sxs-lookup"><span data-stu-id="b0017-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="b0017-115">雖然作業的結果是32位的值，但函數會將中繼結果儲存為64位值，如此一來，當將大型32位值相乘和相除時，資訊就不會遺失。</span><span class="sxs-lookup"><span data-stu-id="b0017-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="b0017-116">大型整數參考</span><span class="sxs-lookup"><span data-stu-id="b0017-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="b0017-117">大型整數函數</span><span class="sxs-lookup"><span data-stu-id="b0017-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="b0017-118">大型整數結構</span><span class="sxs-lookup"><span data-stu-id="b0017-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 