---
title: 避免多型
description: 新的資料類型包括兩個多型類型： INT \_ PTR 和 LONG \_ PTR。
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- 多型64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311103"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="1c71f-104">避免多型</span><span class="sxs-lookup"><span data-stu-id="1c71f-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="1c71f-105">新的資料類型包括兩個多型類型： **INT \_ PTR** 和 **LONG \_ PTR**。</span><span class="sxs-lookup"><span data-stu-id="1c71f-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="1c71f-106">在32位的 Windows 上， **int \_ ptr** 對應到 **int** ，而 **long \_ PTR** 對應到 **long**。</span><span class="sxs-lookup"><span data-stu-id="1c71f-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="1c71f-107">在64位的 Windows 上，這兩種類型都會對應至 **\_ \_ int64** 內建類型。</span><span class="sxs-lookup"><span data-stu-id="1c71f-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="1c71f-108">MIDL 編譯器支援這些類型進行遠端程序呼叫，但在分散式環境中使用這些類型時，您必須記住這項固有的限制。</span><span class="sxs-lookup"><span data-stu-id="1c71f-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="1c71f-109">請務必適當地批註您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1c71f-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="1c71f-110">無論平臺大小為何，這些多型類型的網路大小一律為32位。</span><span class="sxs-lookup"><span data-stu-id="1c71f-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="1c71f-111">在64位 Windows 上進行封送時，執行時間程式庫符號會擴充帶正負號的值，並將零指派給不帶正負號值的高序位位元組。</span><span class="sxs-lookup"><span data-stu-id="1c71f-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="1c71f-112">將64位值放在網路上時，執行時間會截斷高序位的位元組。</span><span class="sxs-lookup"><span data-stu-id="1c71f-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="1c71f-113">因此，只有低序位的32位值可以使用。</span><span class="sxs-lookup"><span data-stu-id="1c71f-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="1c71f-114">只有在移植需要時，才使用多型類型。</span><span class="sxs-lookup"><span data-stu-id="1c71f-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="1c71f-115">針對新的介面，請使用 MIDL 內建整數類型 **\_ \_ int32** 和 **\_ \_ int64**，或使用指標類型或內容控制碼，以最適合傳送的資料類型為准。</span><span class="sxs-lookup"><span data-stu-id="1c71f-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="1c71f-116">64位編譯器支援新的多型內建函式內部 **\_ \_ int3264**。</span><span class="sxs-lookup"><span data-stu-id="1c71f-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="1c71f-117">同樣地，這種類型是為了支援移植工作而開發的，在此情況下，可透明地支援 **UINT \_ PTR** 類型。</span><span class="sxs-lookup"><span data-stu-id="1c71f-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="1c71f-118"> (另一個內建 **\_ \_ long3264**，將會 **支援 \_ ULONG PTR** 類型。 ) 不會直接使用 **\_ \_ int3264** ; 當您基於移植原因需要多型型別時，請使用 **INT \_ ptr** 型別。</span><span class="sxs-lookup"><span data-stu-id="1c71f-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




