---
description: 當指定的事件發生時，LogFileEventConsumer 類別可以將預先定義的文字寫入記錄檔。 此類別是 WMI 提供的標準事件取用者。
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: 根據事件寫入記錄檔
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192181"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="86f23-104">根據事件寫入記錄檔</span><span class="sxs-lookup"><span data-stu-id="86f23-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="86f23-105">當指定的事件發生時， [**LogFileEventConsumer**](logfileeventconsumer.md) 類別可以將預先定義的文字寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="86f23-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="86f23-106">此類別是 WMI 提供的標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="86f23-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="86f23-107">使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="86f23-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="86f23-108">下列程式會新增至基本程式，專屬於 [**LogFileEventConsumer**](logfileeventconsumer.md) 類別，並說明如何建立可執行程式的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="86f23-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="86f23-109">**若要建立寫入記錄檔的事件取用者**</span><span class="sxs-lookup"><span data-stu-id="86f23-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="86f23-110">在受控物件格式 (MOF) 檔中，建立 [**LogFileEventConsumer**](logfileeventconsumer.md) 的實例以接收您在查詢中要求的事件、將實例命名為 **name** 屬性，然後將記錄檔的路徑放在 **Filename** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="86f23-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="86f23-111">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="86f23-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="86f23-112">提供文字模板，以寫入 Text 屬性中的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="86f23-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="86f23-113">如需詳細資訊，請參閱 [使用標準字串範本](using-standard-string-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="86f23-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="86f23-114">建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並定義查詢來指定將啟動取用者的事件。</span><span class="sxs-lookup"><span data-stu-id="86f23-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="86f23-115">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="86f23-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="86f23-116">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**LogFileEventConsumer**](logfileeventconsumer.md)的實例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="86f23-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="86f23-117">若要控制讀取或寫入記錄檔的物件，請將記錄檔所在目錄的安全性設定為所需的層級。</span><span class="sxs-lookup"><span data-stu-id="86f23-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="86f23-118">使用 [**Mofcomp.exe**](mofcomp.md)編譯您的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="86f23-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="86f23-119">範例</span><span class="sxs-lookup"><span data-stu-id="86f23-119">Example</span></span>

<span data-ttu-id="86f23-120">本節中的範例是在 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。</span><span class="sxs-lookup"><span data-stu-id="86f23-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="86f23-121">此範例會使用標準 LogFileEventConsumer 來建立名為 LogFileEvent 的取用者類別，以在建立類別 LogFileEvent 的實例時，將行寫入至 file c： \\ Logfile。</span><span class="sxs-lookup"><span data-stu-id="86f23-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="86f23-122">下列程式說明如何使用範例。</span><span class="sxs-lookup"><span data-stu-id="86f23-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="86f23-123">**使用範例**</span><span class="sxs-lookup"><span data-stu-id="86f23-123">**To use the example**</span></span>

1.  <span data-ttu-id="86f23-124">將下列 MOF 清單複製到文字檔中，並以 MOF 副檔名儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="86f23-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="86f23-125">在命令視窗中，使用下列命令編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="86f23-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="86f23-126">**Mofcomp.exe** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="86f23-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="86f23-127">開啟 Logfile 以查看 LogFileEvent.Name 所指定的行：「記錄檔事件取用者事件」。</span><span class="sxs-lookup"><span data-stu-id="86f23-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a><span data-ttu-id="86f23-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="86f23-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f23-129">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="86f23-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



