---
description: COM + 執行緒模型是設計在名為一個單元的物件集合周圍。 一個單元是包含在進程中的內容集合。
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: COM + 執行緒模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "103696035"
---
# <a name="com-threading-models"></a><span data-ttu-id="7058f-104">COM + 執行緒模型</span><span class="sxs-lookup"><span data-stu-id="7058f-104">COM+ Threading Models</span></span>

<span data-ttu-id="7058f-105">COM + 執行緒模型是設計在名為一個單元的物件集合周圍。</span><span class="sxs-lookup"><span data-stu-id="7058f-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="7058f-106">一個單元是包含在進程中的內容集合，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="7058f-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![此圖表顯示進程內活動中的內容集合。](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="7058f-108">在一個單元內的呼叫是直接的，而跨 (跨進程的) 則是間接的，且需要 proxy 和存根程式碼。</span><span class="sxs-lookup"><span data-stu-id="7058f-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="7058f-109">單元允許具有不同同步處理和重新進入屬性的物件，且有兩個類別：單一執行緒和多執行緒。</span><span class="sxs-lookup"><span data-stu-id="7058f-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="7058f-110">單一執行緒單元中的物件 (STA) 在其建立所在的特定執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="7058f-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="7058f-111">Sta 一次只允許一個方法執行。</span><span class="sxs-lookup"><span data-stu-id="7058f-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="7058f-112">它們是專為使用者介面所設計，並依賴 Microsoft Windows 訊息佇列來處理傳入的呼叫。</span><span class="sxs-lookup"><span data-stu-id="7058f-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="7058f-113">多執行緒單元中的物件 (MTA) 在任何執行緒上執行，並允許任何數目的方法同時發生。</span><span class="sxs-lookup"><span data-stu-id="7058f-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="7058f-114">Mta 支援隱含 reentrance。</span><span class="sxs-lookup"><span data-stu-id="7058f-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="7058f-115">COM + 類別會以 **>threadingmodel** 屬性標記，可讓 com + 在適當的單元中建立物件。</span><span class="sxs-lookup"><span data-stu-id="7058f-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="7058f-116">為了判斷要在其中建立物件的單元， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 會使用 **>threadingmodel** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7058f-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="7058f-117">執行緒必須先呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ，才能使用 com +。</span><span class="sxs-lookup"><span data-stu-id="7058f-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="7058f-118">這會在正確的單元和內容中建立它們。</span><span class="sxs-lookup"><span data-stu-id="7058f-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="7058f-119">主要執行緒的單元會被判斷為 **CoInitializeEx** 所呼叫的第一個 STA。</span><span class="sxs-lookup"><span data-stu-id="7058f-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="7058f-120">這通常與進程的主執行緒相關聯。</span><span class="sxs-lookup"><span data-stu-id="7058f-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="7058f-121">**CoInitializeEx** 藉由設定下列旗標，指出執行緒所需的單元類型：</span><span class="sxs-lookup"><span data-stu-id="7058f-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="7058f-122">**COINIT \_多執行緒**-在單一多執行緒單元中尋找執行緒。</span><span class="sxs-lookup"><span data-stu-id="7058f-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="7058f-123">**COINIT \_APARTMENTTHREADED**：將執行緒放入新的 STA 中。</span><span class="sxs-lookup"><span data-stu-id="7058f-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="7058f-124">本節中的下列主題提供有關在 COM + 中使用執行緒模型和單元的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="7058f-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="7058f-125">執行緒模型屬性</span><span class="sxs-lookup"><span data-stu-id="7058f-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="7058f-126">中性單元</span><span class="sxs-lookup"><span data-stu-id="7058f-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="7058f-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="7058f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7058f-128">進程、執行緒和單元</span><span class="sxs-lookup"><span data-stu-id="7058f-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="7058f-129">**>threadingmodel**</span><span class="sxs-lookup"><span data-stu-id="7058f-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
