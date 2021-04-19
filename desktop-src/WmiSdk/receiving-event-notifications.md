---
description: 暫存事件取用者、永久事件取用者和事件提供者都會使用事件查詢。 事件取用者會使用事件查詢來指定感興趣的事件，而事件提供者會使用查詢來指定它們所提供的事件。
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: 接收事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980769"
---
# <a name="receiving-event-notifications"></a><span data-ttu-id="b32f4-104">接收事件通知</span><span class="sxs-lookup"><span data-stu-id="b32f4-104">Receiving Event Notifications</span></span>

<span data-ttu-id="b32f4-105">暫存事件取用者、永久事件取用者和事件提供者都會使用事件查詢。</span><span class="sxs-lookup"><span data-stu-id="b32f4-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="b32f4-106">事件取用者會使用事件查詢來指定感興趣的事件，而事件提供者會使用查詢來指定它們所提供的事件。</span><span class="sxs-lookup"><span data-stu-id="b32f4-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="b32f4-107">[暫時取用者](receiving-events-for-the-duration-of-your-application.md) 會將查詢放入 [**Iwbemservices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 或 [**iwbemservices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) 方法的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="b32f4-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="b32f4-108">[永久事件取用者](receiving-events-at-all-times.md)會在 [**\_ \_ >eventfilter**](--eventfilter.md)系統類別實例的 **Query** 屬性中放置查詢。</span><span class="sxs-lookup"><span data-stu-id="b32f4-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="b32f4-109">[事件提供者](writing-an-event-provider.md) 會使用事件查詢來註冊，以支援一或多個事件種類。</span><span class="sxs-lookup"><span data-stu-id="b32f4-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="b32f4-110">它們會將查詢放在 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)系統類別實例的 **EventQueryList** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b32f4-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="b32f4-111">所有事件提供者都會建立 **\_ \_ EventProviderRegistration** 實例，以向 Windows Management Instrumentation (WMI) 註冊。</span><span class="sxs-lookup"><span data-stu-id="b32f4-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="b32f4-112">如需詳細資訊，請參閱 [註冊事件提供者](registering-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b32f4-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="b32f4-113">事件取用者和提供者會針對事件查詢使用 [SELECT 語句](select-statement-for-event-queries.md) 和相關的 WHERE 子句，以及 WMI 查詢語言 (WQL) 特有的各種擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b32f4-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="b32f4-114">這些延伸模組是用來保護取用者免于發生太頻繁的通知，而使其變得很有用。</span><span class="sxs-lookup"><span data-stu-id="b32f4-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="b32f4-115">每次發生事件時不需要通知的取用者可以在其查詢中指定下列子句：</span><span class="sxs-lookup"><span data-stu-id="b32f4-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="b32f4-116">[在子句內](within-clause.md)</span><span class="sxs-lookup"><span data-stu-id="b32f4-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="b32f4-117">[Group](group-clause.md) 子句</span><span class="sxs-lookup"><span data-stu-id="b32f4-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="b32f4-118">[HAVING](having-clause.md) 子句</span><span class="sxs-lookup"><span data-stu-id="b32f4-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="b32f4-119">In 和 HAVING 子句會影響事件的時間，而 GROUP 子句會導致傳送具代表性的事件來取代經常發生的事件。</span><span class="sxs-lookup"><span data-stu-id="b32f4-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



