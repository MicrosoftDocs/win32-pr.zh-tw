---
description: 開發成功的 COM + 應用程式需要預先設計的應用程式架構。
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: 使用 UML 設計 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385919"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="b0057-103">使用 UML 設計 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="b0057-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="b0057-104">開發成功的 COM + 應用程式需要預先設計的應用程式架構。</span><span class="sxs-lookup"><span data-stu-id="b0057-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="b0057-105">整合模組化語言 (UML) 是此設計開發的關鍵。</span><span class="sxs-lookup"><span data-stu-id="b0057-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="b0057-106">UML 是一種模型化標記法，適用于結合軟體產業最佳作法的應用程式資料和流程。</span><span class="sxs-lookup"><span data-stu-id="b0057-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="b0057-107">由於 UML 會將應用程式分成三個可反映應用程式的視圖，以及它的封裝和執行，因此模型化標記法可妥善擴充以支援企業模型化。</span><span class="sxs-lookup"><span data-stu-id="b0057-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="b0057-108">UML 會解決應用程式的三個觀點，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b0057-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="b0057-109">靜態視圖，以使用者案例和類別圖所採用的資訊來建立模型。</span><span class="sxs-lookup"><span data-stu-id="b0057-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="b0057-110">動態視圖，使用順序、共同作業和狀態轉換圖表進行模型化。</span><span class="sxs-lookup"><span data-stu-id="b0057-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="b0057-111">功能視圖，這是使用虛擬程式碼和規格的較傳統描述性敘述。</span><span class="sxs-lookup"><span data-stu-id="b0057-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="b0057-112">這些視圖的資訊可透過下列三個可搭配 UML 運作的設計步驟來收集。</span><span class="sxs-lookup"><span data-stu-id="b0057-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="b0057-113">撰寫一行程式碼之前，您必須先建立下列模型：</span><span class="sxs-lookup"><span data-stu-id="b0057-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="b0057-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>概念模型</span><span class="sxs-lookup"><span data-stu-id="b0057-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="b0057-115">決定需要哪些元件和服務。</span><span class="sxs-lookup"><span data-stu-id="b0057-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="b0057-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>邏輯模型</span><span class="sxs-lookup"><span data-stu-id="b0057-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="b0057-117">判斷它們所屬的邏輯設計層。</span><span class="sxs-lookup"><span data-stu-id="b0057-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="b0057-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>實體模型</span><span class="sxs-lookup"><span data-stu-id="b0057-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="b0057-119">判斷元件的實際位置，以及它們的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="b0057-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="b0057-120">然後，這些模型可以搭配以 UML 為基礎的案例工具使用。</span><span class="sxs-lookup"><span data-stu-id="b0057-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="b0057-121">如需這三種設計模型的詳細資訊，請參閱本節中的下列主題：</span><span class="sxs-lookup"><span data-stu-id="b0057-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="b0057-122">概念模型：應用程式需求</span><span class="sxs-lookup"><span data-stu-id="b0057-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="b0057-123">邏輯模型：應用程式定義和規劃</span><span class="sxs-lookup"><span data-stu-id="b0057-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="b0057-124">實體模型：應用程式架構</span><span class="sxs-lookup"><span data-stu-id="b0057-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="b0057-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0057-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0057-126">COM + 設計假設和原則</span><span class="sxs-lookup"><span data-stu-id="b0057-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="b0057-127">使用 COM + 的一般設計秘訣</span><span class="sxs-lookup"><span data-stu-id="b0057-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="b0057-128">優化與 COM + 商務邏輯層的互動</span><span class="sxs-lookup"><span data-stu-id="b0057-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="b0057-129">用來建立分散式應用程式的其他 Microsoft 工具</span><span class="sxs-lookup"><span data-stu-id="b0057-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



