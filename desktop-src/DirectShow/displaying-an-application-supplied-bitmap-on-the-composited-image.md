---
title: 在複合影像上顯示應用程式提供的點陣圖
description: 在複合影像上顯示 Application-Supplied 點陣圖
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90768cc9ba9ed3a7f53336c63b0112f297e1844ba9638799e8badf28588775eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653512"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>在複合影像上顯示應用程式提供的點陣圖

應用程式可以使用 VMR 的混合模式，在影片矩形內部分或完全顯示 Alpha 混合的通道標誌、使用者介面或廣告。 因為圖形處理器會在硬體中執行混合，所以對影片串流的播放效能會有最大的影響，而且沒有可偵測的閃爍或撕裂的成品。 應用程式可以視需要頻繁地變更顯示的影像。 請注意，只有當 DirectShow 篩選圖形處於 [執行中] 狀態時，才會在螢幕上反映變更。

VMR 會使用其混音器元件，將點陣圖重迭至複合影像。 使用 VMR-7 時，應用程式必須強制 VMR 載入其混音器，即使只有一個影片串流也一樣。 VMR-9 並不需要這麼做，因為它預設會載入其混音器。

為了 blend 靜態點陣圖影像與影片資料流程，應用程式會建立 VMR 並將它新增至圖形，然後呼叫 [**IVMRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)。 傳遞給此函式的值會識別 VMR 應該建立的輸入圖釘數目。 應用程式可以指定介於1到最大混音器串流之間的任何值 \_ \_ ; 如果應用程式只是要顯示單一影片串流，則指定1的值是有效的。 即使 VMR-7 預設有單一輸入 pin，還是必須呼叫這個方法，才能強制它載入其混音器元件。  (VMR-9 預設會載入其混音器並設定四個 pin。 ) 

若要設定點陣圖，請使用 VMR 7 上的 [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) 介面或 VMR-9 上的 [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) 介面。

您可以透過 GDI 裝置內容的控制碼 (hDC) 或 DirectDraw 介面介面來指定點陣圖。 如果應用程式想要影像包含內嵌的 Alpha 資訊 (也知道每個圖元的 Alpha) 必須將影像資料放在 DirectDraw 介面介面中。 這是因為目前無法使用 GDI 裝置內容來放置每個圖元的 Alpha 資訊。 DirectDraw 表面必須是 RGB32 或 ARGB32，而且最好是系統記憶體介面。 表面維度不需要是2的乘冪。

VMR 可讓應用程式指定影像的位置和整體透明度值。 下列程式碼示範如何將影像資料向下傳遞至 VMR，以進行後續的混合：


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



本主題所討論的概念是在 [VMRPlayer 範例](vmrplayer-sample.md) 應用程式範例中示範。

**使用點陣圖影像建立簡單的動畫**

若要建立簡單的動畫點陣圖標誌，請將所有點陣圖「框架」放入單一影像中，如下圖所示。

![vmr 圖像塊](images/vmr-image-strip.png)

當您一開始使用 [**IVMRMixerBitmap：： SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap)設定點陣圖時，如果點陣圖位於 hdc 中，請設定 **VMRALPHABITMAP** 結構的 **.rsrc** 欄位，以指定在 hdc 內整個點陣圖的大小。 結構的 **top** 和 **left** 成員會設定為0，而 **右邊** 和 **下** 成員則是點陣圖的寬度和高度。 如果點陣圖在 DirectDraw 表面中，則會知道介面大小，因此不需要在此方法中指定 .Rsrc。

當您呼叫 [**IVMRMixerBitmap：： UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)時，請針對 HDC 和 DirectDraw 點陣圖使用 **.rsrc** 成員，以指定您想要顯示之影像內的特定框架或矩形，然後在 **>srcrect** 成員中設定 **VMRBITMAP \_ dwFlags** 旗標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



