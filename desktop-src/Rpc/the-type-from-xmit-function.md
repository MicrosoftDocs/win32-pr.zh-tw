---
title: Type_from_xmit 函式
description: 存根從 xmit 函式呼叫型別， \_ \_ 以將資料從其傳送的型別轉換為向應用程式呈現的型別。
ms.assetid: 679a2738-a166-4e73-bca7-950f979ed97a
keywords:
- type_from_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e594e8586522dd3697f5ae62c95851917741f73c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021891"
---
# <a name="the-type_from_xmit-function"></a><span data-ttu-id="a2fca-104">Xmit 函式中的型別 \_ \_</span><span class="sxs-lookup"><span data-stu-id="a2fca-104">The type\_from\_xmit Function</span></span>

<span data-ttu-id="a2fca-105">存根 **\_ 從 \_ xmit** 函式呼叫型別，以將資料從其傳送的型別轉換為向應用程式呈現的型別。</span><span class="sxs-lookup"><span data-stu-id="a2fca-105">The stubs call the **type\_from\_xmit** function to convert data from its transmitted type to the type that is presented to the application.</span></span> <span data-ttu-id="a2fca-106">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="a2fca-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_from_xmit ( 
    <xmit_type> __RPC_FAR *, 
    <type> __RPC_FAR *);
```

<span data-ttu-id="a2fca-107">第一個參數是傳輸資料的指標。</span><span class="sxs-lookup"><span data-stu-id="a2fca-107">The first parameter is a pointer to the transmitted data.</span></span> <span data-ttu-id="a2fca-108">函式會設定第二個參數以指向呈現的資料。</span><span class="sxs-lookup"><span data-stu-id="a2fca-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="a2fca-109">**\_ \_ Xmit** 函式中的型別必須管理顯示類型的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a2fca-109">The **type\_from\_xmit** function must manage memory for the presented type.</span></span> <span data-ttu-id="a2fca-110">函式必須為從第二個參數所指定的位址開始的整個資料結構配置記憶體，但參數本身 (存根會為根節點配置記憶體，並將其傳遞至函式) 。</span><span class="sxs-lookup"><span data-stu-id="a2fca-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="a2fca-111">第二個參數的值不能在呼叫期間變更。</span><span class="sxs-lookup"><span data-stu-id="a2fca-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="a2fca-112">函數可以變更該位址的內容。</span><span class="sxs-lookup"><span data-stu-id="a2fca-112">The function can change the contents at that address.</span></span>

<span data-ttu-id="a2fca-113">在此範例中，xmit 的函式雙重 \_ 連結 \_ 類型會 \_ \_ 將調整大小的陣列轉換成雙重連結的清單。</span><span class="sxs-lookup"><span data-stu-id="a2fca-113">In this example, the function DOUBLE\_LINK\_TYPE\_from\_xmit converts the sized array to a double-linked list.</span></span> <span data-ttu-id="a2fca-114">函式會保留清單開頭的有效指標、釋放與清單其餘部分相關聯的記憶體，然後建立從相同指標開始的新清單。</span><span class="sxs-lookup"><span data-stu-id="a2fca-114">The function retains the valid pointer to the beginning of the list, frees memory associated with the rest of the list, then creates a new list that starts at the same pointer.</span></span> <span data-ttu-id="a2fca-115">函數會使用公用程式函式 **InsertNewNode**，將清單節點附加至清單結尾，並將 *pNext* 和 *pPrevious* 指標指派給適當的值。</span><span class="sxs-lookup"><span data-stu-id="a2fca-115">The function uses a utility function, **InsertNewNode**, to append a list node to the end of the list and to assign the *pNext* and *pPrevious* pointers to appropriate values.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_from_xmit(
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    DOUBLE_LINK_TYPE *pCurrent;
    int i;
 
    if (pArray->sSize <= 0) 
    {  
        // error checking
        return;
    }
 
    if (pList == NULL) // if invalid, create the list head
        pList = InsertNewNode(pArray->asNumber[0], NULL);             
    else 
    {    
        DOUBLE_LINK_TYPE_free_inst(pList);  // free all other nodes
        pList->sNumber = pArray->asNumber[0];
        pList->pNext = NULL; 
    }
 
    pCurrent = pList; 
    for (i = 1; i < pArray->sSize; i++)  
        pCurrent = InsertNewNode(pArray->asNumber[i], pCurrent);
    
    return;
}
```



 

 




