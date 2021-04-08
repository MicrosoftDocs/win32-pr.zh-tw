---
title: 註冊 DSP 外掛程式
description: 註冊 DSP 外掛程式
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Windows Media Player 外掛程式、登錄專案
- 外掛程式，登錄專案
- 數位信號處理外掛程式，登錄專案
- DSP 外掛程式，登錄專案
- 登錄、DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932937"
---
# <a name="registering-dsp-plug-ins"></a>註冊 DSP 外掛程式

若要在 Windows Media Player 中提供您的 DSP 外掛程式，您必須在使用者的電腦上建立下列登錄子機碼和專案。


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



在上述的登錄語法中，斜體的符號是 (Guid 外掛程式專屬的 Guid) 的名稱和全域唯一識別碼的預留位置。 下表描述這些預留位置。



| 預留位置               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | GUID，這是 DSP 外掛程式主要類別的類別識別碼。 這是實 **IMediaObject**、 **IPluginEnable** 和可能 **ISpecifyPropertyPages** 的類別。 在雙重模式的外掛程式中，此類別也會執行 **IMFTransform** 和 **IMFGetService**。此 GUID 必須是登錄格式，以大括弧完成。<br/> 格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/> |
| *PluginClassFriendlyName* | DSP 外掛程式主要類別的易記名稱。範例： "ProsewareDSP Class"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | 執行 DSP 外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *執行緒*               | 字串，指定外掛程式的執行緒模型。 如果外掛程式要在 Windows Vista 上以 Windows Media Player 11 執行，此登錄專案必須等於「兩者」。 如果外掛程式即將在 Windows XP 或較舊的作業系統上執行，此登錄專案可以等於 "公寓" 或 "Both"。                                                                                           |



 

如果您的 DSP 外掛程式會執行自訂介面，且外掛程式即將在 Windows Vista 上的 Windows Media Player 11 中執行，您必須在使用者的電腦上建立下列登錄子機碼和專案。


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



在上述的登錄語法中，以斜體表示的符號是名稱、數值和全域唯一識別碼的預留位置， (Guid 外掛程式專屬的 Guid) 。 下表描述這些預留位置。



| 預留位置           | 描述                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | GUID，這是類別的類別識別碼，可針對 DSP 外掛程式的自訂介面，執行 proxy 和存根。此 GUID 必須是登錄格式，以大括弧完成。<br/> 格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/> |
| *ProxyStubModuleName* | 針對 DSP 外掛程式執行 proxy 和存根介面之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | GUID，這是由 DSP 外掛程式所執行之自訂介面的介面識別碼。此 GUID 必須是登錄格式，以大括弧完成。<br/> 格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/>                           |
| *CustomInterfaceName* | DSP 外掛程式所執行之自訂介面的名稱。範例： "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | 自訂介面所定義之方法的數目，包括繼承的方法。範例： "5"<br/>                                                                                                                                                                  |



 

如果您的 DSP 外掛程式提供屬性頁，您必須在使用者的電腦上建立下列登錄子機碼和專案。


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



在上述的登錄語法中，斜體的符號是 (Guid 外掛程式專屬的 Guid) 的名稱和全域唯一識別碼的預留位置。 下表描述這些預留位置。



| 預留位置                 | 描述                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | GUID，這是 DSP 外掛程式所提供之屬性頁類別的類別識別碼。此 GUID 必須是登錄格式，以大括弧完成。<br/> 格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。<br/> |
| *PropPageClassFriendlyName* | 屬性頁類別的易記名稱。範例： "ProsewareDSP Property Page Class"<br/>                                                                                                                                     |
| *PluginModuleName*          | 執行 DSP 外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**呼叫 IWMPPluginRegistrar**

除了上述清單和資料表中所述的登錄子機碼和專案以外，您還必須呼叫 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin)來建立一些登錄機碼和專案。 這個方法會執行必要的註冊，讓 Windows Media Player 辨識您的外掛程式，並將其顯示為使用者的選項。

在外掛程式的 **DllRegisterServer** 函式中呼叫 **IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin** ，然後在外掛程式的 **WMPUnRegisterPlayerPlugin** 函數中呼叫 [IWMPMediaPluginRegistrar：： DllUnregisterServer](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) 。 若要取得 **IWMPMediaPluginRegistrar** 介面的指標，請呼叫 **COCREATEINSTANCE**，將 CLSID \_ WMPMediaPluginRegistrar 傳遞為類別識別碼。 常數 CLSID \_ WMPMediaPluginRegistrar 是在 wmpservices 中定義。

**在 DSP 外掛程式嚮導中註冊**

Windows SDK 中包含的 DSP 外掛程式 wizard 會根據 Active Template Library (ATL) 產生範例程式碼。 範例外掛程式的 **DllRegisterServer** 函式會呼叫 ATL 的 **RegisterServer** 函式，此函式會根據 Visual Studio 專案中的兩個登入指令檔檔，建立登錄子機碼和專案。 檔案 *名稱* 為 .rgs 包含用來註冊外掛程式主要類別的腳本，而檔案 *專案名稱* PropPage 則包含用來註冊外掛程式屬性頁類別的腳本。 範例外掛程式的 **DllRegisterServer** 函數也會呼叫 **IWMPPluginRegistrar：： WMPRegisterPlayerPlugin**。

DSP 外掛程式 wizard 也會產生自我註冊 .dll 檔案之 proxy 存根元件的程式碼。 該檔案的註冊碼位於 dlldata.c .cpp 中。 宏 **Dlldata.c \_ 常式** 會展開以包含 **DllRegisterServer** 的執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





