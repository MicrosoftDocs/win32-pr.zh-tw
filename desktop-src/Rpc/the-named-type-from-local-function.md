---
title: Named_type_from_local 函式
description: 存根從區域函式呼叫命名的 \_ 型別 \_ \_ 。
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300440"
---
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="6b6be-104">區域函式中的命名 \_ 類型 \_ \_</span><span class="sxs-lookup"><span data-stu-id="6b6be-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="6b6be-105">存根從區域函式呼叫命名的 \_ 型別 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b6be-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="6b6be-106">它會將應用程式使用的型別轉換成存根在網路上傳輸的型別。</span><span class="sxs-lookup"><span data-stu-id="6b6be-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="6b6be-107">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="6b6be-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="6b6be-108">第一個參數是應用程式資料的指標。</span><span class="sxs-lookup"><span data-stu-id="6b6be-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="6b6be-109">第二個參數是指向指標的指標。</span><span class="sxs-lookup"><span data-stu-id="6b6be-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="6b6be-110">函式會將它指向傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="6b6be-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="6b6be-111">函數必須為傳輸的類型配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="6b6be-111">The function must allocate memory for the transmitted type.</span></span>

 

 




