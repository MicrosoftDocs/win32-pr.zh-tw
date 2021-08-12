---
description: 測試圖形驅動程式是否支援 COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: 測試圖形驅動程式是否支援 COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651828"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>測試圖形驅動程式是否支援 COPP

經認證的輸出保護通訊協定 (COPP) 可讓應用程式在視訊卡從視訊卡移動到顯示裝置時，保護其內容。 如果圖形驅動程式支援 COPP，則驅動程式會保留由 Microsoft 簽署的憑證鏈，以驗證驅動程式。 使用 COPP 強制執行內容保護的播放應用程式必須驗證憑證鏈，以確保驅動程式未遭到篡改。

不過，您可能會想要檢查圖形驅動程式是否支援 COPP，而不需驗證憑證。 例如，當數位媒體提供者發出數位版權管理 (DRM) 授權時，可能會想要檢查使用者是否有已啟用 COPP 的圖形驅動程式。 提供者不需要在發出授權時強制執行 COPP;它只需要測試驅動程式是否支援 COPP。

下列程式碼顯示如何測試驅動程式是否支援 COPP。 應用程式必須傳入將用來測試驅動程式的影片檔案名。 這是必要的，因為 Microsoft® DirectShow®的影片混合轉譯器篩選器在連接篩選器之前，不會將 COPP 會話初始化。 此函數可以包含在用戶端應用程式中，以檢查驅動程式是否能夠執行 COPP。

> [!Note]  
> 如果使用者的電腦有兩個圖形配接器，此函式會測試主要圖形配接器的驅動程式，而不是次要圖形配接器的驅動程式。

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用經認證的輸出保護通訊協定](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



