---
description: 您可能會想要撰寫可隨時回應事件的應用程式。
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: 隨時接收事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5559068e1e108c6f4185c31f8858a9e4169c50c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318868"
---
# <a name="receiving-events-at-all-times"></a><span data-ttu-id="50ebf-103">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="50ebf-103">Receiving Events at All Times</span></span>

<span data-ttu-id="50ebf-104">您可能會想要撰寫可隨時回應事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="50ebf-104">You may want to write an application that can react to events at any time.</span></span> <span data-ttu-id="50ebf-105">例如，系統管理員可能會想要在網路伺服器上的特定效能措施拒絕時收到電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="50ebf-105">For example, an administrator may want to receive an email message when specific performance measures decline on network servers.</span></span> <span data-ttu-id="50ebf-106">在此情況下，您的應用程式應該隨時執行。</span><span class="sxs-lookup"><span data-stu-id="50ebf-106">In this case, your application should run at all times.</span></span> <span data-ttu-id="50ebf-107">不過，持續執行應用程式並不會有效率地使用系統資源。</span><span class="sxs-lookup"><span data-stu-id="50ebf-107">However, running an application continuously is not an efficient use of system resources.</span></span> <span data-ttu-id="50ebf-108">相反地，WMI 可讓您建立永久事件取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-108">Instead, WMI allows you to create a permanent event consumer.</span></span> <span data-ttu-id="50ebf-109">永久事件取用者必須符合特殊的安全性需求。</span><span class="sxs-lookup"><span data-stu-id="50ebf-109">Permanent event consumers must meet special security requirements.</span></span> <span data-ttu-id="50ebf-110">如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-110">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="50ebf-111">永久事件取用者會收到事件，直到明確取消其註冊為止。</span><span class="sxs-lookup"><span data-stu-id="50ebf-111">A permanent event consumer receives events until its registration is explicitly canceled.</span></span>

<span data-ttu-id="50ebf-112">永久事件取用者是位於您系統上的下列 WMI 類別、篩選和 COM 物件的組合：</span><span class="sxs-lookup"><span data-stu-id="50ebf-112">A permanent event consumer is a combination of the following WMI classes, filters, and COM objects that reside on your system:</span></span>

-   <span data-ttu-id="50ebf-113">稱為實體取用者的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="50ebf-113">A COM object called a physical consumer.</span></span> <span data-ttu-id="50ebf-114">WMI 提供數個標準的永久取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-114">WMI supplies several standard permanent consumers.</span></span> <span data-ttu-id="50ebf-115">例如，動態指令碼事件取用者 [會在事件發生時執行腳本](running-a-script-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-115">For example, the Active Script Event consumer [runs a script when an event occurs](running-a-script-based-on-an-event.md).</span></span>
-   <span data-ttu-id="50ebf-116">新的永久取用者類別。</span><span class="sxs-lookup"><span data-stu-id="50ebf-116">A new permanent consumer class.</span></span>
-   <span data-ttu-id="50ebf-117">永久取用者類別的實例，稱為邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-117">An instance of the permanent consumer class called a logical consumer.</span></span>
-   <span data-ttu-id="50ebf-118">包含事件查詢的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="50ebf-118">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="50ebf-119">取用者與篩選之間的連結。</span><span class="sxs-lookup"><span data-stu-id="50ebf-119">A linkage between the consumer and the filter.</span></span>

<span data-ttu-id="50ebf-120">邏輯事件取用者的屬性會指定在事件收到通知時要執行的動作，但不會定義與其相關聯的事件查詢。</span><span class="sxs-lookup"><span data-stu-id="50ebf-120">The properties of a logical event consumer specify the actions to perform when notified of an event, but do not define the event queries with which they are associated.</span></span> <span data-ttu-id="50ebf-121">當收到信號時，WMI 會自動將代表永久事件取用者的 COM 物件載入至使用中記憶體。</span><span class="sxs-lookup"><span data-stu-id="50ebf-121">When signaled, WMI automatically loads the COM object that represents the permanent event consumer into active memory.</span></span> <span data-ttu-id="50ebf-122">一般來說，這會在啟動期間或為了回應觸發的事件時發生。</span><span class="sxs-lookup"><span data-stu-id="50ebf-122">Typically, this occurs during startup or in response to a triggering event.</span></span> <span data-ttu-id="50ebf-123">在啟用之後，永久事件取用者會以一般事件取用者的形式運作，但會一直保留到作業系統特別卸載為止。</span><span class="sxs-lookup"><span data-stu-id="50ebf-123">After being activated, the permanent event consumer acts as a normal event consumer, but remains until specifically unloaded by the operating system.</span></span>

