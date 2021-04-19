---
description: 測試圖形驅動程式是否支援 COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: 測試圖形驅動程式是否支援 COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987722"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a><span data-ttu-id="b58fd-103">測試圖形驅動程式是否支援 COPP</span><span class="sxs-lookup"><span data-stu-id="b58fd-103">Testing Whether a Graphics Driver Supports COPP</span></span>

<span data-ttu-id="b58fd-104">經認證的輸出保護通訊協定 (COPP) 可讓應用程式在視訊卡從視訊卡移動到顯示裝置時，保護其內容。</span><span class="sxs-lookup"><span data-stu-id="b58fd-104">Certified Output Protection Protocol (COPP) enables an application to protect video content as it travels from the video card to the display device.</span></span> <span data-ttu-id="b58fd-105">如果圖形驅動程式支援 COPP，則驅動程式會保留由 Microsoft 簽署的憑證鏈，以驗證驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b58fd-105">If a graphics driver supports COPP, the driver holds a certificate chain, signed by Microsoft, authenticating the driver.</span></span> <span data-ttu-id="b58fd-106">使用 COPP 強制執行內容保護的播放應用程式必須驗證憑證鏈，以確保驅動程式未遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="b58fd-106">Playback applications that use COPP to enforce content protection must validate the certificate chain to ensure that the driver has not been tampered with.</span></span>

<span data-ttu-id="b58fd-107">不過，您可能會想要檢查圖形驅動程式是否支援 COPP，而不需驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b58fd-107">However, you might want to check whether a graphics driver supports COPP, without validating the certificate.</span></span> <span data-ttu-id="b58fd-108">例如，當數位媒體提供者發出數位版權管理 (DRM) 授權時，可能會想要檢查使用者是否有已啟用 COPP 的圖形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b58fd-108">For example, when a digital media provider issues a digital rights management (DRM) license, it might want to check whether the user has a COPP-enabled graphics driver.</span></span> <span data-ttu-id="b58fd-109">提供者不需要在發出授權時強制執行 COPP;它只需要測試驅動程式是否支援 COPP。</span><span class="sxs-lookup"><span data-stu-id="b58fd-109">The provider does not need to enforce COPP at the time it issues the license; it only needs to test whether the driver supports COPP.</span></span>

<span data-ttu-id="b58fd-110">下列程式碼顯示如何測試驅動程式是否支援 COPP。</span><span class="sxs-lookup"><span data-stu-id="b58fd-110">The following code shows how to test whether a driver supports COPP.</span></span> <span data-ttu-id="b58fd-111">應用程式必須傳入將用來測試驅動程式的影片檔案名。</span><span class="sxs-lookup"><span data-stu-id="b58fd-111">The application must pass in the name of a video file that will be used to test the driver.</span></span> <span data-ttu-id="b58fd-112">這是必要的，因為在連線到篩選器之前，Microsoft® DirectShow®的影片混合轉譯器篩選器不會將 COPP 會話初始化。</span><span class="sxs-lookup"><span data-stu-id="b58fd-112">This is required because the Video Mixing Renderer filter in Microsoft® DirectShow® does not initialize a COPP session until the filter is connected.</span></span> <span data-ttu-id="b58fd-113">此函數可以包含在用戶端應用程式中，以檢查驅動程式是否能夠執行 COPP。</span><span class="sxs-lookup"><span data-stu-id="b58fd-113">This function can be included in a client application to check if the driver is capable of running COPP.</span></span>

> [!Note]  
> <span data-ttu-id="b58fd-114">如果使用者的電腦有兩個圖形配接器，此函式會測試主要圖形配接器的驅動程式，而不是次要圖形配接器的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b58fd-114">If the user's computer has two graphics cards, this function tests the driver for the primary graphics card, but not the secondary graphics card.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="b58fd-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b58fd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b58fd-116">使用經認證的輸出保護通訊協定</span><span class="sxs-lookup"><span data-stu-id="b58fd-116">Using Certified Output Protection Protocol</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



