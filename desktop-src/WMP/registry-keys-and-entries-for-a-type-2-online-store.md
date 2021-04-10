---
title: Type 2 線上商店的登錄機碼和專案
description: Type 2 線上商店的登錄機碼和專案
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player 線上商店，登錄
- 線上商店、登錄
- 輸入2個線上商店、登錄
- 登錄，類型2線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092578"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Type 2 線上商店的登錄機碼和專案

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

若要在 Windows Media Player 中提供類型2線上商店，線上商店提供者必須在使用者的電腦上建立下列登錄子機碼和專案。


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



在上述的登錄語法中，以斜體表示的符號是 (Guid) 的名稱和全域唯一識別碼的預留位置，這些是線上商店專屬的識別碼。 下表描述這些預留位置。



| 預留位置    | 描述                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | 在 Microsoft 與線上商店之間同意的字串。 這個字串可唯一識別線上商店。範例： "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | 一或多個外掛程式功能旗標的位 **or** 會指定 Windows Media Player 是否應該呼叫 [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) 和 [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)的特定方法。 如需支援之旗標的詳細資訊，請參閱此表格後面的外掛程式功能旗標表。範例：00000037<br/> |
| *Clsid*        | GUID，也就是在線上商店的外掛程式中執行 **IWMPSubscriptionService** 之類別的類別識別碼 (CLSID) 。 此 GUID 必須是登錄格式，以大括弧完成。格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/>                                                                                                                                    |
| *友好* | 線上商店的易記名稱。範例：「Proseware 音樂服務」<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | 線上商店外掛程式的名稱。範例： "Proseware Service 外掛程式"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | 在線上商店的外掛程式中，用來執行 **IWMPSubscriptionService** 的類別名稱。範例： "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | 執行線上存放區外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

下表描述外掛程式功能旗標。



| 旗標                                    | 值 | 描述                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 訂用帳戶 \_ 上限 \_ ALLOWPLAY            | 0X1   | Windows Media Player 應呼叫 [IWMPSubscriptionService：： allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)。                                                                                                                      |
| 訂用帳戶 \_ 上限 \_ ALLOWCDBURN          | 0X2   | Windows Media Player 應呼叫 [IWMPSubscriptionService：： allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn)。                                                                                                                  |
| 訂用帳戶 \_ 上限 \_ ALLOWPDATRANSFER     | 0X4   | Windows Media Player 應呼叫 [IWMPSubscriptionService：： allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer)。                                                                                                        |
| 訂用帳戶 \_ 上限 \_ BACKGROUNDPROCESSING | 0X8   | Windows Media Player 應呼叫 [IWMPSubscriptionService：： startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing)。                                                                                      |
| 訂用帳戶 \_ 上限 \_ DEVICEAVAILABLE      | 0X10  | Windows Media Player 應呼叫 [IWMPSubscriptionService2：:D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)。                                                                                                        |
| 訂用帳戶 \_ 上限 \_ PREPAREFORSYNC       | 0X20  | Windows Media Player 應呼叫 [IWMPSubscriptionService2：:P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync)。                                                                                                          |
| 訂用帳戶 \_ V1 \_ cap                  | 0XF   | 預設值。 如果未註冊任何，則會使用此值。 這相當於合併訂用帳戶 \_ cap \_ ALLOWPLAY、訂用帳戶 \_ 上限 ALLOWCDBURN、訂用帳戶上限 \_ \_ \_ ALLOWPDATRANSFER 和訂用帳戶 \_ 上限 \_ BACKGROUNDPROCESSING。 |



 

**用於開發和測試的登錄專案**

當您開始開發線上商店時，Microsoft 會提供您兩個金鑰：測試金鑰和生產金鑰。 在開發和測試階段中，只有當您的測試金鑰或生產金鑰位於使用者電腦的登錄中時，您的線上商店才會出現在 Windows Media Player 中。 如需有關測試和生產金鑰的詳細資訊，請參閱 [類型2線上商店的測試和生產金鑰](test-and-production-keys-for-a-type-2-online-store.md)。

將您的測試或生產金鑰放在登錄中的下列位置。


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



請注意，TestParameter 登錄專案的值可以指定多個測試或生產金鑰。 例如，假設 Proseware 的測試金鑰為 "1234"，而 Contoso 的測試金鑰為 "2345"。 下列登錄專案指定 Proseware 和 Contoso 的測試存放區將會出現在 Windows Media Player 中。


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**ActiveService 登錄專案**

當使用者啟動線上商店時，Windows Media Player 寫入登錄中的資訊，以識別作用中的線上商店。 Windows Media Player 將資訊放在使用者電腦上登錄的下列位置中。


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



在上述的登錄語法中， *serviceInfo* 是字串的預留位置，其中包含作用中線上商店的描述性資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型 2 線上商店的參考**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





