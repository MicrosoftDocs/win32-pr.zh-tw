---
description: 事件取用者提供者是永久取用者架構的元件，可判斷哪個永久性事件取用者會處理指定的事件。
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: 撰寫事件取用者提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982486"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="ee213-103">撰寫事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="ee213-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="ee213-104">事件取用者提供者是永久取用者架構的元件，可判斷哪個永久性事件取用者會處理指定的事件。</span><span class="sxs-lookup"><span data-stu-id="ee213-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="ee213-105">您應建立事件取用者提供者以及永久事件取用者，以正確地從 WMI 路由事件。</span><span class="sxs-lookup"><span data-stu-id="ee213-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="ee213-106">事件取用者提供者會連結事件提供者與取用者類別清單。</span><span class="sxs-lookup"><span data-stu-id="ee213-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="ee213-107">然後，這些取用者類別的實例會接收來自該提供者的事件。</span><span class="sxs-lookup"><span data-stu-id="ee213-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="ee213-108">WMI 會根據 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)實例來識別傳遞事件的取用者提供者，這會將取用者提供者 [**\_ \_ Win32Provider**](--win32provider.md)實例與邏輯取用者類別產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ee213-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="ee213-109">使用者會在永久訂用帳戶中建立取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ee213-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="ee213-110">如果事件發生時，事件提供者未執行，則 WMI 會在需要傳遞事件時啟動提供者。</span><span class="sxs-lookup"><span data-stu-id="ee213-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="ee213-111">下列程式描述如何執行事件取用者提供者。</span><span class="sxs-lookup"><span data-stu-id="ee213-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="ee213-112">**若要執行事件取用者提供者**</span><span class="sxs-lookup"><span data-stu-id="ee213-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="ee213-113">在受控物件格式 (MOF) 中設計取用者類別，並向 WMI 註冊它們。</span><span class="sxs-lookup"><span data-stu-id="ee213-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="ee213-114">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="ee213-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="ee213-115">類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)類別，向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="ee213-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="ee213-116">如需詳細資訊，請參閱 [註冊事件取用者提供者](registering-an-event-consumer-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ee213-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="ee213-117">為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="ee213-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="ee213-118">WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="ee213-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="ee213-119">如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ee213-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="ee213-120">強烈建議您使用多執行緒模型「兩者」的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="ee213-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="ee213-121">為您的提供者執行 [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="ee213-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="ee213-122">[**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)介面是事件取用者提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="ee213-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="ee213-123">提供一或多個實體取用者，以接收來自 WMI 的事件訊息。</span><span class="sxs-lookup"><span data-stu-id="ee213-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="ee213-124">實體取用者是代表永久事件取用者的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ee213-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="ee213-125">所有實體取用者都必須執行 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) 介面。</span><span class="sxs-lookup"><span data-stu-id="ee213-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="ee213-126">如需詳細資訊，請參閱實 [作為實體取用者](implementing-a-physical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="ee213-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



