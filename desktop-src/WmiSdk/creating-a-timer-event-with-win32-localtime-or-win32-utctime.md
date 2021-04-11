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
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a>使用 Win32 \_ LocalTime 或 win32 UTCTime 建立計時器事件 \_

您可以搭配使用內建事件和事件篩選器的標準模型與 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 或 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 類別，以接收計時通知。 內部方法是產生計時事件的建議方式，因為它與 Microsoft 事件模型的其餘部分一致，並支援複雜的排程條件。

[**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)和 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)類別是根 \\ cimv2 命名空間中代表系統時鐘的單一類別。 在查詢時， **Win32 \_ LocalTime** 會以具有本機參考的24小時制傳回目前的資料抓取時間。 **Win32 \_ UTCTime** 類別會傳回目前的時間與 UTC 參考。

**使用 Win32 \_ LocalTime 或 win32 UTCTime 產生計時或重複事件 \_**

-   設定 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 或 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 的內建通知事件篩選準則，以要求特定日期和時間的通知。

例如，如果日光節約時間下的當地時間是 4 P.M。 而位置是 GMT-8，則 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 會傳回16和 [**win32 \_ UTCTime。 hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 會傳回23。

下列程式碼範例說明如何建立事件篩選器，以在每日午夜發出重複的事件信號。

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

 

 
