---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: 'E (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998536"
---
# <a name="e-wmi"></a><span data-ttu-id="3bfa3-103">E (WMI) </span><span class="sxs-lookup"><span data-stu-id="3bfa3-103">E (WMI)</span></span>

<span data-ttu-id="3bfa3-104">[B](gloss-a.md) [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="3bfa3-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="3bfa3-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**事件類別**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-106">事件取用 *者* 可以透過 *事件查詢* 訂閱的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="3bfa3-107">類別會報告特定類型的發生。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="3bfa3-108">例如， [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) 類別會報告特定進程已停止。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**事件取用者**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-110">報告事件發生之通知的接收者。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="3bfa3-111">事件取用者是 [*暫時性*](gloss-t.md) 或 [*永久性*](gloss-p.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**事件取用者提供者**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-113">決定哪一個永久的事件消費者會處理給定之事件的提供者。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="3bfa3-114">[**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)實例會向 WMI 註冊事件取用者提供者，其中包含事件取用者提供者所支援的 [*邏輯取用者*](gloss-l.md)類別清單。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="3bfa3-115">事件取用者提供者是將 [*實體取用者*](gloss-p.md) 對應至 *邏輯取用者* 的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="3bfa3-116">事件取用者提供者支援 [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) 介面，且為永久取用者架構的元件。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**事件篩選器**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-118">[**\_ \_ >eventfilter**](--eventfilter.md)系統類別的實例，描述事件種類和傳遞通知的條件。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="3bfa3-119">取用者會使用事件篩選器來註冊，以接收特定事件種類的通知。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**事件提供者**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-121">WMI 提供者，可監視事件的來源，並在事件發生時通知 WMI。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="3bfa3-122">事件提供者會執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 介面，有時也會 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**事件查詢**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-124">事件取用者用來註冊的 [*WMI 查詢語言*](gloss-w.md) 語句，以接收特定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="3bfa3-125">事件提供者使用事件查詢來登錄要產生特定事件的告知。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**延伸模組架構**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-127">[*Cim 架構*](gloss-c.md)的第三層，包含 cim 架構的平臺專屬延伸模組，例如 WINDOWS、UNIX 和 Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="3bfa3-128">另請參閱 [*常見的模型*](gloss-c.md) 和核心模型。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="3bfa3-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**外來事件**</span><span class="sxs-lookup"><span data-stu-id="3bfa3-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="3bfa3-130">來自提供者的事件通知。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-130">An event notification from a provider.</span></span> <span data-ttu-id="3bfa3-131">大部分的提供者會建立提供者 MOF 檔案中定義之事件類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="3bfa3-132">外來事件繼承自 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="3bfa3-133">例如， [事件記錄檔提供者](/previous-versions/windows/desktop/eventlogprov/event-log-provider) 會定義事件類別 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="3bfa3-134">另請參閱 [*內部事件*](gloss-i.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfa3-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
