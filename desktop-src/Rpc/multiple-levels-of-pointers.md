---
title: 多個指標層級
description: 在遠端程序呼叫中使用多個層級的指標， (RPC) 。
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933456"
---
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="f5fba-103">多個指標層級</span><span class="sxs-lookup"><span data-stu-id="f5fba-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="f5fba-104">當有多個指標層級時，屬性會與最接近變數名稱的指標相關聯。</span><span class="sxs-lookup"><span data-stu-id="f5fba-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="f5fba-105">用戶端仍須負責配置與回應相關聯的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="f5fba-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="f5fba-106">下列範例可讓存根在不事先事先知道將傳回多少資料的情況下呼叫伺服器：</span><span class="sxs-lookup"><span data-stu-id="f5fba-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

<span data-ttu-id="f5fba-107">在此範例中，存根會將唯一指標傳遞給伺服器，伺服器會將它初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f5fba-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="f5fba-108">然後伺服器會配置橫條區塊、設定指標、設定 size 引數，然後傳回。</span><span class="sxs-lookup"><span data-stu-id="f5fba-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="f5fba-109">請注意，為了讓伺服器在呼叫端上有作用，您必須將 \[ ref 指標傳遞 \] 至您的 \[ 資料的 [**唯一**](/windows/desktop/Midl/unique) \] 指標。</span><span class="sxs-lookup"><span data-stu-id="f5fba-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="f5fba-110">另請注意， \[ [**大小 \_ 為**](/windows/desktop/Midl/size-is) (， \* pSize ) \] ，表示最上層指標不是大小的指標，但較低層級的指標是。</span><span class="sxs-lookup"><span data-stu-id="f5fba-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="f5fba-111">在用戶端上，存根集會在 \* 呼叫遠端程式之前，將 ppBar 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f5fba-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="f5fba-112">然後，存根會配置並拆收橫條圖物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="f5fba-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="f5fba-113">Size 引數表示區塊 (的大小，以及) 的取消封送的橫條數。</span><span class="sxs-lookup"><span data-stu-id="f5fba-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="f5fba-114">當不再需要時，用戶端必須釋放所傳回的 BAR 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="f5fba-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5fba-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5fba-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5fba-116">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="f5fba-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 