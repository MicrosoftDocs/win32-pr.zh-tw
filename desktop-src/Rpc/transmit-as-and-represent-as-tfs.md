---
title: Transmit_as 和 Represent_as
description: 傳送 \_ as 和表示為共用相同的版面配置，但不含 \_ 前置的權杖; 權杖 \_ \_ 會以或 fc 表示的 fc 傳輸 \_ \_ ，但基礎程式碼很常見。
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933280"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="66b73-103">傳送 \_ as 和表示 \_ 為</span><span class="sxs-lookup"><span data-stu-id="66b73-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="66b73-104">傳送 \_ as 和表示為共用相同的版面配置，但不含 \_ 前置的權杖; 權杖 \_ \_ 會以或 fc 表示的 fc 傳輸 \_ \_ ，但基礎程式碼很常見。</span><span class="sxs-lookup"><span data-stu-id="66b73-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="66b73-105">描述具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="66b73-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="66b73-106">旗標<1> 位元組包含上方旗標半形和較低的對齊半形。</span><span class="sxs-lookup"><span data-stu-id="66b73-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="66b73-107">對齊的半項會保持傳輸類型的連線對齊。</span><span class="sxs-lookup"><span data-stu-id="66b73-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="66b73-108">當緩衝區調整大小，並使用來自格式代碼的傳輸類型時，就需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="66b73-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="66b73-109">旗標半位元組可以有下列旗標：</span><span class="sxs-lookup"><span data-stu-id="66b73-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="66b73-110">顯示的 \_ 類型 \_ 是 \_ 陣列旗標，會將頂層傳輸標示為 (，或表示為) 引數，其為某個事物的陣列並以傳值方式傳遞。</span><span class="sxs-lookup"><span data-stu-id="66b73-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="66b73-111">[**– Oi**](/windows/desktop/Midl/-oi)解譯器會使用此旗標來跳過這類引數 (這實際上是堆疊上的指標，而不是陣列) 。</span><span class="sxs-lookup"><span data-stu-id="66b73-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="66b73-112">另外兩個旗標也只能用在先前的解譯器中，以正確地在堆疊上的呈現型別上執行。</span><span class="sxs-lookup"><span data-stu-id="66b73-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="66b73-113">Quintuple \_ 索引<2> 是回呼常式 quintuple 的索引 (這實際上是四個函式) 。</span><span class="sxs-lookup"><span data-stu-id="66b73-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="66b73-114">此資料表通用於傳送 as 和表示為，而且會有明顯的對應來表示常式的位置，因為相同的進入點服務會以和表示為程式碼的方式傳輸。</span><span class="sxs-lookup"><span data-stu-id="66b73-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="66b73-115">對應是從 \_ local => 到 \_ xmit、 \_ local => from \_ xmit、free \_ inst => free \_ xmit、free \_ local => free \_ inst。</span><span class="sxs-lookup"><span data-stu-id="66b73-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="66b73-116">顯示的 \_ 類型 \_ 記憶體 \_ 大小<2> 一律會提供顯示/區欄位型別的大小，包括未知的表示為類型。</span><span class="sxs-lookup"><span data-stu-id="66b73-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="66b73-117">傳輸的 \_ 類型 \_ 緩衝區 \_ 大小<2> 為零、大小變化或實際固定大小。</span><span class="sxs-lookup"><span data-stu-id="66b73-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="66b73-118">這是可在調整緩衝區大小時略過某些回呼的優化。</span><span class="sxs-lookup"><span data-stu-id="66b73-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="66b73-119">傳輸的 \_ 類型 \_ 位移<2> 是傳輸類型格式字串的一般相對類型位移。</span><span class="sxs-lookup"><span data-stu-id="66b73-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 