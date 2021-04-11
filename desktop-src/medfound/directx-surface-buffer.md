---
description: DirectX 介面緩衝區
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: DirectX 介面緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111788"
---
# <a name="directx-surface-buffer"></a>DirectX 介面緩衝區

DirectX 介面緩衝區物件是管理 Direct3D 介面的媒體緩衝區。 若要建立這個物件的實例，請呼叫 [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) 並傳入 DirectX 介面的指標。 DirectX 介面緩衝區會公開下列介面：

-   [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

有數種方式可從緩衝區物件存取 surface memory：

-   建議：對緩衝區呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 。 使用服務識別碼 **MR \_ 緩衝區 \_ 服務**。 方法會傳回基礎 Direct3D 介面的指標。
-   呼叫 [**IMF2DBuffer：： Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d)。 這個方法會直接在介面上呼叫 **IDirect3DSurface9：： LockRect** 。 [**IMF2DBuffer：： Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d)方法會在介面上呼叫 **UnlockRect** 。
-   呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)。 一般而言，這不是建議的作法，因為它會強制物件從 Direct3D 介面複製記憶體，然後再次返回。 [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d)方法更有效率。

如果基礎資料表面無法鎖定，則 [**鎖定**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 和 [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 可能會失敗。 DirectX 介面緩衝區會針對並非設計來搭配 Direct3D 介面運作的元件，執行這兩種方法。

增強型影片轉譯器 (EVR) 在未針對 DirectX Video 加速 (DXVA) 設定解碼器時，會建立 DirectX 介面緩衝區。 如需詳細資訊，請參閱 [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)。

### <a name="obtaining-the-direct3d-surface"></a>取得 Direct3D 介面

若要從影片範例取得 Direct3D 介面，請執行下列動作：

1.  以零的索引值呼叫 [**IMFSample：： GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) 。
2.  呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 並指定 **MR \_ 緩衝區 \_ 服務** 服務識別碼。

下列程式碼顯示這些步驟：


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體緩衝區](media-buffers.md)
</dt> <dt>

[影片範例](video-samples.md)
</dt> </dl>

 

 



