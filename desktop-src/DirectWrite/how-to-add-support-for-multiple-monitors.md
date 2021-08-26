---
title: 如何新增多個監視器的支援
description: DirectWrite 包含多個監視器的系統支援。
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bbfb2c803372e52128cd62dddeec407985e4180039d84f9aed66092149911b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048888"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>如何新增多個監視器的支援

[DirectWrite](direct-write-portal.md)包含多個監視器的系統支援。 不同的監視器可能會有不同的圖元幾何 (RGB、BGR 或平面) 或其他屬性。 如需圖元幾何的詳細資訊，請參閱 [**DWRITE \_ 圖元 \_ 幾何**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) 參考主題。 本主題將說明如何將多個監視器的支援新增至您的 DirectWrite 應用程式。

為了支援多個監視器，您必須處理 **WM \_ WINDOWPOSCHANGED** 視窗訊息。 此訊息會在移動視窗時傳送，因此您必須檢查視窗是否已移至不同的監視器，如下列程式碼所示。


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



如果視窗位於新的監視器上，您就必須使用 [**IDWriteFactory：： CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) 方法來建立新監視器的呈現參數。

> [!Note]  
> 請勿使用 [**IDWriteFactory：： CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) 方法來建立轉譯參數，因為它一律會建立主要監視器的參數。

 

當您有 [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) 物件時，請使用 [**ID2DRenderTarget：： SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) 方法設定轉譯目標的轉譯參數。

最後，使用 [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) 函式，讓視窗以新的轉譯參數重新繪製。

 

 