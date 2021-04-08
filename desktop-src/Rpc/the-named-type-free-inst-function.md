---
title: Named_type_free_inst 函式
description: Stub 會呼叫指名 \_ 型別 \_ free inst 函式來釋 \_ 出與傳輸類型相關聯的記憶體。
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672260"
---
# <a name="the-named_type_free_inst-function"></a><span data-ttu-id="8cd2b-104">指名 \_ 型別 \_ free \_ inst 函式</span><span class="sxs-lookup"><span data-stu-id="8cd2b-104">The named\_type\_free\_inst Function</span></span>

<span data-ttu-id="8cd2b-105">Stub 會呼叫 **指名 \_ 型別 \_ free \_ inst** 函式來釋出與傳輸類型相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8cd2b-105">The stubs call the **named\_type\_free\_inst** function to free memory associated with the transmitted type.</span></span> <span data-ttu-id="8cd2b-106">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="8cd2b-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="8cd2b-107">參數指向已傳送型別的實例。</span><span class="sxs-lookup"><span data-stu-id="8cd2b-107">The parameter points to the instance of the transmitted type.</span></span> <span data-ttu-id="8cd2b-108">此物件不應該釋放。</span><span class="sxs-lookup"><span data-stu-id="8cd2b-108">This object should not be freed.</span></span> <span data-ttu-id="8cd2b-109">如需有關何時呼叫函數的討論，請參閱 [代表 \_ as 屬性](the-represent-as-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="8cd2b-109">For a discussion on when to call the function, see [The represent\_as Attribute](the-represent-as-attribute.md).</span></span>

 

 




