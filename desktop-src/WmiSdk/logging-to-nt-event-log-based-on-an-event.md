---
description: NTEventLogEventConsumer 類別會在指定的事件發生時，將訊息寫入 Windows 事件記錄檔。 此類別是 WMI 提供的標準事件取用者。
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: 根據事件記錄至 NT 事件記錄檔
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850756"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="19128-104">根據事件記錄至 NT 事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="19128-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="19128-105">[**NTEventLogEventConsumer**](nteventlogeventconsumer.md)類別會在指定的事件發生時，將訊息寫入 Windows 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="19128-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="19128-106">此類別是 WMI 提供的標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="19128-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="19128-107">依預設，已驗證的使用者不能將事件記錄到遠端電腦上的應用程式記錄檔。</span><span class="sxs-lookup"><span data-stu-id="19128-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="19128-108">因此，如果您使用 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)類別的 **UNCServerName** 屬性，並將遠端電腦指定為其值，則本主題中所述的範例將會失敗。</span><span class="sxs-lookup"><span data-stu-id="19128-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="19128-109">若要瞭解如何變更事件記錄檔安全性，請參閱這 [篇知識庫文章](https://support.microsoft.com/kb/323076)。</span><span class="sxs-lookup"><span data-stu-id="19128-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="19128-110">使用標準取用者的基本程式說明如何使用標準取用者 [來監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="19128-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="19128-111">以下是使用 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) 類別時所需的基本程式以外的其他步驟。</span><span class="sxs-lookup"><span data-stu-id="19128-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="19128-112">這些步驟說明如何建立寫入應用程式事件記錄檔的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="19128-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="19128-113">下列程式描述如何建立寫入至 NT 事件記錄檔的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="19128-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="19128-114">**若要建立寫入 Windows 事件記錄檔的事件取用者**</span><span class="sxs-lookup"><span data-stu-id="19128-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="19128-115">在受控物件格式 (MOF) 檔中，建立 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) 的實例，以接收您在查詢中要求的事件。</span><span class="sxs-lookup"><span data-stu-id="19128-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="19128-116">如需撰寫 MOF 程式碼的詳細資訊，請參閱 [設計受控物件格式 (mof) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="19128-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="19128-117">建立並命名 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，然後建立查詢來指定觸發寫入至 NT 事件記錄檔的事件種類。</span><span class="sxs-lookup"><span data-stu-id="19128-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="19128-118">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="19128-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="19128-119">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)的實例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="19128-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="19128-120">使用 [**Mofcomp.exe**](mofcomp.md)編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="19128-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="19128-121">範例</span><span class="sxs-lookup"><span data-stu-id="19128-121">Example</span></span>

<span data-ttu-id="19128-122">本節中的範例是在 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。</span><span class="sxs-lookup"><span data-stu-id="19128-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="19128-123">此範例示範如何使用 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)來建立取用者，以寫入至應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="19128-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="19128-124">MOF 會建立名為 "NTLogCons Example" 的新類別 \_ ，這是用來查詢作業的事件篩選器，例如建立、在這個新類別的實例上，以及篩選和取用者之間的系結。</span><span class="sxs-lookup"><span data-stu-id="19128-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="19128-125">因為 MOF 中的最後一個動作是建立 NTLogCons 範例的實例 \_ ，所以您可以在應用程式事件記錄檔中，藉由執行 Eventvwr.exe 來立即查看該事件。</span><span class="sxs-lookup"><span data-stu-id="19128-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="19128-126">會 `EventID=0x0A for SourceName="WinMgmt"` 識別具有下列文字的訊息。</span><span class="sxs-lookup"><span data-stu-id="19128-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="19128-127">"%1"、"%2"、"%3" 是 InsertionStringTemplates 陣列中所指定對應字串的預留位置。</span><span class="sxs-lookup"><span data-stu-id="19128-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="19128-128">下列程式說明如何使用範例。</span><span class="sxs-lookup"><span data-stu-id="19128-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="19128-129">**使用範例**</span><span class="sxs-lookup"><span data-stu-id="19128-129">**To use the example**</span></span>

1.  <span data-ttu-id="19128-130">將下列 MOF 清單複製到文字檔中，並以 MOF 副檔名儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="19128-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="19128-131">在命令視窗中，使用下列命令編譯 MOF 檔案：</span><span class="sxs-lookup"><span data-stu-id="19128-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="19128-132">**Mofcomp.exe** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="19128-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="19128-133">執行 Eventvwr.exe。</span><span class="sxs-lookup"><span data-stu-id="19128-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="19128-134">查看應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="19128-134">Look at the Application event log.</span></span> <span data-ttu-id="19128-135">您應該會看到 ID = 10 (**EventID**) 、Source = "WMI" 和 Type = Error 的事件。</span><span class="sxs-lookup"><span data-stu-id="19128-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="19128-136">在 [**事件**] 資料行中，按兩下 WMI 中的 **資訊類型** 訊息，並輸入10。</span><span class="sxs-lookup"><span data-stu-id="19128-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="19128-137">將會顯示事件的下列描述。</span><span class="sxs-lookup"><span data-stu-id="19128-137">The following description will be displayed for the event.</span></span>

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a><span data-ttu-id="19128-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="19128-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19128-139">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="19128-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



