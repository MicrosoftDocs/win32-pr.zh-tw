---
description: 藉由使用 SMTPEventConsumer 類別，您可以在發生指定事件時，將電子郵件傳送給指定的使用者。 此類別是 WMI 提供的標準事件取用者。
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: 根據事件傳送電子郵件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980896"
---
# <a name="sending-email-based-on-an-event"></a>根據事件傳送電子郵件

藉由使用 [SMTPEventConsumer](smtpeventconsumer.md) 類別，您可以在發生指定事件時，將電子郵件傳送給指定的使用者。 此類別是 WMI 提供的 [標準事件取用者](standard-consumer-classes.md) 。

[SMTPEventConsumer](smtpeventconsumer.md)類別需要下列條件，才能傳送電子郵件訊息以回應事件：

-   [SMTPEventConsumer](smtpeventconsumer.md)類別必須編譯成正確的命名空間。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。
-   SMTP 伺服器必須存在於網路上。
-   電子郵件訊息不能有附件。
-   電子郵件訊息必須以 US-ASCII 編碼。

使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。 下列程式會新增至基本程式;是 [SMTPEventConsumer](smtpeventconsumer.md) 類別特有的;並描述如何建立傳送電子郵件的事件取用者。

下列程式描述如何建立傳送電子郵件的事件取用者。

**建立傳送電子郵件的事件取用者**

1.  如有必要，請安裝並註冊 [SMTPEventConsumer](smtpeventconsumer.md) 類別。

    WMI 安裝程式會將 [SMTPEventConsumer](smtpeventconsumer.md) 類別編譯為根 \\ 訂用帳戶命名空間。

2.  找出您想要監視的事件，並建立事件查詢。

    可能會有用來監視事件的現有內部事件。 大部分內建事件都與 "root \\ cimv2" 命名空間中的類別實例變更相關聯。 藉由分析 [WMI 類別](wmi-classes.md) 參考中的類別，您可能會找到可識別您要監視之事件的類別。 例如，使用 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別來監視硬碟的變更。

    如果沒有任何現有的內部事件使用，可能會有可運作的外來事件提供者。 例如，使用登錄提供者的 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) 類別來監視系統登錄的變更。

    如果找不到識別您要監視之事件的類別，您必須建立自己的事件提供者，並定義新的外建事件類別。 如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。

3.  在受控物件格式 (MOF) 檔中，建立 [SMTPEventConsumer](smtpeventconsumer.md) 的實例以接收事件。

    您可以使用實例的屬性，定義事件發生時要傳送的電子郵件訊息。 例如， **ToLine** 屬性會定義電子郵件地址，而 **Message** 屬性則會定義電子郵件訊息的文字。 您必須定義電子郵件地址、主旨和訊息的文字，但是電子郵件訊息不能有附件。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。

4.  建立指定您要監視之事件的事件查詢。

    如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

5.  建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並將您的查詢儲存在 **查詢** 屬性中。

    如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

6.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以建立篩選和取用者的關聯。
7.  使用 [**Mofcomp.exe**](mofcomp.md)編譯 MOF 檔案。


## <a name="example"></a>範例

本節中的範例是在 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。

下列程式說明如何使用範例。

**使用範例**

1.  將下列 MOF 複製到文字檔，並以 MOF 副檔名儲存檔案。
2.  在 [命令提示字元] 視窗中，使用下列命令編譯 MOF 檔案：

    **Mofcomp.exe** *filename * * *. mof**

> [!Note]  
> 當 MOF 程式碼編譯為根訂用帳戶 \\ 命名空間時， [SMTPEventConsumer](smtpeventconsumer.md) 會編譯成相同的命名空間。

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
