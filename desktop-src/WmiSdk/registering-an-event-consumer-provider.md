---
description: 若要建立 WMI 事件取用者提供者，您必須 \_ \_ 使用 EventConsumerProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: 註冊事件取用者提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1922970838b99e2a4a371ed7b00ae0f506a0381f0018509bfd6874074e0dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992539"
---
# <a name="registering-an-event-consumer-provider"></a>註冊事件取用者提供者

若要建立 WMI [*事件取用者提供*](gloss-e.md)者，您必須使用 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。 如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。 下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。

下列程式說明如何註冊事件取用者提供者。

**註冊事件取用者提供者**

1.  建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。
2.  建立 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)類別的實例，以描述提供者的功能集。

    [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)所定義的屬性包含提供者的物件路徑，以及事件取用者提供者所支援之邏輯取用者類別的名稱。

    請務必使用 **動態** 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。 **動態** 限定詞表示 WMI 應該使用提供者來取出類別實例。 **提供者** 辨識符號會指定 WMI 應使用的提供者名稱。

下列程式碼範例顯示如何註冊事件取用者提供者。

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



