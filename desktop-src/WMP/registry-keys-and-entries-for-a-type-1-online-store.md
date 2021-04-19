---
title: 類型1線上商店的登錄機碼和專案
description: 類型1線上商店的登錄機碼和專案
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player 線上商店，登錄
- 線上商店、登錄
- 輸入1個線上商店、登錄
- 登錄，請輸入1個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966440"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>類型1線上商店的登錄機碼和專案

若要在 Windows Media Player 中提供類型1線上商店，線上商店提供者必須在使用者的電腦上建立下列登錄子機碼和專案。


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> 將 DllSurrogate 的值設為空字串，表示 COM 執行時間會將線上商店的外掛程式載入預設 DLL 代理，dllhost.exe。

 

在上述的登錄語法中，以斜體表示的符號是 (Guid) 的名稱和全域唯一識別碼的預留位置，這些是線上商店專屬的識別碼。 下表描述這些預留位置。



| 預留位置    | 描述                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | 在 Microsoft 與線上商店之間同意的字串。 這個字串可唯一識別線上商店。範例： "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | 一或多個外掛程式功能旗標的位 **or** 會指定 Windows Media Player 是否應該呼叫 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)的特定方法。 如需支援之旗標的詳細資訊，請參閱此表格後面的外掛程式功能旗標表。範例：00000058<br/> |
| *Clsid*        | GUID，也就是在線上商店的外掛程式中執行 **IWMPContentPartner** 之類別的類別識別碼 (CLSID) 。 此 GUID 必須是登錄格式，以大括弧完成。格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/>                                                                  |
| *友好* | 線上商店的易記名稱。範例：「Proseware 音樂服務」<br/>                                                                                                                                                                                                                                              |
| *appid*        | GUID，這是線上商店的外掛程式 (AppID) 的應用程式識別碼。 此 GUID 必須是登錄格式，以大括弧完成。格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/>                                                                                                                |
| *pluginName*   | 線上商店外掛程式的名稱。範例： "Proseware Content Partner 外掛程式"<br/>                                                                                                                                                                                                                                   |
| *className*    | 在線上商店的外掛程式中，用來執行 **IWMPContentpartner** 的類別名稱。範例： "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | 執行線上存放區外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *執行緒*    | 外掛程式執行所在的公寓型別。 ">threadingmodel" = "公寓" 表示外掛程式會在單一執行緒的單元 (STA) 中執行。 ">threadingmodel" = "Free" 表示外掛程式會在多執行緒單元 (MTA) 中執行。                                                                                     |



 

下表描述外掛程式功能旗標。



| 旗標                                    | 值 | 描述                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 訂用帳戶 \_ 上限 \_ BACKGROUNDPROCESSING | 0x8   | Windows Media Player 應呼叫 [IWMPContentPartner：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) ，以通知外掛程式應該啟動並停止背景處理。                                                                                                     |
| 訂用帳戶 \_ 上限 \_ DEVICEAVAILABLE      | 0x10  | Windows Media Player 應呼叫 [IWMPContentPartner：： UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice)。                                                                                                                                                                   |
| 訂用帳戶 \_ 上限 \_ 為 \_ CONTENTPARTNER   | 0x40  | 通知 Windows Media Player 外掛程式會執行 **IWMPContentPartner** 介面。 所有類型1線上商店外掛程式都必須設定此旗標。                                                                                                                         |
| 訂用帳戶 \_ 上限 \_ ALTLOGIN             | 0x80  | 通知 Windows Media Player 外掛程式支援替代登入。 如果外掛程式支援替代登入，Windows Media Player 會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，以抓取替代登入 URL 和標題。 |



 

**用於開發和測試的登錄專案**

當您開始開發線上商店時，Microsoft 會提供您兩個金鑰：測試金鑰和生產金鑰。 在開發和測試階段中，只有當您的測試金鑰或生產金鑰位於使用者電腦的登錄中時，您的線上商店才會出現在 Windows Media Player 中。 如需有關測試和生產金鑰的詳細資訊，請參閱 [類型1線上商店的測試和生產金鑰](test-and-production-keys-for-a-type-1-online-store.md)。

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

[**類型 1 線上商店的參考**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





