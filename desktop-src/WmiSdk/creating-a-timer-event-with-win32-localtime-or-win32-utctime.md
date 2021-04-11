---
description: 您可以搭配使用內建事件和事件篩選器的標準模型與 Win32 \_ LocalTime 或 win32 \_ UTCTime 類別，以接收計時通知。
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: 使用 Win32_LocalTime 或 Win32_UTCTime 建立計時器事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194707"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a><span data-ttu-id="2e19a-103">使用 Win32 \_ LocalTime 或 win32 UTCTime 建立計時器事件 \_</span><span class="sxs-lookup"><span data-stu-id="2e19a-103">Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime</span></span>

<span data-ttu-id="2e19a-104">您可以搭配使用內建事件和事件篩選器的標準模型與 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 或 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 類別，以接收計時通知。</span><span class="sxs-lookup"><span data-stu-id="2e19a-104">You can use the standard model of intrinsic events and event filters in combination with the [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes to receive a timed notification.</span></span> <span data-ttu-id="2e19a-105">內部方法是產生計時事件的建議方式，因為它與 Microsoft 事件模型的其餘部分一致，並支援複雜的排程條件。</span><span class="sxs-lookup"><span data-stu-id="2e19a-105">The intrinsic method is a recommended way of generating timed events, as it is consistent with the rest of the Microsoft event model and supports complex scheduling conditions.</span></span>

<span data-ttu-id="2e19a-106">[**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)和 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)類別是根 \\ cimv2 命名空間中代表系統時鐘的單一類別。</span><span class="sxs-lookup"><span data-stu-id="2e19a-106">The [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) and [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes are singleton classes in the root\\cimv2 namespace that represent the system clock.</span></span> <span data-ttu-id="2e19a-107">在查詢時， **Win32 \_ LocalTime** 會以具有本機參考的24小時制傳回目前的資料抓取時間。</span><span class="sxs-lookup"><span data-stu-id="2e19a-107">When queried, **Win32\_LocalTime** returns the current time at the moment of data retrieval in a 24-hour clock with local reference.</span></span> <span data-ttu-id="2e19a-108">**Win32 \_ UTCTime** 類別會傳回目前的時間與 UTC 參考。</span><span class="sxs-lookup"><span data-stu-id="2e19a-108">The **Win32\_UTCTime** class returns the current time with UTC reference.</span></span>

<span data-ttu-id="2e19a-109">**使用 Win32 \_ LocalTime 或 win32 UTCTime 產生計時或重複事件 \_**</span><span class="sxs-lookup"><span data-stu-id="2e19a-109">**To generate timed or repeating events with Win32\_LocalTime or Win32\_UTCTime**</span></span>

-   <span data-ttu-id="2e19a-110">設定 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 或 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 的內建通知事件篩選準則，以要求特定日期和時間的通知。</span><span class="sxs-lookup"><span data-stu-id="2e19a-110">Set up an intrinsic notification event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) that requests notification for a specific date and time.</span></span>

<span data-ttu-id="2e19a-111">例如，如果日光節約時間下的當地時間是 4 P.M。</span><span class="sxs-lookup"><span data-stu-id="2e19a-111">For example, if the local time under Daylight Savings Time is 4 P.M.</span></span> <span data-ttu-id="2e19a-112">而位置是 GMT-8，則 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 會傳回16和 [**win32 \_ UTCTime。 hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 會傳回23。</span><span class="sxs-lookup"><span data-stu-id="2e19a-112">and the location is GMT -8, then [**Win32\_LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) returns 16 and [**Win32\_UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) returns 23.</span></span>

<span data-ttu-id="2e19a-113">下列程式碼範例說明如何建立事件篩選器，以在每日午夜發出重複的事件信號。</span><span class="sxs-lookup"><span data-stu-id="2e19a-113">The following code example describes how to create an event filter that signals a repeating event every day at midnight.</span></span>

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
