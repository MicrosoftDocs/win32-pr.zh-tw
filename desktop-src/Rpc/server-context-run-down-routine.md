---
title: 伺服器內容執行例行常式
description: 如果通訊中斷時，伺服器會代表用戶端維護內容，則可能需要清除常式，以代表指定的用戶端清除伺服器所維護的狀態。
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021893"
---
# <a name="server-context-run-down-routine"></a><span data-ttu-id="15ad2-103">伺服器內容執行例行常式</span><span class="sxs-lookup"><span data-stu-id="15ad2-103">Server Context Run-down Routine</span></span>

<span data-ttu-id="15ad2-104">如果通訊中斷時，伺服器會代表用戶端維護內容，則可能需要清除常式，以代表指定的用戶端清除伺服器所維護的狀態。</span><span class="sxs-lookup"><span data-stu-id="15ad2-104">If communication breaks down while the server is maintaining context on behalf of the client, a cleanup routine may be needed to clean up the state maintained by the server on behalf of a given client.</span></span> <span data-ttu-id="15ad2-105">此清除常式稱為 *內容執行常式*。</span><span class="sxs-lookup"><span data-stu-id="15ad2-105">This cleanup routine is called a *context run-down routine*.</span></span> <span data-ttu-id="15ad2-106">當連接中斷時，伺服器 stub 和執行時間程式庫會在用戶端開啟的每個內容控制碼上呼叫這個常式。</span><span class="sxs-lookup"><span data-stu-id="15ad2-106">When a connection breaks, the server stub and the run-time library will call this routine on every context handle opened by the client.</span></span>

<span data-ttu-id="15ad2-107">當您將 \[ **內容 \_ 控制碼** 屬性套用至型別定義時，需要執行內容執行程式，並以隱含方式宣告和命名 \] 。</span><span class="sxs-lookup"><span data-stu-id="15ad2-107">The context run-down routine is required, and is implicitly declared and named, when you apply the \[**context\_handle**\] attribute to a type definition.</span></span> <span data-ttu-id="15ad2-108">如果 \[ **內容 \_ 控制碼** \] 屬性直接套用至參數，伺服器將不會呼叫內容執行常式。</span><span class="sxs-lookup"><span data-stu-id="15ad2-108">The server will not call the context run-down routine if the \[**context\_handle**\] attribute was applied directly to a parameter.</span></span>

<span data-ttu-id="15ad2-109">內容的執行常式語法如下：</span><span class="sxs-lookup"><span data-stu-id="15ad2-109">The context run-down routine syntax is:</span></span>

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

<span data-ttu-id="15ad2-110">請注意，型別名稱會決定內容執行常式的名稱。</span><span class="sxs-lookup"><span data-stu-id="15ad2-110">Note that the type name determines the name of the context run-down routine.</span></span>

<span data-ttu-id="15ad2-111">接下來的程式碼片段會顯示範例內容的執行常式。</span><span class="sxs-lookup"><span data-stu-id="15ad2-111">The code fragment that follows presents a sample context run-down routine.</span></span> <span data-ttu-id="15ad2-112">這會使用內容控制碼、使用內容控制碼的[伺服器開發](server-development-using-context-handles.md)，以及[使用內容控制碼的用戶端開發](client-development-using-context-handles.md)，來呼叫在[介面開發](interface-development-using-context-handles.md)的範例中使用的 RemoteClose 程式。</span><span class="sxs-lookup"><span data-stu-id="15ad2-112">that calls the RemoteClose procedure used in the example in [Interface Development Using Context Handles](interface-development-using-context-handles.md), [Server Development Using Context Handles](server-development-using-context-handles.md), and [Client Development Using Context Handles](client-development-using-context-handles.md).</span></span> <span data-ttu-id="15ad2-113">此程式會關閉檔案控制代碼、釋出與檔案相關聯的記憶體，並將 **Null** 指派給內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="15ad2-113">This procedure closes the file handle, frees the memory associated with the file, and assigns **NULL** to the context handle.</span></span> <span data-ttu-id="15ad2-114">指派 **Null** 是呼叫 RemoteClose 函式的結果，不需要在執行中的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="15ad2-114">Assigning **NULL** is a result of calling the RemoteClose function, and is not necessary in a run-down scenario.</span></span> <span data-ttu-id="15ad2-115">無論內容控制碼是否設為 **Null**，RPC 執行時間都會清除其狀態。</span><span class="sxs-lookup"><span data-stu-id="15ad2-115">The RPC run time cleans up its state regardless of whether the context handle is set to **NULL**.</span></span>

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