<span data-ttu-id="50ebf-124">您可以撰寫自己的永久事件取用者，或使用 WMI 預先安裝的 [標準取用者類別](standard-consumer-classes.md)，例如 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-124">You can write your own permanent event consumer or use the WMI preinstalled [Standard Consumer Classes](standard-consumer-classes.md), such as [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span> <span data-ttu-id="50ebf-125">如需詳細資訊，請參閱 [標準取用者類別](standard-consumer-classes.md)、 [使用標準取用者監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)，以及 [監視事件](monitoring-events.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-125">For more information, see [Standard Consumer Classes](standard-consumer-classes.md), [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md), and [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="50ebf-126">下列程式說明如何建立您自己的永久事件取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-126">The following procedure describes how to create your own permanent event consumer.</span></span>

<span data-ttu-id="50ebf-127">**建立您自己的永久事件取用者**</span><span class="sxs-lookup"><span data-stu-id="50ebf-127">**To create your own permanent event consumer**</span></span>

1.  <span data-ttu-id="50ebf-128">決定您想要接收的事件種類。</span><span class="sxs-lookup"><span data-stu-id="50ebf-128">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="50ebf-129">WMI 支援內部和外來事件。</span><span class="sxs-lookup"><span data-stu-id="50ebf-129">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="50ebf-130">內建事件是 WMI 預先定義的事件，而外建事件則是由協力廠商提供者所定義的事件。</span><span class="sxs-lookup"><span data-stu-id="50ebf-130">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="50ebf-131">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-131">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="50ebf-132">[實行實體取用者](implementing-a-physical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-132">[Implement a physical consumer](implementing-a-physical-consumer.md).</span></span>

    <span data-ttu-id="50ebf-133">管理應用程式與 [*實體取用者*](gloss-p.md) 之間的主要差異在於，使用者會載入和卸載管理應用程式，而 WMI 會載入和卸載實體取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-133">The main difference between a management application and a [*physical consumer*](gloss-p.md) is that a user loads and unloads a management application, whereas WMI loads and unloads a physical consumer.</span></span> <span data-ttu-id="50ebf-134">大部分的程式碼撰寫都應該在實體取用者中。</span><span class="sxs-lookup"><span data-stu-id="50ebf-134">Most of your coding should be in the physical consumer.</span></span>

    > [!Note]  
    > <span data-ttu-id="50ebf-135">此步驟會先在程式中提供簡單的說明。</span><span class="sxs-lookup"><span data-stu-id="50ebf-135">This step is first in the procedure for ease of explanation.</span></span> <span data-ttu-id="50ebf-136">就程式碼而言，您應該先實際建立實體取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-136">In terms of coding, you should actually create the physical consumer last.</span></span> <span data-ttu-id="50ebf-137">如此一來，您就可以在開始冗長的程式碼之前，為您的永久事件提供者配置參數和邏輯。</span><span class="sxs-lookup"><span data-stu-id="50ebf-137">That way you can lay out your parameters and logic for your permanent event provider before you start lengthy coding.</span></span> <span data-ttu-id="50ebf-138">但是，不會先撰寫實體取用者的限制。</span><span class="sxs-lookup"><span data-stu-id="50ebf-138">However, there is no restriction against writing the physical consumer first.</span></span>

     

3.  <span data-ttu-id="50ebf-139">[建立新的取用者類別來描述實體取用者](creating-a-new-permanent-event-consumer-class.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-139">[Create a new consumer class describing the physical consumer](creating-a-new-permanent-event-consumer-class.md).</span></span>

    <span data-ttu-id="50ebf-140">就像任何類別一樣，取用者類別會描述永久事件取用者對 WMI 的一般參數。</span><span class="sxs-lookup"><span data-stu-id="50ebf-140">Like any class, the consumer class describes the general parameters of a permanent event consumer to WMI.</span></span>

4.  <span data-ttu-id="50ebf-141">[建立取用者類別的實例](creating-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-141">[Create an instance of the consumer class](creating-a-logical-consumer.md).</span></span>

    <span data-ttu-id="50ebf-142">如同其他任何 WMI 類別，如果您想要執行類別，則必須建立取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="50ebf-142">Like any other WMI class, you must create an instance of the consumer class if you want to implement the class.</span></span> <span data-ttu-id="50ebf-143">取用者類別的實例也稱為 [*邏輯取用者*](gloss-l.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-143">An instance of a consumer class is also known as a [*logical consumer*](gloss-l.md).</span></span> <span data-ttu-id="50ebf-144">邏輯取用者代表 WMI 的實體取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-144">The logical consumer represents the physical consumer to WMI.</span></span>

5.  <span data-ttu-id="50ebf-145">[建立事件篩選準則](creating-an-event-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-145">[Create an event filter](creating-an-event-filter.md).</span></span>

    <span data-ttu-id="50ebf-146">啟用永久事件取用者的事件查詢稱為「 [*事件篩選準則*](gloss-e.md)」。</span><span class="sxs-lookup"><span data-stu-id="50ebf-146">The event queries that activate permanent event consumers are called [*event filters*](gloss-e.md).</span></span> <span data-ttu-id="50ebf-147">單一事件篩選器可以與多個邏輯事件取用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="50ebf-147">A single event filter can be associated with multiple logical event consumers.</span></span> <span data-ttu-id="50ebf-148">此外，多個事件篩選器可以與單一邏輯事件取用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="50ebf-148">Furthermore, multiple event filters can be associated with a single logical event consumer.</span></span> <span data-ttu-id="50ebf-149">篩選是 [**\_ \_ >eventfilter**](--eventfilter.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="50ebf-149">The filter is an instance of [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="50ebf-150">當永久性事件取用者的查詢失敗時，就會產生 NT 記錄事件。</span><span class="sxs-lookup"><span data-stu-id="50ebf-150">An NT Log event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="50ebf-151">事件的來源為 WinMgmt，事件識別碼為10，而事件種類為「錯誤」。</span><span class="sxs-lookup"><span data-stu-id="50ebf-151">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="50ebf-152">將[事件篩選器連結至邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-152">[Link the event filter to the logical consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="50ebf-153">藉由將事件篩選器連結至邏輯取用者，您可以指示 WMI 哪些事件篩選器屬於哪個邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-153">By linking the event filter to the logical consumer, you instruct WMI about which event filter belongs to which logical consumer.</span></span> <span data-ttu-id="50ebf-154">邏輯事件取用者和事件篩選器會透過 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的關聯類別實例來連結。</span><span class="sxs-lookup"><span data-stu-id="50ebf-154">Logical event consumers and event filters are linked by an association class instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md).</span></span> <span data-ttu-id="50ebf-155">當收到的事件符合事件篩選器中所述的事件查詢時，WMI 會藉由查看關聯類別實例來尋找相關聯的邏輯事件取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-155">When an event is received that matches an event query described in an event filter, WMI finds the associated logical event consumer by looking at the association class instance.</span></span> <span data-ttu-id="50ebf-156">在邏輯事件取用者實例找到之後，WMI 會使用 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)類別的實例來尋找並執行與此實例相關聯的實體事件取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-156">After the logical event consumer instance is located, WMI uses an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class to locate and run the physical event consumer associated with this instance.</span></span>

7.  <span data-ttu-id="50ebf-157">[撰寫事件取用者提供者](writing-an-event-consumer-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="50ebf-157">[Writing an event consumer provider](writing-an-event-consumer-provider.md).</span></span>

    <span data-ttu-id="50ebf-158">事件取用者提供者是 COM 物件，可尋找 WMI 的實體取用者。</span><span class="sxs-lookup"><span data-stu-id="50ebf-158">The event consumer provider is a COM object that locates the physical consumer for WMI.</span></span>

 

 



