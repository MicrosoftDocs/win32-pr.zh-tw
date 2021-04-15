---
title: 不同陣列
description: 在 MIDL 中，不同陣列的大小是固定的。 它們可讓用戶端將不同的陣列部分從用戶端傳遞至伺服器。 陣列部分的大小可能會因調用而異。 但是，整體陣列的大小是固定的。
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463525"
---
# <a name="varying-arrays"></a><span data-ttu-id="e95f2-106">不同陣列</span><span class="sxs-lookup"><span data-stu-id="e95f2-106">Varying Arrays</span></span>

<span data-ttu-id="e95f2-107">在 MIDL 中，不同陣列的大小是固定的。</span><span class="sxs-lookup"><span data-stu-id="e95f2-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="e95f2-108">它們可讓用戶端將不同的陣列部分從用戶端傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="e95f2-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="e95f2-109">陣列部分的大小可能會因調用而異。</span><span class="sxs-lookup"><span data-stu-id="e95f2-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="e95f2-110">但是，整體陣列的大小是固定的。</span><span class="sxs-lookup"><span data-stu-id="e95f2-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="e95f2-111">例如，下列範例顯示 MIDL 檔案介面中的遠端程式定義。</span><span class="sxs-lookup"><span data-stu-id="e95f2-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="e95f2-112">用戶端傳遞至伺服器的陣列大小是由常數陣列大小來修正 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e95f2-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="e95f2-113">介面會指定用戶端在參數 firstElement 和 chunkSize 中傳遞給伺服器之陣列的部分。</span><span class="sxs-lookup"><span data-stu-id="e95f2-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="e95f2-114">介面定義 \[ [**\_ 會先**](/windows/desktop/Midl/first-is)使用 MIDL 屬性， \] 來指定用戶端傳遞至伺服器之陣列部分中第一個元素的索引編號。</span><span class="sxs-lookup"><span data-stu-id="e95f2-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="e95f2-115">[ \[ [**長度] \_ 是**](/windows/desktop/Midl/length-is) \] [屬性] 指定用戶端傳遞的陣列元素總數。</span><span class="sxs-lookup"><span data-stu-id="e95f2-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="e95f2-116">如需有關這些 MIDL 屬性的詳細資訊，請參閱 [陣列屬性](array-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="e95f2-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="e95f2-117">下列程式碼片段說明用戶端可能如何叫用先前 MIDL 檔案中定義的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="e95f2-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



<span data-ttu-id="e95f2-118">此片段會呼叫遠端過程 MyRemoteProc 兩次。</span><span class="sxs-lookup"><span data-stu-id="e95f2-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="e95f2-119">在第一次叫用時，它會傳遞編號為20到119的陣列元素，如變數 firstArrayElementNumber 和 totalElementsPassed 中的值所示。</span><span class="sxs-lookup"><span data-stu-id="e95f2-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="e95f2-120">第二次呼叫時，用戶端會傳遞編號為120到319的陣列元素。</span><span class="sxs-lookup"><span data-stu-id="e95f2-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 