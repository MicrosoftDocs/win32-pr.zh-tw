---
description: 當物件在指定的內容中啟動時，在內容中對其進行的後續呼叫會以不同于整個內容界限的呼叫來處理。
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: 攔截跨內容呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317880"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="be68b-103">攔截跨內容呼叫</span><span class="sxs-lookup"><span data-stu-id="be68b-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="be68b-104">當物件在指定的內容中啟動時，在內容中對其進行的後續呼叫會以不同于整個內容界限的呼叫來處理。</span><span class="sxs-lookup"><span data-stu-id="be68b-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="be68b-105">跨內容界限的呼叫會以羽量級 proxy 處理。</span><span class="sxs-lookup"><span data-stu-id="be68b-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="be68b-106">這些 proxy 會處理任何需要的中繼工作，將執行時間環境從容納呼叫者的執行時間環境調整為容納被呼叫端的環境。</span><span class="sxs-lookup"><span data-stu-id="be68b-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="be68b-107">此進程稱為 *攔截*。</span><span class="sxs-lookup"><span data-stu-id="be68b-107">This process is known as *interception*.</span></span>

<span data-ttu-id="be68b-108">跨內容呼叫攔截是必要的，因為不同內容中的物件有不同的執行時間需求，這就是內容的確切原因。</span><span class="sxs-lookup"><span data-stu-id="be68b-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="be68b-109">COM + 會攔截您傳遞做為方法參數的任何物件參考，並自動將它們轉換成 proxy，以便在新的內容中使用它們。</span><span class="sxs-lookup"><span data-stu-id="be68b-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="be68b-110">如果您透過其他方法（例如，在全域變數中）在內容界限之間共用物件參考，則應該一律使用 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) 和 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)。</span><span class="sxs-lookup"><span data-stu-id="be68b-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="be68b-111">這些函數可以將物件參考轉譯成可在不同內容中使用的 proxy。</span><span class="sxs-lookup"><span data-stu-id="be68b-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="be68b-112">絕對不要在內容界限之間共用原始物件參考。</span><span class="sxs-lookup"><span data-stu-id="be68b-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="be68b-113">當物件公開無法封送處理的介面時，跨內容的呼叫行為可能會有不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="be68b-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="be68b-114">在這種情況下，您可能會想要確保無法封送處理的物件只會在其呼叫端的內容中啟用，而且絕不會在其本身的內容中啟動。</span><span class="sxs-lookup"><span data-stu-id="be68b-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="be68b-115">您可以在 [元件 **屬性**] 頁面的 [**啟用**] 索引標籤上，選取 [**必須在呼叫者的內容中** 啟動] 選項來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="be68b-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="be68b-116"> (參閱 [在呼叫端的內容中強制啟用](enforcing-activation-in-the-caller-s-context.md) ，以取得逐步指示。 ) </span><span class="sxs-lookup"><span data-stu-id="be68b-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="be68b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="be68b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be68b-118">內容啟用</span><span class="sxs-lookup"><span data-stu-id="be68b-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
