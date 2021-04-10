---
title: Type_free_xmit 函式
description: Stub 會呼叫類型 \_ free xmit 函式 \_ 來釋出與傳輸資料相關聯的記憶體。
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183583"
---
# <a name="the-type_free_xmit-function"></a><span data-ttu-id="58624-104">Type \_ free \_ xmit 函式</span><span class="sxs-lookup"><span data-stu-id="58624-104">The type\_free\_xmit Function</span></span>

<span data-ttu-id="58624-105">Stub 會呼叫 **類型 \_ free \_ xmit** 函式來釋出與傳輸資料相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="58624-105">The stubs call the **type\_free\_xmit** function to free memory associated with the transmitted data.</span></span> <span data-ttu-id="58624-106">在 [ \_ \_ xmit](the-type-from-xmit-function.md) 函式中的型別將傳輸的資料轉換成其所呈現的型別之後，就不再需要記憶體。</span><span class="sxs-lookup"><span data-stu-id="58624-106">After the [type\_from\_xmit](the-type-from-xmit-function.md) function converts the transmitted data to its presented type, the memory is no longer needed.</span></span> <span data-ttu-id="58624-107">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="58624-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

<span data-ttu-id="58624-108">參數是記憶體的指標，其中包含已傳送的型別。</span><span class="sxs-lookup"><span data-stu-id="58624-108">The parameter is a pointer to the memory that contains the transmitted type.</span></span>

<span data-ttu-id="58624-109">在此範例中，記憶體包含單一結構中的陣列。</span><span class="sxs-lookup"><span data-stu-id="58624-109">In this example, the memory contains an array that is in a single structure.</span></span> <span data-ttu-id="58624-110">函數雙重 \_ 連結 \_ 類型 \_ free xmit 會 \_ 使用使用者提供的 midl midl \_ 使用者 \_ free 來釋放記憶體：</span><span class="sxs-lookup"><span data-stu-id="58624-110">The function DOUBLE\_LINK\_TYPE\_free\_xmit uses the user-supplied function midl\_user\_free to free the memory:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




