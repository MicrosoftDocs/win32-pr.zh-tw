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
ms.openlocfilehash: b0b7e7b1d1e79e64fb1eb83f17f3aa2d118a9eb53b23c19cbdfd624e2c501a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992778"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>使用標準取用者監視及回應事件

您可以使用已安裝的 [標準取用者類別](standard-consumer-classes.md) ，根據作業系統中的事件來執行動作。 標準取用者是已註冊的簡單類別，而且會定義永久的取用者類別。 每個標準取用者會在收到事件通知之後，採取特定的動作。 例如，您可以定義 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 的實例，以在電腦上的可用磁碟空間與指定的大小不同時執行腳本。

WMI 會將標準取用者編譯為與作業系統相依的預設命名空間，例如：

-   在 Windows Server 2003 中，所有標準取用者預設都會編譯為「根訂用帳戶」 \\ 命名空間。

> [!Note]  
> 如需每個 WMI 類別特有的預設命名空間和作業系統，請參閱每個類別主題的備註和需求一節。

 

下表列出並描述 WMI 標準取用者。



| 標準取用者                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | 在接收到事件通知時執行腳本。 如需詳細資訊，請參閱 [根據事件執行腳本](running-a-script-based-on-an-event.md)。                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | 在接收到事件通知時，將自訂字串寫入至文字記錄檔。 如需詳細資訊，請參閱 [根據事件寫入記錄](writing-to-a-log-file-based-on-an-event.md)檔。                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | 將特定訊息記錄到應用程式事件記錄檔。 如需詳細資訊，請參閱 [根據事件記錄至 NT 事件記錄](logging-to-nt-event-log-based-on-an-event.md)檔。                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | 每次傳遞事件給它時，使用 SMTP 傳送電子郵件訊息。 如需詳細資訊，請參閱 [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)。                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | 當事件傳遞至本機系統時啟動處理常式。 可執行檔必須位於安全的位置，或使用強式存取控制清單 (ACL) 保護，以防止未經授權的使用者以不同的可執行檔取代您的可執行檔。 如需詳細資訊，請參閱 [根據事件從命令列執行程式](running-a-program-from-the-command-line-based-on-an-event.md)。 |



 

下列程式描述如何使用標準取用者來監視和回應事件。 請注意，受控物件格式 (MOF) 檔、腳本或應用程式的程式都相同。

**使用標準取用者監視及回應事件**

1.  使用 MOF 預處理器命令[ \# pragma 命名空間](pragma-namespace.md)來指定 mof 檔案中的命名空間。 在腳本或應用程式中，指定程式碼中連接至 WMI 的命名空間。

    下列 MOF 程式碼範例顯示如何指定根訂用帳戶 \\ 命名空間。

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    大部分的內建 [*事件*](gloss-i.md) 會與根 cimv2 命名空間中類別實例的變更相關聯 \\ 。 不過， [](/previous-versions/windows/desktop/regprov/registrykeychangeevent) \\ [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)會在根預設命名空間中引發登錄事件（例如 RegistryKeyChangeEvent）。

    取用者可以包含位於其他命名空間中的事件類別，方法是在 [**\_ \_ >eventfilter**](--eventfilter.md)查詢事件的 **EventNamespace** 屬性中指定命名空間。 內建 [*事件*](gloss-i.md)類別（例如 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) ）可在每個命名空間中使用。

2.  建立並填入標準取用者類別的實例。

    此實例在 **Name** 屬性中可能會有唯一的值。 您可以重複使用相同的名稱來更新現有的取用者。

    **InsertionStringTemplates** 包含要插入 **您在 [** 事件種類] 中指定之事件的文字。 您可以使用常值字串，或直接參考屬性。 如需詳細資訊，請參閱 [使用標準字串範本](using-standard-string-templates.md) 和 [SELECT 語句進行事件查詢](select-statement-for-event-queries.md)。

    使用事件記錄檔的現有來源，以支援不含相關文字的插入字串。

    下列 MOF 程式碼範例示範如何使用現有的 WSH 來源和 **EventID** 值8。

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

3.  建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並定義事件的查詢。

    在下列範例中，篩選器會監視登錄機碼，以註冊啟動程式。 監視此登錄機碼可能很重要，因為未經授權的程式可以在機碼下註冊本身，這樣會在電腦開機時啟動。

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

4.  識別要監視的事件，並建立事件查詢。

    您可以查看是否有使用的內建或外來事件。 例如，使用登錄提供者的 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) 類別來監視系統登錄的變更。

    如果類別不存在描述您需要監視的事件，您必須建立自己的事件提供者，並定義新的外來事件類別。 如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。

    在 MOF 檔案中，您可以定義篩選準則和取用者的 [*別名*](gloss-a.md) ，以提供簡單的方式來描述實例路徑。

    下列範例顯示如何定義篩選準則和取用者的 [*別名*](gloss-a.md) 。

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以建立篩選和取用者類別的關聯。 此實例會決定當符合指定篩選準則的事件發生時，取用者所指定的動作必須發生。 [**\_ \_ >Eventfilter**](--eventfilter.md)、 [**\_ \_ EventConsumer**](--eventconsumer.md)和 **\_ \_ FilterToConsumerBinding** 在 **CreatorSID** 屬性中必須有相同的個別安全識別碼 (SID) 。 如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。

    下列範例示範如何透過物件路徑來識別實例，或使用別名做為物件路徑的速記運算式。

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    下列範例會使用別名將篩選準則系結至取用者。

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    您可以將一個篩選器系結至多個取用者，這表示當相符事件發生時，必須採取幾個動作;或者，您可以將一個取用者系結至數個篩選準則，這表示當符合其中一個篩選準則的事件發生時，必須採取動作。

    系統會根據取用者和事件的條件來採取下列動作：

    -   如果其中一個永久取用者失敗，則要求事件的其他取用者會收到通知。
    -   如果事件遭到捨棄，WMI 就會引發 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。
    -   如果您訂閱此事件，它會傳回已卸載的事件，而且 [**\_ \_ EventConsumer**](--eventconsumer.md)的參考代表失敗的取用者。
    -   如果取用者失敗，WMI 會引發 [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md)，其中可能包含 **ErrorCode**、 **ErrorDescription** 和 **ErrorObject** 屬性中的詳細資訊。

    如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。

## <a name="example"></a>範例

下列範例顯示 [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)實例的 MOF。 在編譯此 MOF 之後，任何嘗試在登錄路徑中建立、刪除或修改值的 **HKEY \_ 本機 \_ 電腦軟體， \\ \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** 會在應用程式 eventlog 的來源「WSH」下記錄專案。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[安全地接收事件](receiving-events-securely.md)
</dt> </dl>

 

 
