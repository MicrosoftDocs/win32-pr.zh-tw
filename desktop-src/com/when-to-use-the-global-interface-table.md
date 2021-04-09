---
title: 使用全域介面資料表的時機
description: 使用全域介面資料表的時機
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024137"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="5879f-103">使用全域介面資料表的時機</span><span class="sxs-lookup"><span data-stu-id="5879f-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="5879f-104">如果您要在進程中的單元之間多次封送處理介面指標，您可以使用 [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) 介面。</span><span class="sxs-lookup"><span data-stu-id="5879f-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="5879f-105">使用其他技術時，您必須 remarshal 每次。</span><span class="sxs-lookup"><span data-stu-id="5879f-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="5879f-106">如果介面指標只是取消封送一次，您可能會想要使用 [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) 函數。</span><span class="sxs-lookup"><span data-stu-id="5879f-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="5879f-107">它也可以用來將介面指標從某個執行緒傳遞至相同進程中的另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="5879f-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="5879f-108">[**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)介面也會讓程式設計人員更容易發生另一個困難的問題。</span><span class="sxs-lookup"><span data-stu-id="5879f-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="5879f-109">當下列條件成立時，就會發生此問題：</span><span class="sxs-lookup"><span data-stu-id="5879f-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="5879f-110">同進程 agile 物件會匯總無限制執行緒封送處理器。</span><span class="sxs-lookup"><span data-stu-id="5879f-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="5879f-111">這個相同的 agile 物件也會將 (做為成員變數，) 介面指標指向其他不是 agile 的物件，而且不會匯總無限制執行緒封送處理器。</span><span class="sxs-lookup"><span data-stu-id="5879f-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="5879f-112">在這種情況下，如果外部物件被封送處理至另一個單元，而應用程式呼叫它，而物件嘗試在其任何不是無限制執行緒的成員變數介面指標上呼叫，或為其他單元中的物件 proxy，則可能會得到不正確的結果或錯誤 RPC E 錯誤的 \_ \_ \_ 執行緒。</span><span class="sxs-lookup"><span data-stu-id="5879f-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="5879f-113">發生此錯誤的原因是，內部介面設計為只能從第一次儲存在成員變數中的單元中呼叫。</span><span class="sxs-lookup"><span data-stu-id="5879f-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="5879f-114">若要解決這個問題，匯總無限制執行緒封送處理器的外部物件應該在內部介面上呼叫 [**IGlobalInterfaceTable：： RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) ，並將產生的 cookie 儲存在其成員變數中，而不是儲存實際的介面指標。</span><span class="sxs-lookup"><span data-stu-id="5879f-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="5879f-115">當外部物件要在內建物件的介面指標上呼叫時，它應該呼叫 [**IGlobalInterfaceTable：： GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal)，使用傳回的介面指標，然後釋放它。</span><span class="sxs-lookup"><span data-stu-id="5879f-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="5879f-116">當外部物件消失時，它應該呼叫 [**IGlobalInterfaceTable：： RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) 來移除全域介面資料表中的介面。</span><span class="sxs-lookup"><span data-stu-id="5879f-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5879f-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5879f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5879f-118">建立全域介面資料表</span><span class="sxs-lookup"><span data-stu-id="5879f-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 