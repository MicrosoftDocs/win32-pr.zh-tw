---
title: 伺服器上的持續性儲存體
description: 您可以將應用程式優化，讓伺服器 stub 在遠端程序呼叫結束時，不會釋放伺服器上的記憶體。
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932395"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="88634-103">伺服器上的持續性儲存體</span><span class="sxs-lookup"><span data-stu-id="88634-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="88634-104">您可以將應用程式優化，讓伺服器 stub 在遠端程序呼叫結束時，不會釋放伺服器上的記憶體。</span><span class="sxs-lookup"><span data-stu-id="88634-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="88634-105">例如，當多個遠端程式將操作內容控制碼時，您可以使用 ACF 屬性 **\[ 配置 (不要 \_ 釋放) \]** 來保留伺服器上配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="88634-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="88634-106">**\[ 配置 (不會 \_ 釋放) \]** 屬性會新增至 ACF 中的 ACF **typedef** 宣告。</span><span class="sxs-lookup"><span data-stu-id="88634-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="88634-107">例如：</span><span class="sxs-lookup"><span data-stu-id="88634-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="88634-108">當 **\[ 配置 (未 \_ 釋放) \]** 屬性時，會由伺服器 stub 配置樹狀結構資料結構，但不會加以釋放。</span><span class="sxs-lookup"><span data-stu-id="88634-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="88634-109">當您將指標變成可供其他常式使用的持續性資料區域時（例如，藉由將指標複製到全域變數），保留的資料可供其他伺服器函數存取。</span><span class="sxs-lookup"><span data-stu-id="88634-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="88634-110">**\[ 配置 (不會 \_ 釋放) \]** 屬性特別適合用來將持續性指標結構維護為與內容控制碼類型相關聯的伺服器狀態資訊的一部分。</span><span class="sxs-lookup"><span data-stu-id="88634-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




