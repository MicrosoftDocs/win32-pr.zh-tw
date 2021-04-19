---
description: 事件提供者是一種 COM 物件，其提供內建和外來事件通知的 WMI。
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: 撰寫事件提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981514"
---
# <a name="writing-an-event-provider"></a><span data-ttu-id="957cd-103">撰寫事件提供者</span><span class="sxs-lookup"><span data-stu-id="957cd-103">Writing an Event Provider</span></span>

<span data-ttu-id="957cd-104">事件提供者是一種 COM 物件，其提供內建和外來事件通知的 WMI。</span><span class="sxs-lookup"><span data-stu-id="957cd-104">An event provider is a COM object that supplies WMI with notifications of intrinsic and extrinsic events.</span></span> <span data-ttu-id="957cd-105">內建事件會報告內部資料變更至 WMI，而外建事件則會報告未由內建事件描述的使用者定義事件。</span><span class="sxs-lookup"><span data-stu-id="957cd-105">An intrinsic event reports an internal data change to WMI, while an extrinsic event reports a user-defined event not described by an intrinsic event.</span></span> <span data-ttu-id="957cd-106">例如，回應變更、建立或刪除 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的事件會分類為內部事件。</span><span class="sxs-lookup"><span data-stu-id="957cd-106">For example, an event in response to changes, creation, or deletion of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class would classify as an intrinsic event.</span></span> <span data-ttu-id="957cd-107">基於修改、建立或刪除現有 WMI 物件以外的其他專案所產生的事件，是外來事件。</span><span class="sxs-lookup"><span data-stu-id="957cd-107">An event that is generated on the basis of something other than the modification, creation, or deletion of an existing WMI object is an extrinsic event.</span></span> <span data-ttu-id="957cd-108">不論支援的類別為何，您都可以用相同的方式來執行所有事件提供者。</span><span class="sxs-lookup"><span data-stu-id="957cd-108">Regardless of the supported class, you can implement all event providers in the same manner.</span></span>

<span data-ttu-id="957cd-109">下列程式描述如何執行事件提供者。</span><span class="sxs-lookup"><span data-stu-id="957cd-109">The following procedure describes how to implement an event provider.</span></span>

<span data-ttu-id="957cd-110">**若要執行事件提供者**</span><span class="sxs-lookup"><span data-stu-id="957cd-110">**To implement an event provider**</span></span>

1.  <span data-ttu-id="957cd-111">使用 WMI 設計和註冊您的類別提供者。</span><span class="sxs-lookup"><span data-stu-id="957cd-111">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="957cd-112">類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別，向 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="957cd-112">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span> <span data-ttu-id="957cd-113">如需詳細資訊，請參閱 [註冊事件提供者](registering-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-113">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

2.  <span data-ttu-id="957cd-114">為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。</span><span class="sxs-lookup"><span data-stu-id="957cd-114">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="957cd-115">[**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)介面是 WMI 用來載入和初始化所有提供者的通用介面。</span><span class="sxs-lookup"><span data-stu-id="957cd-115">The [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface is a common interface WMI uses to load and initialize all providers.</span></span> <span data-ttu-id="957cd-116">如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-116">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

3.  <span data-ttu-id="957cd-117">將 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 實作為提供者的主要介面。</span><span class="sxs-lookup"><span data-stu-id="957cd-117">Implement the [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) as the primary interface for your provider.</span></span>

    <span data-ttu-id="957cd-118">[**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)介面會使用 **ProviderEvents** 方法將事件提供給 WMI。</span><span class="sxs-lookup"><span data-stu-id="957cd-118">The [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interface uses the **ProviderEvents** method to supply events to WMI.</span></span> <span data-ttu-id="957cd-119">如需詳細資訊，請參閱 [執行事件提供者的主要介面](implementing-the-primary-interface-for-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-119">For more information, see [Implementing the Primary Interface for an Event Provider](implementing-the-primary-interface-for-an-event-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="957cd-120">事件提供者必須使用多執行緒模型「兩者」。</span><span class="sxs-lookup"><span data-stu-id="957cd-120">Event providers must use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="957cd-121">（選擇性）您也可以執行 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) 介面，以增加事件提供者的效能。</span><span class="sxs-lookup"><span data-stu-id="957cd-121">Optionally, you may also implement the [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) interface to increase the performance of your event provider.</span></span>

    <span data-ttu-id="957cd-122">[**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)介面允許提供者在將回應傳送至 WMI 之前將查詢優化，而且對於提供多個類型之事件以及需要盡可能執行最多內部優化的提供者而言，最有用。</span><span class="sxs-lookup"><span data-stu-id="957cd-122">The [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) interface allows the provider to optimize queries before sending a response to WMI, and is most useful for a provider that supplies events of multiple types and that needs to perform as many internal optimizations as possible.</span></span> <span data-ttu-id="957cd-123">如需詳細資訊，請參閱 [優化事件提供者](optimizing-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-123">For more information, see [Optimizing an Event Provider](optimizing-an-event-provider.md).</span></span>

5.  <span data-ttu-id="957cd-124">執行 [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) 介面，將取用者限制為 (sid) 或執行 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) 以保護接收器本身的特定安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="957cd-124">Implement the [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) interface to limit consumers to certain security identifiers (SIDs) or implement [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) to secure the sink itself.</span></span> <span data-ttu-id="957cd-125">提供者也可以設定事件類別中的 **安全 \_ 描述項** 屬性，以保護 MOF 程式碼中的個別事件。</span><span class="sxs-lookup"><span data-stu-id="957cd-125">The provider can also set the **SECURITY\_DESCRIPTOR** property in the event class to secure individual events in the MOF code.</span></span> <span data-ttu-id="957cd-126">如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-126">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>
6.  <span data-ttu-id="957cd-127">加入提供者所需的任何其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="957cd-127">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="957cd-128">設計提供者時，您很可能需要呼叫 WMI 介面。</span><span class="sxs-lookup"><span data-stu-id="957cd-128">When designing your provider, you most likely need to call WMI interfaces.</span></span> <span data-ttu-id="957cd-129">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="957cd-130">取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="957cd-130">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="957cd-131">如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-131">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

7.  <span data-ttu-id="957cd-132">以您的新程式碼取代預先存在的提供者。</span><span class="sxs-lookup"><span data-stu-id="957cd-132">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="957cd-133">如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="957cd-133">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="957cd-134">如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-134">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

<span data-ttu-id="957cd-135">用戶端應用程式可以透過將 WMI 註冊為事件取用者的方式來要求事件。</span><span class="sxs-lookup"><span data-stu-id="957cd-135">A client application can request an event by registering itself with WMI as an event consumer.</span></span> <span data-ttu-id="957cd-136">如需詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="957cd-136">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 
