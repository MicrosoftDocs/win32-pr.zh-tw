---
title: 完整指標
description: 與唯一指標不同，完整指標支援別名。
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933343"
---
# <a name="full-pointers"></a><span data-ttu-id="584ac-103">完整指標</span><span class="sxs-lookup"><span data-stu-id="584ac-103">Full Pointers</span></span>

<span data-ttu-id="584ac-104">與 [唯一](unique-pointers.md) 指標不同，完整指標支援別名。</span><span class="sxs-lookup"><span data-stu-id="584ac-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="584ac-105">這表示多個指標可以參考相同的資料，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="584ac-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![參考相同資料的兩個指標](images/prog-a02.png)

<span data-ttu-id="584ac-107">完整指標具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="584ac-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="584ac-108">其值可以是 null。</span><span class="sxs-lookup"><span data-stu-id="584ac-108">It can have the value null.</span></span>
-   <span data-ttu-id="584ac-109">在呼叫期間，它可以從 null 變更為非 null。</span><span class="sxs-lookup"><span data-stu-id="584ac-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="584ac-110">當值變更為非 null 時，用戶端 stub 會配置傳回時配置的新記憶體。</span><span class="sxs-lookup"><span data-stu-id="584ac-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="584ac-111">用戶端程式應該在它結束之前釋出此記憶體。</span><span class="sxs-lookup"><span data-stu-id="584ac-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="584ac-112">在呼叫期間，它可以從非 null 變更為 null。</span><span class="sxs-lookup"><span data-stu-id="584ac-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="584ac-113">當值變更為 null 時，應用程式會負責釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="584ac-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="584ac-114">值可以從一個非 null 值變更為另一個值。</span><span class="sxs-lookup"><span data-stu-id="584ac-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="584ac-115">在作業中，可能會透過另一個指標或名稱來存取完整指標指向的儲存體。</span><span class="sxs-lookup"><span data-stu-id="584ac-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="584ac-116">如果指標沒有 null 值，則會將傳回的資料寫入至現有的儲存體。</span><span class="sxs-lookup"><span data-stu-id="584ac-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="584ac-117">使用 \[ [**ptr**](/windows/desktop/Midl/ptr) \] 屬性指定完整的指標，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="584ac-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="584ac-118">在此範例中， *ptrName1* 和 *ptrName2* 參數定義為字串的完整指標。</span><span class="sxs-lookup"><span data-stu-id="584ac-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="584ac-119">這兩個指標可能會指向包含單一字串的相同記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="584ac-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="584ac-120">\[**ptr** \]提供別名支援時是必要的。</span><span class="sxs-lookup"><span data-stu-id="584ac-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="584ac-121">不過，因為它需要大部分的 RPC 中可用指標的處理，所以不建議用於大部分的應用程式。</span><span class="sxs-lookup"><span data-stu-id="584ac-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 