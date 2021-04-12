---
title: " in、out、size_is 原型"
description: '\ in、out、size \_ 是 \ 原型使用從用戶端到伺服器，以及從伺服器傳遞至用戶端的單一計數位符陣列。'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315373"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="7e970-103">\[in、out、size \_ 為 \] 原型</span><span class="sxs-lookup"><span data-stu-id="7e970-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="7e970-104">下列函式原型使用以兩種方式傳遞的單一計數位符陣列：從用戶端到伺服器，以及從伺服器到用戶端：</span><span class="sxs-lookup"><span data-stu-id="7e970-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="7e970-105">\[ [](/windows/desktop/Midl/in) \] *AchInOut* 必須指向用戶端上的有效儲存體，做為 in 參數。</span><span class="sxs-lookup"><span data-stu-id="7e970-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="7e970-106">開發人員在進行遠端程序呼叫之前，會先在用戶端上配置與陣列相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7e970-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="7e970-107">存根使用的 \[ [**大小 \_ 是**](/windows/desktop/Midl/size-is) \] 參數 *strsize* 來佈建服務器上的記憶體，然後使用 \[ [**長度 \_ 為**](/windows/desktop/Midl/length-is) \] 參數 *pcbSize* ，將陣列元素傳輸至此記憶體。</span><span class="sxs-lookup"><span data-stu-id="7e970-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="7e970-108">開發人員必須確定用戶端程式代碼會在呼叫遠端程式之前，先將 **\[ 長度設定 \_ 為 \]** 變數。</span><span class="sxs-lookup"><span data-stu-id="7e970-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="7e970-109">在某些情況下，針對輸入和輸出使用不同的參數，而不是單一字串，會更有效率，並提供彈性。</span><span class="sxs-lookup"><span data-stu-id="7e970-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="7e970-110">下一個範例會示範這一點：</span><span class="sxs-lookup"><span data-stu-id="7e970-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="7e970-111">在上述範例中，字元陣列 achInOut 也用來當做 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數。</span><span class="sxs-lookup"><span data-stu-id="7e970-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="7e970-112">在 C 中，陣列的名稱相當於使用指標。</span><span class="sxs-lookup"><span data-stu-id="7e970-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="7e970-113">依預設，所有最上層指標都是參考指標，它們在值中不會變更，而且會在呼叫前後指向用戶端上相同的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="7e970-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="7e970-114">遠端程式所存取的所有記憶體都必須符合用戶端在呼叫之前指定的大小，否則 stub 將會產生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7e970-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="7e970-115">在傳回之前，伺服器上的分析函數必須重設 *pcbSize* 參數，以指出伺服器將傳送至用戶端的元素數目，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e970-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 