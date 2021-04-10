---
title: Type_to_xmit 函式
description: 存根會將型別呼叫 xmit 函式， \_ \_ 以將應用程式所呈現的型別轉換成傳輸型別。
ms.assetid: fb5b3760-d660-4e4e-b5c5-768e8e598e23
keywords:
- type_to_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6a6b250d661fc19b0ee8fb68d21f171960e512
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932432"
---
# <a name="the-type_to_xmit-function"></a><span data-ttu-id="f8638-104">要 xmit 的型別 \_ \_ 函數</span><span class="sxs-lookup"><span data-stu-id="f8638-104">The type\_to\_xmit Function</span></span>

<span data-ttu-id="f8638-105">存根會將 **型別 \_ 呼叫 \_ xmit** 函式，以將應用程式所呈現的型別轉換成傳輸型別。</span><span class="sxs-lookup"><span data-stu-id="f8638-105">The stubs call the **type\_to\_xmit** function to convert the type that is presented by the application into the transmitted type.</span></span> <span data-ttu-id="f8638-106">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="f8638-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_to_xmit ( 
     <type> __RPC_FAR *, <xmit_type> __RPC_FAR *     __RPC_FAR *);
```

<span data-ttu-id="f8638-107">第一個參數是應用程式資料的指標。</span><span class="sxs-lookup"><span data-stu-id="f8638-107">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="f8638-108">第二個參數是由函式所設定，以指向傳輸的資料。</span><span class="sxs-lookup"><span data-stu-id="f8638-108">The second parameter is set by the function to point to the transmitted data.</span></span> <span data-ttu-id="f8638-109">函數必須為傳輸的類型配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="f8638-109">The function must allocate memory for the transmitted type.</span></span>

<span data-ttu-id="f8638-110">在下列範例中，用戶端會呼叫具有 DOUBLE 連結類型之 **\[ in、out \]** 參數的遠端過程 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f8638-110">In the following example, the client calls the remote procedure that has an **\[in, out\]** parameter of type DOUBLE\_LINK\_TYPE.</span></span> <span data-ttu-id="f8638-111">用戶端 stub 會呼叫 **\_ \_ xmit** 函式（在此為 xmit 的類型），以 \_ \_ \_ \_ 將雙重連結的清單資料轉換成大小的陣列。</span><span class="sxs-lookup"><span data-stu-id="f8638-111">The client stub calls the **type\_to\_xmit** function, here named DOUBLE\_LINK\_TYPE\_to\_xmit, to convert double-linked list data into a sized array.</span></span>

<span data-ttu-id="f8638-112">函式會判斷清單中的專案數、配置夠大的陣列來容納這些元素，然後將清單專案複製到陣列中。</span><span class="sxs-lookup"><span data-stu-id="f8638-112">The function determines the number of elements in the list, allocates an array large enough to hold those elements, then copies the list elements into the array.</span></span> <span data-ttu-id="f8638-113">在函數傳回之前，會將第二個參數 *ppArray* 設定為指向新配置的資料結構。</span><span class="sxs-lookup"><span data-stu-id="f8638-113">Before the function returns, the second parameter, *ppArray*, is set to point to the newly allocated data structure.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray)
{
    short cCount = 0;
    DOUBLE_LINK_TYPE * pHead = pList;  // save pointer to start 
    DOUBLE_XMIT_TYPE * pArray;
 
    /* count the number of elements to allocate memory */
    for (; pList != NULL; pList = pList->pNext)
        cCount++;
 
    /* allocate the memory for the array */
    pArray = (DOUBLE_XMIT_TYPE *) MIDL_user_allocate 
         (sizeof(DOUBLE_XMIT_TYPE) + (cCount * sizeof(short)));
    pArray->sSize = cCount;
 
    /* copy the linked list contents into the array */
    cCount = 0;
    for (i = 0, pList = pHead; pList != NULL; pList = pList->pNext)
        pArray->asNumber[cCount++] = pList->sNumber;
 
    /* return the address of the pointer to the array */
    *ppArray = pArray;
}
```



 

 




