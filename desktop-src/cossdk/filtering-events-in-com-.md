---
description: COM + 事件提供兩種方式來控制哪些事件可抵達哪些訂閱者：發行者篩選和參數篩選。
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: 在 COM + 中篩選事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689108"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="244ef-103">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="244ef-103">Filtering Events in COM+</span></span>

<span data-ttu-id="244ef-104">COM + 事件提供兩種方式來控制哪些事件可抵達哪些訂閱者： *發行者篩選* 和 *參數篩選*。</span><span class="sxs-lookup"><span data-stu-id="244ef-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="244ef-105">發行者篩選</span><span class="sxs-lookup"><span data-stu-id="244ef-105">Publisher Filtering</span></span>

<span data-ttu-id="244ef-106">發行者篩選會依據 [事件類別](the-com--event-class-object.md) 物件，控制事件方法的順序和引發。</span><span class="sxs-lookup"><span data-stu-id="244ef-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="244ef-107">發行者篩選可讓發行者判斷哪些訂閱者會收到特定的事件。</span><span class="sxs-lookup"><span data-stu-id="244ef-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="244ef-108">發行者篩選的有效使用範例是股票交換。</span><span class="sxs-lookup"><span data-stu-id="244ef-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="244ef-109">大部分的訂閱者都想要知道何時新增股票。</span><span class="sxs-lookup"><span data-stu-id="244ef-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="244ef-110">但是，其中許多相同的訂閱者可能不想要在每次股價變更時都知道。</span><span class="sxs-lookup"><span data-stu-id="244ef-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="244ef-111">「發行者篩選」提供將事件有效傳遞給只需要此資訊的「訂閱者」所需的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="244ef-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="244ef-112">在具現化事件類別物件上叫用方法時，它會收集該方法上的任何發行者篩選準則。</span><span class="sxs-lookup"><span data-stu-id="244ef-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="244ef-113">篩選準則會強制事件物件將事件方法引發至特定的訂閱者。</span><span class="sxs-lookup"><span data-stu-id="244ef-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="244ef-114">篩選準則會決定要引發哪些訂用帳戶，以及要引發這些訂閱的順序。</span><span class="sxs-lookup"><span data-stu-id="244ef-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="244ef-115">例如，篩選器可以讀取訂用帳戶清單，並根據某些應用程式準則建立訂單，然後依該順序呼叫「訂閱者」。</span><span class="sxs-lookup"><span data-stu-id="244ef-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="244ef-116">如需建立發行者篩選準則的詳細指示，請參閱 [建立發行者篩選](creating-a-publisher-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="244ef-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="244ef-117">參數篩選</span><span class="sxs-lookup"><span data-stu-id="244ef-117">Parameter Filtering</span></span>

<span data-ttu-id="244ef-118">相較于發行者篩選，COM + 事件服務會針對每個訂閱及每個事件方法調用，提供選擇性的訂閱者參數篩選。</span><span class="sxs-lookup"><span data-stu-id="244ef-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="244ef-119">參數篩選會根據事件方法的參數來評估訂閱 >filtercriteria 屬性。</span><span class="sxs-lookup"><span data-stu-id="244ef-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="244ef-120">這種類型的篩選適用于個別方法、每個訂用帳戶，並在事件來源提供訂閱者篩選層級。</span><span class="sxs-lookup"><span data-stu-id="244ef-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="244ef-121">篩選準則字串會辨識檢查相等 (=、= =、!,! =、~、~ =、 <>) 、嵌套括弧和邏輯關鍵字 **and**、 **or** 或 **NOT** 的關係運算子。</span><span class="sxs-lookup"><span data-stu-id="244ef-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="244ef-122">參數篩選會在任何發行者篩選之後，以及針對指定的訂用帳戶引發標準事件物件時進行。</span><span class="sxs-lookup"><span data-stu-id="244ef-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="244ef-123">如果使用發行者篩選，只有當發行者篩選準則叫用 [**IFiringControl：： FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription)時，才會進行參數篩選。</span><span class="sxs-lookup"><span data-stu-id="244ef-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="244ef-124">基於這個原因，發行者篩選和參數篩選可以一起撰寫，但發行者篩選會優先使用。</span><span class="sxs-lookup"><span data-stu-id="244ef-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="244ef-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="244ef-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="244ef-126">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="244ef-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="244ef-127">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="244ef-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="244ef-128">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="244ef-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="244ef-129">使用 com + 事件與 COM + 佇列元件</span><span class="sxs-lookup"><span data-stu-id="244ef-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



