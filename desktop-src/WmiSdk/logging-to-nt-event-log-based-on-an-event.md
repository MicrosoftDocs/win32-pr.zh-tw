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
ms.openlocfilehash: c8c070b1a52fe41f32b8610ff0931d33be7feb33f9f5cd6f6067652e963f6824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050706"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>根據事件記錄至 NT 事件記錄檔

[**NTEventLogEventConsumer**](nteventlogeventconsumer.md)類別會在指定的事件發生時，將訊息寫入 Windows 事件記錄檔。 此類別是 WMI 提供的標準事件取用者。

> [!Note]  
> 依預設，已驗證的使用者不能將事件記錄到遠端電腦上的應用程式記錄檔。 因此，如果您使用 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)類別的 **UNCServerName** 屬性，並將遠端電腦指定為其值，則本主題中所述的範例將會失敗。 若要瞭解如何變更事件記錄檔安全性，請參閱這 [篇知識庫文章](https://support.microsoft.com/kb/323076)。

 

使用標準取用者的基本程式說明如何使用標準取用者 [來監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。 以下是使用 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) 類別時所需的基本程式以外的其他步驟。 這些步驟說明如何建立寫入應用程式事件記錄檔的事件取用者。

下列程式描述如何建立寫入至 NT 事件記錄檔的事件取用者。

**若要建立寫入 Windows 事件記錄檔的事件取用者**

1.  在受控物件格式 (MOF) 檔中，建立 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) 的實例，以接收您在查詢中要求的事件。 如需撰寫 MOF 程式碼的詳細資訊，請參閱 [設計受控物件格式 (mof) 類別](designing-managed-object-format--mof--classes.md)。
2.  建立並命名 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，然後建立查詢來指定觸發寫入至 NT 事件記錄檔的事件種類。

    如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

3.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)的實例產生關聯。
4.  使用 [**Mofcomp.exe**](mofcomp.md)編譯 MOF 檔案。

## <a name="example"></a>範例

本節中的範例是在 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。 此範例示範如何使用 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)來建立取用者，以寫入至應用程式事件記錄檔。 MOF 會建立名為 "NTLogCons Example" 的新類別 \_ ，這是用來查詢作業的事件篩選器，例如建立、在這個新類別的實例上，以及篩選和取用者之間的系結。 因為 MOF 中的最後一個動作是建立 NTLogCons 範例的實例 \_ ，所以您可以在應用程式事件記錄檔中，藉由執行 Eventvwr.exe 來立即查看該事件。

會 `EventID=0x0A for SourceName="WinMgmt"` 識別具有下列文字的訊息。 "%1"、"%2"、"%3" 是 InsertionStringTemplates 陣列中所指定對應字串的預留位置。

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

下列程式說明如何使用範例。

**使用範例**

1.  將下列 MOF 清單複製到文字檔中，並以 MOF 副檔名儲存檔案。
2.  在命令視窗中，使用下列命令編譯 MOF 檔案：

    **Mofcomp.exe** *filename * * *. mof**

3.  執行 Eventvwr.exe。 查看應用程式事件記錄檔。 您應該會看到 ID = 10 (**EventID**) 、Source = "WMI" 和 Type = Error 的事件。
4.  在 [**事件**] 資料行中，按兩下 WMI 中的 **資訊類型** 訊息，並輸入10。 將會顯示事件的下列描述。

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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



