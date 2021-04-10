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
# <a name="writing-to-a-log-file-based-on-an-event"></a>根據事件寫入記錄檔

當指定的事件發生時， [**LogFileEventConsumer**](logfileeventconsumer.md) 類別可以將預先定義的文字寫入記錄檔。 此類別是 WMI 提供的標準事件取用者。

使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

下列程式會新增至基本程式，專屬於 [**LogFileEventConsumer**](logfileeventconsumer.md) 類別，並說明如何建立可執行程式的事件取用者。

**若要建立寫入記錄檔的事件取用者**

1.  在受控物件格式 (MOF) 檔中，建立 [**LogFileEventConsumer**](logfileeventconsumer.md) 的實例以接收您在查詢中要求的事件、將實例命名為 **name** 屬性，然後將記錄檔的路徑放在 **Filename** 屬性中。

    如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。

2.  提供文字模板，以寫入 Text 屬性中的記錄檔。

    如需詳細資訊，請參閱 [使用標準字串範本](using-standard-string-templates.md)。

3.  建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並定義查詢來指定將啟動取用者的事件。

    如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

4.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**LogFileEventConsumer**](logfileeventconsumer.md)的實例產生關聯。
5.  若要控制讀取或寫入記錄檔的物件，請將記錄檔所在目錄的安全性設定為所需的層級。
6.  使用 [**Mofcomp.exe**](mofcomp.md)編譯您的 MOF 檔案。

## <a name="example"></a>範例

本節中的範例是在 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。 此範例會使用標準 LogFileEventConsumer 來建立名為 LogFileEvent 的取用者類別，以在建立類別 LogFileEvent 的實例時，將行寫入至 file c： \\ Logfile。

下列程式說明如何使用範例。

**使用範例**

1.  將下列 MOF 清單複製到文字檔中，並以 MOF 副檔名儲存檔案。
2.  在命令視窗中，使用下列命令編譯 MOF 檔案。

    **Mofcomp.exe** *filename * * *. mof**

3.  開啟 Logfile 以查看 LogFileEvent.Name 所指定的行：「記錄檔事件取用者事件」。

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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



