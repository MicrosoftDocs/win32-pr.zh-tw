---
description: 實體取用者是可實 IWbemUnboundObjectSink 介面的 COM 物件。
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: 執行實體取用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0a9530ed7a98ce19b3b39f2f5a1fe52f3b0631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000300"
---
# <a name="implementing-a-physical-consumer"></a><span data-ttu-id="06da9-103">執行實體取用者</span><span class="sxs-lookup"><span data-stu-id="06da9-103">Implementing a Physical Consumer</span></span>

<span data-ttu-id="06da9-104">實體取用者是可實 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="06da9-104">A physical consumer is a COM object that implements the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="06da9-105">WMI 會載入您的實體取用者，並透過 **IWbemUnboundObjectSink** 傳遞事件，以回應一或多個事件（如相關聯的邏輯取用者所定義）。</span><span class="sxs-lookup"><span data-stu-id="06da9-105">WMI loads your physical consumer and passes events through **IWbemUnboundObjectSink** in response to one or more events, as defined by the associated logical consumer.</span></span> <span data-ttu-id="06da9-106">永久取用者具有特殊的安全性需求。</span><span class="sxs-lookup"><span data-stu-id="06da9-106">Permanent consumers have special security requirements.</span></span> <span data-ttu-id="06da9-107">如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="06da9-107">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="06da9-108">下列程式說明如何為永久事件取用者執行實體取用者。</span><span class="sxs-lookup"><span data-stu-id="06da9-108">The following procedure describes how to implement a physical consumer for a permanent event consumer.</span></span>

<span data-ttu-id="06da9-109">**若要為永久事件取用者執行實體取用者**</span><span class="sxs-lookup"><span data-stu-id="06da9-109">**To implement a physical consumer for a permanent event consumer**</span></span>

1.  <span data-ttu-id="06da9-110">建立 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="06da9-110">Create a COM object.</span></span>

    <span data-ttu-id="06da9-111">您必須使用 COM 通訊協定，將實體取用者實作為本機或遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="06da9-111">You must implement a physical consumer as a local or remote server using the COM protocol.</span></span>

