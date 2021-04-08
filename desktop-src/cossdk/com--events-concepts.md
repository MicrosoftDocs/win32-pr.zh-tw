---
description: COM + 事件概念
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: COM + 事件概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689220"
---
# <a name="com-events-concepts"></a><span data-ttu-id="c088b-103">COM + 事件概念</span><span class="sxs-lookup"><span data-stu-id="c088b-103">COM+ Events Concepts</span></span>

<span data-ttu-id="c088b-104">COM + 事件服務是一個自動、 *鬆散結合的事件* 系統，可將來自不同發行者的事件資訊儲存在 com + 目錄中。</span><span class="sxs-lookup"><span data-stu-id="c088b-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="c088b-105">訂閱者可以查詢此事件存放區，並選取想要聽取的事件。</span><span class="sxs-lookup"><span data-stu-id="c088b-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="c088b-106">*事件* 是由 com + 介面中的方法所識別（稱為 *事件方法*），並由發行者發出，並透過 com + 事件服務分派給正確的訂閱者或訂閱者。</span><span class="sxs-lookup"><span data-stu-id="c088b-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="c088b-107">事件方法必須是唯一的名稱，而且只能包含輸入參數 (沒有任何輸出或輸入/輸出參數) 。</span><span class="sxs-lookup"><span data-stu-id="c088b-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="c088b-108">傳回值必須是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c088b-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="c088b-109">COM + 事件服務會處理發行者和訂閱者的大部分事件語義。</span><span class="sxs-lookup"><span data-stu-id="c088b-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="c088b-110">發行者會提供發佈事件種類和訂閱者要求發行者的事件種類。</span><span class="sxs-lookup"><span data-stu-id="c088b-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="c088b-111">不同于 *緊密結合的事件* 系統（發行者必須直接處理呼叫訂閱者的額外負荷），com + 事件服務會維護 com + 目錄中的訂閱資料，而不受發行者和訂閱者的影響。</span><span class="sxs-lookup"><span data-stu-id="c088b-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="c088b-112">這會簡化發行者和訂閱者的程式設計模型，因為 COM + 訂閱者元件不需要包含建立訂閱的邏輯。</span><span class="sxs-lookup"><span data-stu-id="c088b-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="c088b-113">由於 COM + 事件訂閱資料的生命週期與「發行者」或「訂閱者」的存留期不同，因此可以在「訂閱者」或「發行者」應用程式為作用中之前建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="c088b-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="c088b-114">這也表示可以另外開發和部署發行者和訂閱者。</span><span class="sxs-lookup"><span data-stu-id="c088b-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="c088b-115">您可以撰寫發行者，而不知道訂閱者的數目和位置。</span><span class="sxs-lookup"><span data-stu-id="c088b-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="c088b-116">訂閱者會使用 COM + 事件服務來尋找發行者及管理其訂閱。</span><span class="sxs-lookup"><span data-stu-id="c088b-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="c088b-117">本章節中的下列主題提供有關 COM + 事件服務核心元素的詳細資訊，以及如何使用這些專案。</span><span class="sxs-lookup"><span data-stu-id="c088b-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="c088b-118">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="c088b-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="c088b-119">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="c088b-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="c088b-120">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="c088b-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="c088b-121">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="c088b-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="c088b-122">使用 com + 事件與 COM + 佇列元件</span><span class="sxs-lookup"><span data-stu-id="c088b-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="c088b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c088b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c088b-124">COM + 事件安全性考慮</span><span class="sxs-lookup"><span data-stu-id="c088b-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="c088b-125">COM + 事件工作</span><span class="sxs-lookup"><span data-stu-id="c088b-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



