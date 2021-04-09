---
title: 參考指標
description: 參考指標是最簡單的指標，且需要用戶端存根的最少處理量。
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023976"
---
# <a name="reference-pointers"></a><span data-ttu-id="8e57b-103">參考指標</span><span class="sxs-lookup"><span data-stu-id="8e57b-103">Reference Pointers</span></span>

<span data-ttu-id="8e57b-104">參考指標是最簡單的指標，且需要用戶端存根的最少處理量。</span><span class="sxs-lookup"><span data-stu-id="8e57b-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="8e57b-105">當用戶端程式傳遞參考指標給遠端程式時，參考指標一律會包含有效記憶體區塊的位址。</span><span class="sxs-lookup"><span data-stu-id="8e57b-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="8e57b-106">當遠端程式完成時，它仍會指向相同的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="8e57b-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="8e57b-107">這些指標主要用來實作為參考語義，並允許 \[ [](/windows/desktop/Midl/out-idl) \] C 中的 out 參數。</span><span class="sxs-lookup"><span data-stu-id="8e57b-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="8e57b-108">在下列範例中，在呼叫期間，指標的值不會變更，但是指標所指出之位址的資料內容可能會變更。</span><span class="sxs-lookup"><span data-stu-id="8e57b-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![在靜態參考指標位址變更資料](images/prog-a07.png)

<span data-ttu-id="8e57b-110">參考指標具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="8e57b-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="8e57b-111">它一律會指向有效的儲存體，而且永遠不會有 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="8e57b-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="8e57b-112">它永遠不會在呼叫期間變更，而且一律會在呼叫前後指向相同的儲存體。</span><span class="sxs-lookup"><span data-stu-id="8e57b-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="8e57b-113">從遠端程式傳回的資料會寫入至現有的儲存體。</span><span class="sxs-lookup"><span data-stu-id="8e57b-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="8e57b-114">參考指標所指向的儲存體無法由函式中的任何其他指標或任何其他名稱存取。</span><span class="sxs-lookup"><span data-stu-id="8e57b-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="8e57b-115">您可以使用 \[ [**ref**](/windows/desktop/Midl/ref) \] 屬性在介面定義中指定參考指標，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="8e57b-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="8e57b-116">這個範例會將參數 *pChar* 定義為單一字元的指標，而不是字元陣列。</span><span class="sxs-lookup"><span data-stu-id="8e57b-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="8e57b-117">它是 \[ **out** \] 參數和參考指標，指向伺服器常式 RemoteFn 將填入資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8e57b-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 