2.  <span data-ttu-id="06da9-112">判斷您是否要支援同步或非同步事件通知。</span><span class="sxs-lookup"><span data-stu-id="06da9-112">Determine if you want to support synchronous or asynchronous event notification.</span></span>

    <span data-ttu-id="06da9-113">使用非同步事件通知時，傳送執行緒與接收執行緒無關。</span><span class="sxs-lookup"><span data-stu-id="06da9-113">With asynchronous event notification, the sending thread is unrelated to the receiving thread.</span></span> <span data-ttu-id="06da9-114">因此，當 WMI 將通知傳遞給任何已註冊要接收事件的取用者時，WMI 和事件提供者都不會遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="06da9-114">Therefore, neither WMI nor the event provider gets blocked while WMI delivers a notification to any consumer registered to receive the event.</span></span> <span data-ttu-id="06da9-115">非同步傳遞的缺點是，在提供者產生事件和取用者收到事件之間的時間之間，會發生內容切換。</span><span class="sxs-lookup"><span data-stu-id="06da9-115">The disadvantage to asynchronous delivery is that a context switch occurs between the time the provider produces the event and the time the consumer receives the event.</span></span> <span data-ttu-id="06da9-116">如需以非同步方式工作的詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的 COM 章節中的 [Com 基本](../com/guide.md) 概念主題。</span><span class="sxs-lookup"><span data-stu-id="06da9-116">For more information about working asynchronously, see the [COM Fundamentals](../com/guide.md) topic in the COM section of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="06da9-117">如需內容切換的詳細資訊，請參閱 Windows SDK 之 Dll、進程和執行緒一節中的 [內容切換](../procthread/context-switches.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="06da9-117">For more information about context switches, see the [Context Switches](../procthread/context-switches.md) topic in the DLLs, Processes, and Threads section of the Windows SDK.</span></span>

    > [!Note]  
    > <span data-ttu-id="06da9-118">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="06da9-118">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="06da9-119">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="06da9-119">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

    <span data-ttu-id="06da9-120">透過同步通知，WMI 會在事件提供者用來將事件傳遞至 WMI 的相同執行緒上傳遞通知。</span><span class="sxs-lookup"><span data-stu-id="06da9-120">With synchronous notification, WMI delivers the notification on the same thread that the event provider used to deliver the event to WMI.</span></span> <span data-ttu-id="06da9-121">在此情況下，當事件提供者傳送通知時，WMI 會封鎖事件提供者，直到 WMI 傳遞通知為止。</span><span class="sxs-lookup"><span data-stu-id="06da9-121">In this case, when an event provider sends a notification, the event provider is blocked by WMI until WMI delivers the notification.</span></span> <span data-ttu-id="06da9-122">只有當您的取用者非常快速，而且可以在100微秒內處理事件，您應該考慮支援同步通知。</span><span class="sxs-lookup"><span data-stu-id="06da9-122">Only if your consumer is extremely fast and can process an event in 100 microseconds or less should you consider supporting synchronous notification.</span></span> <span data-ttu-id="06da9-123">花費太長時間處理事件的同步取用者可能會嚴重降低將事件傳遞給所有其他取用者的速度。</span><span class="sxs-lookup"><span data-stu-id="06da9-123">Synchronous consumers that take too long to process events can seriously slow the delivery of events to all other consumers.</span></span> <span data-ttu-id="06da9-124">此外，它們可能會不慎封鎖提供者。</span><span class="sxs-lookup"><span data-stu-id="06da9-124">Furthermore, they can inadvertently block the provider.</span></span> <span data-ttu-id="06da9-125">如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="06da9-125">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

3.  <span data-ttu-id="06da9-126">執行 [**IWbemUnboundObjectSink：： IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) 函數。</span><span class="sxs-lookup"><span data-stu-id="06da9-126">Implement the [**IWbemUnboundObjectSink::IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) function.</span></span>

    <span data-ttu-id="06da9-127">WMI 使用 [**IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) 函式，將必要的指標和事件傳遞給您的實體取用者，以進行同步和非同步通訊。</span><span class="sxs-lookup"><span data-stu-id="06da9-127">WMI uses the [**IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) function to pass the necessary pointers and events to your physical consumer for both synchronous and asynchronous communications.</span></span> <span data-ttu-id="06da9-128">您的 **IndicateToConsumer** 執行應該包含所有必要的程式碼來回應事件。</span><span class="sxs-lookup"><span data-stu-id="06da9-128">Your implementation of **IndicateToConsumer** should contain all of the necessary code to respond to an event.</span></span>

    <span data-ttu-id="06da9-129">與暫時性事件取用者不同的是，您不需要呼叫 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) 介面來聯繫 WMI。</span><span class="sxs-lookup"><span data-stu-id="06da9-129">Unlike a temporary event consumer, you do not need to call the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface to contact WMI.</span></span> <span data-ttu-id="06da9-130">相反地，WMI 會透過事件取用者提供者來尋找您的取用者指標。</span><span class="sxs-lookup"><span data-stu-id="06da9-130">Instead, WMI locates a pointer to your consumer through the event consumer provider.</span></span> <span data-ttu-id="06da9-131">如需詳細資訊，請參閱 [撰寫事件取用者提供者](writing-an-event-consumer-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="06da9-131">For more information, see [Writing an Event Consumer Provider](writing-an-event-consumer-provider.md).</span></span>

    <span data-ttu-id="06da9-132">但是，如果您想要回呼 WMI，請使用 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) 和 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面。</span><span class="sxs-lookup"><span data-stu-id="06da9-132">However, if you wish to call back into WMI, use the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) and [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interfaces.</span></span> <span data-ttu-id="06da9-133">連接到 WMI 的傳統方法是在 COM 物件的初始化程式期間。</span><span class="sxs-lookup"><span data-stu-id="06da9-133">The traditional method for connecting to WMI is during the initialization process of your COM object.</span></span> <span data-ttu-id="06da9-134">如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="06da9-134">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

    <span data-ttu-id="06da9-135">如果您將實體取用者實作為同進程 COM 伺服器，並與初始化程式分開連接至 WMI，則必須使用 **CLSID \_ WbemAdministrativeLocator** 類別識別碼來存取 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫中的 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)介面。</span><span class="sxs-lookup"><span data-stu-id="06da9-135">If you implement your physical consumer as an in-process COM server and connect to WMI separately from the initialization process, you must use the **CLSID\_WbemAdministrativeLocator** class identifier to access the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface in the call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="06da9-136">下列範例顯示如何使用 **CLSID \_ WbemAdministrativeLocator** 類別識別碼來存取 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) 介面。</span><span class="sxs-lookup"><span data-stu-id="06da9-136">The following example shows how to use the **CLSID\_WbemAdministrativeLocator** class identifier to access the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface.</span></span>

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    <span data-ttu-id="06da9-137">[**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)介面會取得特定主機電腦上 WMI 的初始命名空間指標。</span><span class="sxs-lookup"><span data-stu-id="06da9-137">The [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface obtains the initial namespace pointer to WMI on a particular host computer.</span></span> <span data-ttu-id="06da9-138">無法在 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫中使用 **CLSID \_ WbemAdministrativeLocator** 識別碼會導致「拒絕存取」錯誤。</span><span class="sxs-lookup"><span data-stu-id="06da9-138">Failure to use the **CLSID\_WbemAdministrativeLocator** identifier in the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call results in an "access denied" error.</span></span>

    <span data-ttu-id="06da9-139">在一般情況下，WMI 會將非同步事件一次傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="06da9-139">Under usual circumstances, WMI delivers asynchronous events to the client one at a time.</span></span> <span data-ttu-id="06da9-140">但是，如果用戶端無法在事件抵達時儘快收到非同步事件通知，WMI 就會開始自動將事件批次處理成單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="06da9-140">However, if a client cannot receive asynchronous event notifications as fast as the events arrive, WMI starts to automatically batch events into a single call.</span></span> <span data-ttu-id="06da9-141">如果反復存取時間是問題的，則自動批次處理會有所説明，這在高輸送量案例中通常是如此。</span><span class="sxs-lookup"><span data-stu-id="06da9-141">Automatic batching helps if the round-trip times are a problem, as is often the case in high-throughput scenarios.</span></span> <span data-ttu-id="06da9-142">但是，如果用戶端或網路頻寬是錯誤的，批次處理就不會改善系統效能。</span><span class="sxs-lookup"><span data-stu-id="06da9-142">However, batching does not improve system performance if the client or the network bandwidth are at fault.</span></span>

 

 
