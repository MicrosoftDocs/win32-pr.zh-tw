---
title: Named_type_to_local 函式
description: 存根會將已命名的型別呼叫 \_ \_ 至區域函式 \_ ，以將資料從傳送的型別轉換為它們呈現給應用程式的型別。
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021447"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="76478-104">區域函式的命名 \_ 類型 \_ \_</span><span class="sxs-lookup"><span data-stu-id="76478-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="76478-105">存根會將 **已命名的型別呼叫 \_ \_ 至 \_ 區域** 函式，以將資料從傳送的型別轉換為它們呈現給應用程式的型別。</span><span class="sxs-lookup"><span data-stu-id="76478-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="76478-106">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="76478-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="76478-107">第一個參數會指向傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="76478-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="76478-108">函式會設定第二個參數以指向呈現的資料。</span><span class="sxs-lookup"><span data-stu-id="76478-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="76478-109">**\_ \_ \_ 區域** 函式的命名類型必須管理所呈現類型的記憶體。</span><span class="sxs-lookup"><span data-stu-id="76478-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="76478-110">函式必須為從第二個參數所指定的位址開始的整個資料結構配置記憶體，但參數本身 (存根會為根節點配置記憶體，並將其傳遞至函式) 。</span><span class="sxs-lookup"><span data-stu-id="76478-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="76478-111">第二個參數的值不能在呼叫期間變更。</span><span class="sxs-lookup"><span data-stu-id="76478-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="76478-112">函數可以變更該位址的內容。</span><span class="sxs-lookup"><span data-stu-id="76478-112">The function can change the contents at that address.</span></span>

 

 




