---
description: 暫時和永久取用者具有不同的方法來保護事件傳遞。
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: 安全地接收事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987239"
---
# <a name="receiving-events-securely"></a>安全地接收事件

暫時和永久取用者具有不同的方法來保護事件傳遞。

本主題將討論下列各節：

-   [保護暫時性取用者](#securing-temporary-consumers)
-   [保障永久消費者的安全](#securing-permanent-consumers)
-   [保護永久訂用帳戶](#securing-the-permanent-subscription)
-   [設定 Administrator-Only SD](#setting-an-administrator-only-sd)
-   [模擬事件提供者身分識別](#impersonating-the-event-provider-identity)
-   [Sid 和永久訂閱](#sids-and-permanent-subscriptions)
-   [使用網域帳戶建立永久訂閱](#creating-permanent-subscriptions-using-domain-accounts)
-   [相關主題](#related-topics)

## <a name="securing-temporary-consumers"></a>保護暫時性取用者

暫時的取用 [*者*](gloss-t.md) 會執行，直到系統重新開機或 WMI 已停止，但在引發特定事件時無法啟動。 例如，對 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 的呼叫會建立暫時的取用者。

[**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)或 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)的呼叫會建立暫存事件取用者。 暫時取用者無法控制誰將事件提供給他們所建立的事件 [*接收*](gloss-s.md) 。

[**ExecNotificationQuery**](swbemservices-execnotificationquery.md)方法的呼叫可以同步、[*半同步方式*](gloss-s.md)或非同步方式進行。 例如，根據 *iflags* 參數的設定方式而定， [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)是可呼叫半同步方式的同步方法。 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 是非同步呼叫。

請注意，針對這些呼叫的非同步版本，其接收的回呼可能不會在與腳本呼叫相同的驗證層級傳回。 因此，建議您使用半同步，而不是非同步呼叫。 如果您需要非同步通訊，請參閱 [呼叫方法](calling-a-method.md) 並 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

腳本訂閱者無法檢查事件提供者的存取權限，以提供事件給腳本所建立的接收。 因此，建議 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 的呼叫會使用呼叫的半值形式，並使用特定的安全性設定。 如需詳細資訊，請參閱 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。

## <a name="securing-permanent-consumers"></a>保障永久消費者的安全

[*永久取用者*](gloss-p.md)具有從事件提供者的事件永久訂用帳戶，該事件提供者會在作業系統重新開機後保存。 支援永久取用者的事件提供者是 [*事件*](gloss-e.md)取用者。 如果事件發生時，事件提供者未執行，則 WMI 會在需要傳遞事件時啟動提供者。 WMI 會根據 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)實例識別要傳遞事件的取用者提供者，這會將取用者提供者 [**\_ \_ Win32Provider**](--win32provider.md)實例與取用者提供者所定義的 [*邏輯取用者類別*](gloss-l.md)產生關聯。 如需取用者提供者角色的詳細資訊，請參閱 [撰寫事件](writing-an-event-consumer-provider.md)取用者提供者。

永久取用者可以控制傳送事件的物件，而事件提供者可以控制誰存取其事件。

用戶端腳本和應用程式會在訂用帳戶中建立邏輯取用者類別的實例。 邏輯取用者類別會定義事件所包含的資訊、用戶端可如何處理事件，以及事件的傳遞方式。

WMI [標準取用者類別](standard-consumer-classes.md) 提供邏輯取用者類別角色的範例。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

## <a name="securing-the-permanent-subscription"></a>保護永久訂用帳戶

永久訂用帳戶有可能會導致 WMI 中的安全性問題，因此有下列安全性需求：

-   邏輯取用者實例、 [**\_ \_ >eventfilter**](--eventfilter.md)和 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例必須在 **CreatorSID** 屬性中擁有相同的個別安全識別碼 (SID) 。 如需詳細資訊，請參閱 [在永久訂用帳戶的所有實例中保留相同的 SID](#sids-and-permanent-subscriptions)。
-   建立訂用帳戶的帳戶必須是具有本機系統管理員許可權的網域帳戶或本機系統管理員群組帳戶。 使用系統管理員群組 SID 可讓訂用帳戶在本機電腦上繼續運作，即使它已與網路中斷連線也一樣。 使用網域帳戶可讓使用者進行確切的識別。

    但是，如果電腦未連線，而且建立帳戶是網域帳戶，則取用者會失敗，因為 WMI 無法驗證帳戶的身分識別。 若要避免訂用帳戶在電腦與網路中斷連線時失敗，請使用訂用帳戶的系統管理員群組 SID。 在此情況下，您應該確定 LocalSystem 帳戶可以存取網域上的群組成員資格資料。 某些事件取用者提供者有特別高的安全性需求，因為 rogue 訂用帳戶可能會造成很大的損害。 例如，標準取用者 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 和 [**CommandLineEventConsumer**](commandlineeventconsumer.md)。

-   您可以設定永久訂用帳戶，只接受來自特定事件提供者身分識別的事件。 將 [**\_ \_ >eventfilter**](--eventfilter.md)實例之 **EventAccess** 屬性中的安全描述項設定為事件提供者身分識別。 WMI 會將事件提供者的身分識別與安全描述項進行比較，以判斷提供者是否有 **WBEM \_ 正確的 \_ 發行** 存取權。 如需詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。

    如果篩選準則允許存取事件提供者身分識別，則它也會信任事件。 這可讓接收事件的取用者引發委派的事件。

    **注意** **EventAccess** 中安全描述項的預設值是 **Null**，可允許存取所有人。 建議您限制 [**\_ \_ >eventfilter**](--eventfilter.md)訂閱實例中的存取，以取得更好的事件安全性。

## <a name="setting-an-administrator-only-sd"></a>設定 Administrator-Only SD

下列 c + + 程式碼範例會在 [**\_ \_ >eventfilter**](--eventfilter.md)實例上建立僅限系統管理員的安全描述項。 此範例會使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) 來建立安全描述項。 如需有關 **WBEM \_ 正確 \_ 訂閱** 的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



上述程式碼範例需要下列參考和 \# include 語句。


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>模擬事件提供者身分識別

永久取用者可能需要模擬事件提供者來處理事件。 當下列條件存在時，永久取用者只能模擬事件提供者：

-   [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例的 **MaintainSecurityCoNtext** 屬性設定為 **True**。
-   事件會在產生事件時，在提供者所在的相同安全性內容中傳遞。 只有實作為 DLL 的取用者（同進程取用者）可以在提供者的安全性內容中接收事件。 如需有關同進程提供者和取用者安全性的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。
-   事件提供者正在允許模擬的進程中執行。

執行取用者進程的帳戶必須具有 WMI 儲存機制的 **完整 \_ 寫入** 許可權 (也稱為 CIM 存放庫) 。 在訂用帳戶中， [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)、 [**\_ \_ EventConsumer**](--eventconsumer.md)和 [**\_ \_ >eventfilter**](--eventfilter.md)實例的 **CreatorSID** 屬性中必須有相同的個別安全識別碼 (SID) 值。 WMI 會將 SID 儲存在每個實例的 **CreatorSID** 中。

## <a name="sids-and-permanent-subscriptions"></a>Sid 和永久訂閱

當系結、取用者和篩選準則不是由相同的使用者建立時，永久訂閱無法運作，這表示 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)、 [**\_ \_ EventConsumer**](--eventconsumer.md)和 [**\_ \_ >eventfilter**](--eventfilter.md)在 **CreatorSID** 屬性中必須有相同的個別安全識別碼 (SID) 值。 Windows Management Instrumentation (WMI) 儲存此值。

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>使用網域帳戶建立永久訂閱

使用網域帳戶來建立永久訂閱時，必須考慮幾個問題。 每個永久訂用帳戶在沒有使用者登入時仍可運作，這表示他們在內建的 LocalSystem 帳戶下運作。

如果網域使用者是安全機密取用者的永久訂用帳戶建立者 ([**ActiveScriptEventConsumer**](activescripteventconsumer.md)、 [**CommandLineEventConsumer**](commandlineeventconsumer.md)) ，則 WMI 會驗證 [**\_ \_ >eventfilter**](--eventfilter.md)類別、 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)類別和取用者實例的 **CreatorSID** 屬性是否屬於本機 Administrators 群組成員的使用者。

下列程式碼範例會顯示如何指定 **CreatorSID** 屬性。

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

針對跨網域狀況，請將已驗證的使用者新增至「Windows 授權存取群組」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[保護 WMI 事件](securing-wmi-events.md)
</dt> <dt>

[接收 WMI 事件](receiving-a-wmi-event.md)
</dt> </dl>

 

 
