---
description: 若要建立 WMI 事件提供者，您必須 \_ \_ 使用 EventProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: 註冊事件提供者
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115801"
---
# <a name="registering-an-event-provider"></a>註冊事件提供者

若要建立 WMI [*事件提供者*](gloss-e.md)，您必須使用 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。 如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。 下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。

下列程式說明如何註冊事件提供者。

**註冊事件提供者**

1.  建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。
2.  建立 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別的實例，以描述提供者的功能集。

    [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別會繼承 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)父類別的許多屬性。 **\_ \_ EventProviderRegistration** 類別的本機屬性是提供者的物件路徑，以及描述提供者支援之事件的查詢清單。 如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。

3.  將 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別的執行載入至 WMI 存放庫。

    WMI 會使用您的類別定義來註冊及存取事件提供者。 如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。

下列程式碼範例說明 [**\_ \_ Win32Provider**](--win32provider.md)類別和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別的實作為。

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

第一個查詢表示提供者會為外來事件類別 FaxEvent 產生所有事件通知。 因為它使用 ISA 運算子，第二個查詢表示提供者會針對 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別及其所有子類別的所有實例建立事件產生通知。

當提供者註冊以提供內建事件時，事件必須套用至類別的所有實例。 換句話說，您無法寫入查詢，只針對屬於 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的部分磁片磁碟機提供實例建立事件。

 

 
