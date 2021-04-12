---
title: Top-Level 和內嵌指標
description: 若要瞭解如何在 Microsoft RPC 中配置指標和其相關聯的資料元素，您必須區分最上層指標和內嵌指標。
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462424"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="efacc-103">Top-Level 和內嵌指標</span><span class="sxs-lookup"><span data-stu-id="efacc-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="efacc-104">若要瞭解如何在 Microsoft RPC 中配置指標和其相關聯的資料元素，您必須區分 *最上層指標* 和 *內嵌指標*。</span><span class="sxs-lookup"><span data-stu-id="efacc-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="efacc-105">參考非最上層指標的所有指標集合也很有用。</span><span class="sxs-lookup"><span data-stu-id="efacc-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="efacc-106">*最上層指標* 是在函式原型中指定為參數名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="efacc-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="efacc-107">最上層指標及其對等一律會在伺服器上進行配置。</span><span class="sxs-lookup"><span data-stu-id="efacc-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="efacc-108">*內嵌指標* 是內嵌在資料結構中的指標，例如陣列、結構和等位。</span><span class="sxs-lookup"><span data-stu-id="efacc-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="efacc-109">當內嵌指標只會將輸出寫入緩衝區，而且在輸入上是 null 時，伺服器應用程式可以將其值變更為非 null。</span><span class="sxs-lookup"><span data-stu-id="efacc-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="efacc-110">在此情況下，用戶端 stub 會為此資料配置新的記憶體。</span><span class="sxs-lookup"><span data-stu-id="efacc-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="efacc-111">如果在呼叫之前，用戶端上的內嵌指標不是 null，則存根不會在傳回時配置用戶端上的記憶體。</span><span class="sxs-lookup"><span data-stu-id="efacc-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="efacc-112">取而代之的是，存根會嘗試將與內嵌指標相關聯的記憶體寫入與該指標相關聯之用戶端的現有記憶體中，以覆寫已存在的資料。</span><span class="sxs-lookup"><span data-stu-id="efacc-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="efacc-113">對於從緩衝區讀取或寫入的資料，以及未指定緩衝區大小的資料，輸出長度必須小於或等於輸入長度。</span><span class="sxs-lookup"><span data-stu-id="efacc-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="efacc-114">偵測到溢位時，就會引發 RPC 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="efacc-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="efacc-115">針對字串資料，輸出長度是藉由檢查輸入字串的長度來決定。</span><span class="sxs-lookup"><span data-stu-id="efacc-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="efacc-116">因此，輸出字串的長度不能超過輸入字串的長度。</span><span class="sxs-lookup"><span data-stu-id="efacc-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="efacc-117">最佳做法指引是藉由一律包含大小指定的參數來表示緩衝區大小，以避免此情況。</span><span class="sxs-lookup"><span data-stu-id="efacc-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="efacc-118">內嵌的僅限寫入指標會在 [結合指標和方向屬性](combining-pointer-and-directional-attributes.md)中討論。</span><span class="sxs-lookup"><span data-stu-id="efacc-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="efacc-119">詞彙 *nontop 層級指標* 會參考未在函式原型中指定為參數名稱的所有指標，包括內嵌指標和多層級的嵌套指標。</span><span class="sxs-lookup"><span data-stu-id="efacc-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




