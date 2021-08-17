---
description: 執行 DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: 執行 DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39d55b73dd70a21c10df26a100f964917a57dd9f036ebd5c2708359bca1dd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998089"
---
# <a name="implementing-dllregisterserver"></a>執行 DllRegisterServer

最後一個步驟是執行 **DllRegisterServer** 函數。 包含元件的 DLL 必須匯出此函數。 設定應用程式或使用者執行 Regsvr32.exe 工具時，會呼叫此函式。

下列範例顯示最基本的 **DlLRegisterServer** 執行：


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



[**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函式會為每個元件建立登錄專案。


```
g_Templates
```



陣列。 不過，此函數有一些限制。 首先，它會將每個篩選指派給「DirectShow 篩選」類別 (CLSID \_ LegacyAmFilterCategory) ，但並非每個篩選都屬於此類別。 例如，「捕獲篩選準則」和「壓縮」篩選器都有自己的類別。 其次，如果您的篩選器支援硬體裝置，您可能需要註冊兩項額外的資訊， **AMovieDLLRegisterServer2** 不會處理這些資訊： *媒體* 和 *pin 類別*。 媒體定義了硬體裝置（例如匯流排）的通訊方法。 Pin 類別會定義 pin 的功能。 如需媒體的相關資訊，請參閱 \_ Microsoft Windows 驅動程式開發工具組中的 "KSPIN MEDIUM" (DDK) 。 如需 pin 類別的清單，請參閱 [釘選屬性集](pin-property-set.md)。

如果您想要指定篩選類別、媒體或釘選類別，請從 **DllRegisterServer** 內呼叫 [**IFilterMapper2：： RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter)方法。 這個方法會採用 [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) 結構的指標，此結構會指定篩選的相關資訊。

為了讓事情稍微複雜一點， **REGFILTER2** 結構支援兩種不同的格式來註冊 pin。 **DwVersion** 成員會指定格式：

-   如果 **dwVersion** 是1，則 pin 格式為 **AMOVIESETUP \_ pin** (先前) 所述。
-   如果 **dwVersion** 為2，則會 [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2)pin 格式。

**REGFILTERPINS2** 結構包含 pin 媒體和 pin 類別目錄的專案。 此外，針對 **AMOVIESETUP \_ 釘** 選為布林值的某些專案，它會使用位旗標。

下列範例顯示如何從 **DllRegisterServer** 內部呼叫 **IFilterMapper2：： RegisterFilter** ：


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



