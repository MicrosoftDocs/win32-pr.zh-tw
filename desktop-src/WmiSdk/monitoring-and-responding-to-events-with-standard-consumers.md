---
description: 您可以使用已安裝的標準取用者類別，根據作業系統中的事件來執行動作。
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: 使用標準取用者監視及回應事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103854104"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="633b8-103">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="633b8-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="633b8-104">您可以使用已安裝的 [標準取用者類別](standard-consumer-classes.md) ，根據作業系統中的事件來執行動作。</span><span class="sxs-lookup"><span data-stu-id="633b8-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="633b8-105">標準取用者是已註冊的簡單類別，而且會定義永久的取用者類別。</span><span class="sxs-lookup"><span data-stu-id="633b8-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="633b8-106">每個標準取用者會在收到事件通知之後，採取特定的動作。</span><span class="sxs-lookup"><span data-stu-id="633b8-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="633b8-107">例如，您可以定義 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 的實例，以在電腦上的可用磁碟空間與指定的大小不同時執行腳本。</span><span class="sxs-lookup"><span data-stu-id="633b8-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="633b8-108">WMI 會將標準取用者編譯為與作業系統相依的預設命名空間，例如：</span><span class="sxs-lookup"><span data-stu-id="633b8-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="633b8-109">在 Windows Server 2003 中，所有標準取用者預設都會編譯為「根訂用帳戶」 \\ 命名空間。</span><span class="sxs-lookup"><span data-stu-id="633b8-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="633b8-110">如需每個 WMI 類別特有的預設命名空間和作業系統，請參閱每個類別主題的備註和需求一節。</span><span class="sxs-lookup"><span data-stu-id="633b8-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="633b8-111">下表列出並描述 WMI 標準取用者。</span><span class="sxs-lookup"><span data-stu-id="633b8-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="633b8-112">標準取用者</span><span class="sxs-lookup"><span data-stu-id="633b8-112">Standard consumer</span></span>                                              | <span data-ttu-id="633b8-113">Description</span><span class="sxs-lookup"><span data-stu-id="633b8-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="633b8-114">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="633b8-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="633b8-115">在接收到事件通知時執行腳本。</span><span class="sxs-lookup"><span data-stu-id="633b8-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="633b8-116">如需詳細資訊，請參閱 [根據事件執行腳本](running-a-script-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="633b8-117">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="633b8-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="633b8-118">在接收到事件通知時，將自訂字串寫入至文字記錄檔。</span><span class="sxs-lookup"><span data-stu-id="633b8-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="633b8-119">如需詳細資訊，請參閱 [根據事件寫入記錄](writing-to-a-log-file-based-on-an-event.md)檔。</span><span class="sxs-lookup"><span data-stu-id="633b8-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="633b8-120">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="633b8-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="633b8-121">將特定訊息記錄到應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="633b8-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="633b8-122">如需詳細資訊，請參閱 [根據事件記錄至 NT 事件記錄](logging-to-nt-event-log-based-on-an-event.md)檔。</span><span class="sxs-lookup"><span data-stu-id="633b8-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="633b8-123">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="633b8-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="633b8-124">每次傳遞事件給它時，使用 SMTP 傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="633b8-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="633b8-125">如需詳細資訊，請參閱 [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="633b8-126">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="633b8-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="633b8-127">當事件傳遞至本機系統時啟動處理常式。</span><span class="sxs-lookup"><span data-stu-id="633b8-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="633b8-128">可執行檔必須位於安全的位置，或使用強式存取控制清單 (ACL) 保護，以防止未經授權的使用者以不同的可執行檔取代您的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="633b8-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="633b8-129">如需詳細資訊，請參閱 [根據事件從命令列執行程式](running-a-program-from-the-command-line-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="633b8-130">下列程式描述如何使用標準取用者來監視和回應事件。</span><span class="sxs-lookup"><span data-stu-id="633b8-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="633b8-131">請注意，受控物件格式 (MOF) 檔、腳本或應用程式的程式都相同。</span><span class="sxs-lookup"><span data-stu-id="633b8-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="633b8-132">**使用標準取用者監視及回應事件**</span><span class="sxs-lookup"><span data-stu-id="633b8-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="633b8-133">使用 MOF 預處理器命令[ \# pragma 命名空間](pragma-namespace.md)來指定 mof 檔案中的命名空間。</span><span class="sxs-lookup"><span data-stu-id="633b8-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="633b8-134">在腳本或應用程式中，指定程式碼中連接至 WMI 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="633b8-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="633b8-135">下列 MOF 程式碼範例顯示如何指定根訂用帳戶 \\ 命名空間。</span><span class="sxs-lookup"><span data-stu-id="633b8-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="633b8-136">大部分的內建 [*事件*](gloss-i.md) 會與根 cimv2 命名空間中類別實例的變更相關聯 \\ 。</span><span class="sxs-lookup"><span data-stu-id="633b8-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="633b8-137">不過， [](/previous-versions/windows/desktop/regprov/registrykeychangeevent) \\ [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)會在根預設命名空間中引發登錄事件（例如 RegistryKeyChangeEvent）。</span><span class="sxs-lookup"><span data-stu-id="633b8-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="633b8-138">取用者可以包含位於其他命名空間中的事件類別，方法是在 [**\_ \_ >eventfilter**](--eventfilter.md)查詢事件的 **EventNamespace** 屬性中指定命名空間。</span><span class="sxs-lookup"><span data-stu-id="633b8-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="633b8-139">內建 [*事件*](gloss-i.md)類別（例如 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) ）可在每個命名空間中使用。</span><span class="sxs-lookup"><span data-stu-id="633b8-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="633b8-140">建立並填入標準取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="633b8-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="633b8-141">此實例在 **Name** 屬性中可能會有唯一的值。</span><span class="sxs-lookup"><span data-stu-id="633b8-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="633b8-142">您可以重複使用相同的名稱來更新現有的取用者。</span><span class="sxs-lookup"><span data-stu-id="633b8-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="633b8-143">**InsertionStringTemplates** 包含要插入 **您在 [** 事件種類] 中指定之事件的文字。</span><span class="sxs-lookup"><span data-stu-id="633b8-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="633b8-144">您可以使用常值字串，或直接參考屬性。</span><span class="sxs-lookup"><span data-stu-id="633b8-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="633b8-145">如需詳細資訊，請參閱 [使用標準字串範本](using-standard-string-templates.md) 和 [SELECT 語句進行事件查詢](select-statement-for-event-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="633b8-146">使用事件記錄檔的現有來源，以支援不含相關文字的插入字串。</span><span class="sxs-lookup"><span data-stu-id="633b8-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="633b8-147">下列 MOF 程式碼範例示範如何使用現有的 WSH 來源和 **EventID** 值8。</span><span class="sxs-lookup"><span data-stu-id="633b8-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  <span data-ttu-id="633b8-148">建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並定義事件的查詢。</span><span class="sxs-lookup"><span data-stu-id="633b8-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="633b8-149">在下列範例中，篩選器會監視登錄機碼，以註冊啟動程式。</span><span class="sxs-lookup"><span data-stu-id="633b8-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="633b8-150">監視此登錄機碼可能很重要，因為未經授權的程式可以在機碼下註冊本身，這樣會在電腦開機時啟動。</span><span class="sxs-lookup"><span data-stu-id="633b8-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  <span data-ttu-id="633b8-151">識別要監視的事件，並建立事件查詢。</span><span class="sxs-lookup"><span data-stu-id="633b8-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="633b8-152">您可以查看是否有使用的內建或外來事件。</span><span class="sxs-lookup"><span data-stu-id="633b8-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="633b8-153">例如，使用登錄提供者的 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) 類別來監視系統登錄的變更。</span><span class="sxs-lookup"><span data-stu-id="633b8-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="633b8-154">如果類別不存在描述您需要監視的事件，您必須建立自己的事件提供者，並定義新的外來事件類別。</span><span class="sxs-lookup"><span data-stu-id="633b8-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="633b8-155">如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="633b8-156">在 MOF 檔案中，您可以定義篩選準則和取用者的 [*別名*](gloss-a.md) ，以提供簡單的方式來描述實例路徑。</span><span class="sxs-lookup"><span data-stu-id="633b8-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="633b8-157">下列範例顯示如何定義篩選準則和取用者的 [*別名*](gloss-a.md) 。</span><span class="sxs-lookup"><span data-stu-id="633b8-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="633b8-158">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以建立篩選和取用者類別的關聯。</span><span class="sxs-lookup"><span data-stu-id="633b8-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="633b8-159">此實例會決定當符合指定篩選準則的事件發生時，取用者所指定的動作必須發生。</span><span class="sxs-lookup"><span data-stu-id="633b8-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="633b8-160">[**\_ \_ >eventfilter**](--eventfilter.md)、 [**\_ \_ EventConsumer**](--eventconsumer.md)和 **\_ \_ FilterToConsumerBinding** 在 **CreatorSID** 屬性中必須有相同的個別安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="633b8-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="633b8-161">如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="633b8-162">下列範例示範如何透過物件路徑來識別實例，或使用別名做為物件路徑的速記運算式。</span><span class="sxs-lookup"><span data-stu-id="633b8-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="633b8-163">下列範例會使用別名將篩選準則系結至取用者。</span><span class="sxs-lookup"><span data-stu-id="633b8-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="633b8-164">您可以將一個篩選器系結至多個取用者，這表示當相符事件發生時，必須採取幾個動作;或者，您可以將一個取用者系結至數個篩選準則，這表示當符合其中一個篩選準則的事件發生時，必須採取動作。</span><span class="sxs-lookup"><span data-stu-id="633b8-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="633b8-165">系統會根據取用者和事件的條件來採取下列動作：</span><span class="sxs-lookup"><span data-stu-id="633b8-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="633b8-166">如果其中一個永久取用者失敗，則要求事件的其他取用者會收到通知。</span><span class="sxs-lookup"><span data-stu-id="633b8-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="633b8-167">如果事件遭到捨棄，WMI 就會引發 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="633b8-168">如果您訂閱此事件，它會傳回已卸載的事件，而且 [**\_ \_ EventConsumer**](--eventconsumer.md)的參考代表失敗的取用者。</span><span class="sxs-lookup"><span data-stu-id="633b8-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="633b8-169">如果取用者失敗，WMI 會引發 [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md)，其中可能包含 **ErrorCode**、 **ErrorDescription** 和 **ErrorObject** 屬性中的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="633b8-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="633b8-170">如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="633b8-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="633b8-171">範例</span><span class="sxs-lookup"><span data-stu-id="633b8-171">Example</span></span>

<span data-ttu-id="633b8-172">下列範例顯示 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)實例的 MOF。</span><span class="sxs-lookup"><span data-stu-id="633b8-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="633b8-173">在您編譯此 MOF 之後，任何嘗試在登錄路徑中建立、刪除或修改值的 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** 會在應用程式 eventlog 的來源「WSH」下記錄一個專案。</span><span class="sxs-lookup"><span data-stu-id="633b8-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a><span data-ttu-id="633b8-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="633b8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="633b8-175">安全地接收事件</span><span class="sxs-lookup"><span data-stu-id="633b8-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
