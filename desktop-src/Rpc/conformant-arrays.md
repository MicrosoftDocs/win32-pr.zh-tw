---
title: 符合標準的陣列
description: 一致性陣列的大小在每次用戶端傳遞至伺服器上的遠端程式時，可能會有所不同或符合。
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023927"
---
# <a name="conformant-arrays"></a><span data-ttu-id="4ec5d-103">符合標準的陣列</span><span class="sxs-lookup"><span data-stu-id="4ec5d-103">Conformant Arrays</span></span>

<span data-ttu-id="4ec5d-104">一致性陣列的大小在每次用戶端傳遞至伺服器上的遠端程式時，可能會有所不同或符合。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="4ec5d-105">應用程式的 MIDL 檔案中的介面定義，可讓用戶端在每次叫用遠端程式時，指定陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="4ec5d-106">在 \[ \] 陣列定義中使用空的方括弧 () 或星號 (\[ \* \]) 以表示符合標準的陣列。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="4ec5d-107">下列範例會在 MIDL 檔案的介面中包含遠端程式的定義。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="4ec5d-108">用戶端會指定由參數 *arraySize* 傳遞給伺服器的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="4ec5d-109">介面定義會使用 MIDL 屬性 \[ [**大小 \_ ，**](/windows/desktop/Midl/size-is) \] 來指定用戶端傳遞至伺服器的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="4ec5d-110">如果您想要指出陣列索引編號的最大值，請改用 \[ [**max \_ 為**](/windows/desktop/Midl/max-is) \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="4ec5d-111">如需有關這些 MIDL 屬性的詳細資訊，請參閱 [陣列屬性](array-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="4ec5d-112">下列程式碼片段說明用戶端可能如何叫用先前 MIDL 檔案中定義的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



<span data-ttu-id="4ec5d-113">此片段會呼叫遠端過程 MyRemoteProc 兩次。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="4ec5d-114">在第一次叫用時，它會傳遞20個元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="4ec5d-115">第二次呼叫時，用戶端會傳遞200個元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="4ec5d-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 