---
description: 已設定的 COM 元件通常會在其本身的內容中啟用;亦即，COM + 會參考元件類別目錄資訊，以提供任何已設定的服務。
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: 在預設內容中強制啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510752"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="218a2-103">在預設內容中強制啟用</span><span class="sxs-lookup"><span data-stu-id="218a2-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="218a2-104">已設定的 COM 元件通常會在其本身的內容中啟用;亦即，COM + 會參考元件的類別目錄資訊，以提供任何已設定的服務。</span><span class="sxs-lookup"><span data-stu-id="218a2-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="218a2-105">不過，您可以選擇在預設內容中啟用已設定的元件。</span><span class="sxs-lookup"><span data-stu-id="218a2-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="218a2-106">基底 COM 元件（沒有 COM + 類別目錄資訊的已註冊元件）通常會在預設內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="218a2-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="218a2-107">啟用預設內容中的 COM 元件提供三個主要的效能優點，如下所示：</span><span class="sxs-lookup"><span data-stu-id="218a2-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="218a2-108">您可以藉由限制所建立的內容數目來節省系統資源。</span><span class="sxs-lookup"><span data-stu-id="218a2-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="218a2-109">您可以藉由限制跨內容呼叫的數目來提高效能。</span><span class="sxs-lookup"><span data-stu-id="218a2-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="218a2-110">因為跨內容的呼叫需要封送處理，所以在預設內容中啟動的 COM 物件會更快地對預設內容中的其他物件進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="218a2-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="218a2-111">在此情況下， (在相同內容中呼叫的效能，) 類似于呼叫副程式。</span><span class="sxs-lookup"><span data-stu-id="218a2-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="218a2-112">您可以將較舊的 COM 應用程式匯入至 COM +，並在沒有問題的情況下執行</span><span class="sxs-lookup"><span data-stu-id="218a2-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="218a2-113">例如，您可能會有數個舊版的 COM 應用程式，但前提是允許它在一個單元內傳遞物件參考，而不需要封送處理參考。</span><span class="sxs-lookup"><span data-stu-id="218a2-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="218a2-114">當匯入至 COM + 時，這些 COM 應用程式無法運作，因為物件參考會跨內容界限傳遞。</span><span class="sxs-lookup"><span data-stu-id="218a2-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="218a2-115">但是，如果您使用 [元件服務] 系統管理工具，將應用程式中的所有類別標示為 **必須在預設內容中** 啟動，您可以在匯入時執行這種類型的 COM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="218a2-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="218a2-116">在預設內容中啟用已設定元件的主要缺點是，COM + 並未提供任何元件的設定服務。</span><span class="sxs-lookup"><span data-stu-id="218a2-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="218a2-117">在增強的效能與使用 COM + 服務的能力之間，會有所取捨。</span><span class="sxs-lookup"><span data-stu-id="218a2-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="218a2-118">例如，假設 COM 元件不需要任何 COM + 服務 (例如 [交易](com--transactions.md)、 [即時啟用](com--just-in-time-activation.md)、 [事件](com--events.md)、 [佇列元件](com--queued-components.md)、 [同步](com--synchronization.md)處理或 [物件](com--object-pooling.md) 共用) ，而且元件會對其他可能在預設內容中啟用的 COM 元件進行一些呼叫。</span><span class="sxs-lookup"><span data-stu-id="218a2-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="218a2-119">在此情況下，在預設內容中啟動呼叫元件是個不錯的主意。</span><span class="sxs-lookup"><span data-stu-id="218a2-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="218a2-120">如果 COM 元件需要 COM + 服務，則無法將它標示為 **必須在預設內容中啟用**。</span><span class="sxs-lookup"><span data-stu-id="218a2-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="218a2-121">此外，如果在預設內容中啟動的 COM 物件會對其他內容中的物件進行一些呼叫，則沒有真正的效能提升。</span><span class="sxs-lookup"><span data-stu-id="218a2-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="218a2-122"> (需詳細資訊，請 [參閱內容](com--contexts.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="218a2-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="218a2-123">**在預設內容中強制啟用**</span><span class="sxs-lookup"><span data-stu-id="218a2-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="218a2-124">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠右鍵按一下 [元件] (位於您要在預設內容中啟動之任何選取 COM + 應用程式) 的 [ **元件** ] 資料夾中，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="218a2-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="218a2-125">在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="218a2-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="218a2-126">選取 [ **必須在預設內容中啟用**] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="218a2-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="218a2-127">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="218a2-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="218a2-128">當您在預設內容中執行已設定的元件時，COM + 不會針對該元件啟動任何已設定的服務。</span><span class="sxs-lookup"><span data-stu-id="218a2-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="218a2-129">當您取消核取 [ **必須在預設內容中啟用**] 核取方塊，然後在其本身的內容中執行設定的元件時，就可以再次使用這些服務。</span><span class="sxs-lookup"><span data-stu-id="218a2-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="218a2-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="218a2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="218a2-131">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="218a2-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="218a2-132">在呼叫端的內容中強制啟用</span><span class="sxs-lookup"><span data-stu-id="218a2-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



