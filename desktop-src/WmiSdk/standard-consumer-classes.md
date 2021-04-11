---
description: 下表列出 WMI 預先安裝的永久取用者類別。
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: 標準取用者類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195231"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="73cd2-103">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="73cd2-103">Standard Consumer Classes</span></span>

<span data-ttu-id="73cd2-104">下表列出 WMI 預先安裝的永久取用者類別。</span><span class="sxs-lookup"><span data-stu-id="73cd2-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="73cd2-105">您可以建立這些類別的實例，以提供永久取用者類別，以提供在篩選中指定的事件所觸發時所回應的邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="73cd2-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="73cd2-106">例如，使用 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別來定義在指定的事件發生時所執行的腳本。</span><span class="sxs-lookup"><span data-stu-id="73cd2-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="73cd2-107">如需詳細資訊，請參閱使用標準取用者和[監視事件](monitoring-events.md)[來監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="73cd2-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="73cd2-108">類別</span><span class="sxs-lookup"><span data-stu-id="73cd2-108">Class</span></span>                                                                        | <span data-ttu-id="73cd2-109">描述</span><span class="sxs-lookup"><span data-stu-id="73cd2-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73cd2-110">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="73cd2-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="73cd2-111">當事件傳遞給它時，以任意指令碼語言執行預先定義的腳本。</span><span class="sxs-lookup"><span data-stu-id="73cd2-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="73cd2-112">範例： [根據事件執行腳本](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="73cd2-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="73cd2-113">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="73cd2-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="73cd2-114">當事件傳遞給它時，會在本機系統內容中啟動任意進程。</span><span class="sxs-lookup"><span data-stu-id="73cd2-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="73cd2-115">範例： [根據事件從命令列執行程式](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="73cd2-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="73cd2-116">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="73cd2-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="73cd2-117">將事件傳遞給文字記錄檔時，將自訂字串寫入至文字記錄檔。</span><span class="sxs-lookup"><span data-stu-id="73cd2-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="73cd2-118">範例：[根據事件寫入記錄](writing-to-a-log-file-based-on-an-event.md)檔</span><span class="sxs-lookup"><span data-stu-id="73cd2-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="73cd2-119">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="73cd2-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="73cd2-120">將事件傳遞給 Windows 事件記錄檔時，會將特定訊息記錄到該記錄檔。</span><span class="sxs-lookup"><span data-stu-id="73cd2-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="73cd2-121">範例：[根據事件記錄至 NT 事件記錄](logging-to-nt-event-log-based-on-an-event.md)檔</span><span class="sxs-lookup"><span data-stu-id="73cd2-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="73cd2-122">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="73cd2-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="73cd2-123">提供 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別的所有實例通用的註冊資料。</span><span class="sxs-lookup"><span data-stu-id="73cd2-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="73cd2-124">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="73cd2-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="73cd2-125">每次傳遞事件給它時，使用 SMTP 傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="73cd2-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="73cd2-126">範例： [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="73cd2-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="73cd2-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="73cd2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73cd2-128">監視事件</span><span class="sxs-lookup"><span data-stu-id="73cd2-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="73cd2-129">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="73cd2-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="73cd2-130">根據事件執行腳本</span><span class="sxs-lookup"><span data-stu-id="73cd2-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="73cd2-131">根據事件傳送電子郵件</span><span class="sxs-lookup"><span data-stu-id="73cd2-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




