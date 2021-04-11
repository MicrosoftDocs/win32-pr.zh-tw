---
description: WMI 包含一組類別，可針對使用 WMI 提供者的用戶端應用程式進行疑難排解。
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: 疑難排解 WMI 用戶端應用程式
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193860"
---
# <a name="troubleshooting-wmi-client-applications"></a>疑難排解 WMI 用戶端應用程式

WMI 包含一組類別，可針對使用 WMI 提供者的用戶端應用程式 [進行疑難排解](wmi-troubleshooting-classes.md) 。 疑難排解事件類別結合了 WMI 事件類別，讓您可以使用已捕捉的疑難排解事件記錄檔來追蹤應用程式的執行。

下列清單包含疑難排解事件類別的範例：

-   [**Msft \_ 的 wmiprovider \_ ExecMethodAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    在 WMI 對提供者呼叫 [**IWbemServices：： ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 之前引發。

-   [**Msft \_ 的 wmiprovider \_ ExecMethodAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    在 WMI 呼叫提供者上的 [**IWbemServices：： ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 之後引發。

下列程式顯示如何針對應用程式執行進行疑難排解。

**設定 WMI 疑難排解**

1.  建立並編譯 MOF 檔案，以使用 WMI 記錄事件取用者。
2.  執行您的用戶端應用程式。
3.  查看所有提供者作業和失敗事件的疑難排解記錄檔，並分析記錄以診斷您遇到的用戶端問題。

另一個疑難排解方法是在 **根 \\ cimv2** 命名空間中列舉 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)，以查看目前在電腦快取中的提供者清單。 此類別中有一些方法，可讓您載入和卸載提供者以進行偵錯工具或安裝。

下列程式碼範例會使用 WMI 記錄事件取用者來捕捉父事件類別的所有事件，進而捕捉所有提供者作業事件。

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

當錯誤訊息表示提供者載入失敗時，請使用 [**MSFT \_ 的 wmiprovider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) 來識別造成錯誤的提供者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[WMI 疑難排解類別](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
