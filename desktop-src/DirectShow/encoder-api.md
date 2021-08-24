---
description: 編碼器 API
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: 編碼器 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b97dc2242cc718605a851186c726e3301493b7637b94e88b7987868741874a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823638"
---
# <a name="encoder-api"></a>編碼器 API

編碼器 API 提供統一的介面來設定軟體和硬體編碼器。 應用程式可以使用編碼器 API 來設定編碼器和儲存設定。 編碼器廠商可使用編碼器 API 來公開編碼器的功能。 雖然編碼器 API 主要是針對編碼器所設計，但它通常也足以支援它。

編碼器 API 會透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面（由編碼器篩選器公開）公開給應用程式。 編碼器篩選器可能是原生 DirectShow 濾波器、硬體編碼器或 DirectX 媒體物件 (DMO) 。

-   軟體篩選：實作為原生 DirectShow 篩選器的編碼器應該直接公開 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 。
-   硬體編碼器：編碼裝置會透過一或多個 AVStream minidrivers 公開，KSProxy 會在使用者模式中表示。 KSProxy 會將 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 方法呼叫轉譯為 KS 屬性集。 如需詳細資訊，請參閱 DDK 檔。
-   DMOs： DMO 應該公開 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)介面。 DirectShow 的應用程式可以查詢 DMO 包裝函式篩選器，藉由匯總 DMO 來公開介面。 以 DirectShow 為基礎的應用程式可以直接查詢 DMO。

### <a name="encoder-capabilties"></a>編碼器功能

編碼器可以將高階功能的清單儲存在系統登錄中，以註冊它們。 每項功能都是由 GUID 所識別。 若要列舉特定編碼器的功能，請執行下列動作：

1.  建立代表編碼器篩選器的標記。  (參閱 [使用系統裝置列舉](using-the-system-device-enumerator.md)值。 ) 
2.  查詢 [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) 介面的篩選準則標記。
3.  呼叫 [**IGetCapabilitiesKey：： GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey)。 方法會將控制碼傳回至包含篩選功能清單的登錄機碼。
4.  呼叫 **RegEnumValue** 函式來列舉傳回索引鍵的值。

如果您要開發編碼器，請在註冊篩選器時建立這些功能的登錄專案。 針對軟體篩選器，請建立名為「 **功能** 」的金鑰，該金鑰與 **FilterData** 和 **FriendlyName** 金鑰相鄰。 一般而言，您會在呼叫 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 之後加入這項資訊，以註冊標準篩選資料。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。 或者，您可以建立 **CapabilitiesLocation** 索引鍵，其中包含的字串可提供登錄中的 **功能** 金鑰位置。 字串的開頭應該是 "HKLM \\ "、"HKCR \\ " 或 "HKCU \\ "，以表示登錄子樹。 針對隨插即用裝置，驅動程式的安裝檔應該建立與篩選的 **FriendlyName** 金鑰連續的 **功能** 金鑰，也可以使用 **CapabilitiesLocation** 金鑰，如軟體篩選器所述。

建立 **功能** 金鑰之後，請為每個功能 GUID 建立一個值。 值的名稱應該是 GUID 的字串格式，格式為 `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` 。 每個實值型別都應該是下列其中一項：

-   單一數值。 使用 **DWORD** 值。
-   GUID。 使用 GUID 的字串形式。
-   數值配對。 使用格式為 "a，b" 的字串來代表值的配對，例如寬度和高度，或分數的分子和分母。
-   值的陣列。 使用多字串 (**REG \_ SZ \_ 多重**) 來代表一個以上的值。

下列範例顯示軟體篩選器的登錄配置：


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>編碼器設定檔

*編碼器設定檔* 是固定的設定值清單，可在執行時間套用至編碼器。 設定檔與編碼器無關;應用程式可以選取編碼器，然後選取設定檔並將設定檔設定套用至編碼器。 設定檔是由 GUID 識別，且應儲存在登錄中的下列位置：


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



*設定檔 GUID*

這是識別設定檔的 GUID 字串形式。 建立每個設定的值。 此外，請建立名為 "FriendlyName" 的字串值，其資料會識別設定檔 (例如 "LowBandwidthVideo" ) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編碼器和解碼器開發](encoder-and-decoder-development.md)
</dt> </dl>

 

 



