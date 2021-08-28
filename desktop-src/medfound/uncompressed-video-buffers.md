---
description: 未壓縮的影片緩衝區
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: 未壓縮的影片緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a54c234ca3e5cd1798f50893101f758a374335db8bb9305fd2e3f0ddab75fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972747"
---
# <a name="uncompressed-video-buffers"></a>未壓縮的影片緩衝區

本文說明如何使用包含未壓縮影片畫面的媒體緩衝區。 依喜好設定的順序，有下列選項可供使用。 並非每個媒體緩衝區都支援每個選項。

1.  使用基礎 Direct3D 介面。  (僅適用于儲存在 Direct3D 介面中的影片畫面。 ) 
2.  使用 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。
3.  使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。

## <a name="use-the-underlying-direct3d-surface"></a>使用基礎 Direct3D 介面

影片畫面可能儲存在 Direct3D 介面內。 若是如此，您可以呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 或 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 在媒體緩衝區物件上取得介面指標。 使用服務識別碼 MR \_ 緩衝區 \_ 服務。 當存取影片畫面的元件設計為使用 Direct3D 時，建議使用此方法。 例如，支援 DirectX Video 加速的影片解碼應使用此方法。

下列程式碼顯示如何從媒體緩衝區取得 **IDirect3DSurface9** 指標。


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



下列物件支援 **MR \_ 緩衝區 \_ 服務** 服務：

-   [DirectX 介面緩衝區](directx-surface-buffer.md)
-   [影片範例](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>使用 IMF2DBuffer 介面

如果影片畫面未儲存在 Direct3D 介面內，或元件不是設計成使用 Direct3D，則下一次存取影片框架的建議方式是查詢 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面的緩衝區。 此介面是專為影像資料所設計。 若要取得這個介面的指標，請呼叫媒體緩衝區上的 **QueryInterface** 。 並非所有媒體緩衝區物件都會公開這個介面。 但是，如果媒體緩衝區確實公開了 **IMF2DBuffer** 介面，您應該使用該介面來存取資料（可能的話），而不是使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)。 您仍然可以使用 **IMFMediaBuffer** 介面，但效率可能較低。

1.  呼叫媒體緩衝區上的 **QueryInterface** 來取得 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。
2.  呼叫 [**IMF2DBuffer：： Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 來存取緩衝區的記憶體。 這個方法會傳回最上層圖元的第一個位元組指標。 它也會傳回影像跨距，也就是從資料列開始到下一個資料列開頭的位元組數目。 緩衝區可能會在每個圖元資料列之後包含填補位元組，因此跨距可能會超出影像寬度（以位元組為單位）。 如果在記憶體中將影像導向最下層，則 Stride 也可以是負數。 如需詳細資訊，請參閱 [影像 Stride](image-stride.md)。
3.  只有當您需要存取記憶體時，才讓緩衝區保持鎖定。 藉由呼叫 [**IMF2DBuffer：： Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d)來解除鎖定緩衝區。

並非每個媒體緩衝區都能實行 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。 如果媒體緩衝區未執行這個介面 (也就是，在步驟 1) 中，緩衝區物件會傳回 E \_ NOINTERFACE，您必須使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面介面（如下所述）。

## <a name="use-the-imfmediabuffer-interface"></a>使用 IMFMediaBuffer 介面

如果媒體緩衝區未公開 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面，請使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。 [使用媒體緩衝區](working-with-media-buffers.md)的主題將描述此介面的一般語法。

1.  呼叫媒體緩衝區上的 **QueryInterface** 來取得 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。
2.  呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以存取緩衝區記憶體。 這個方法會傳回緩衝區記憶體的指標。 使用 **鎖定** 方法時，stride 一律是有問題的影片格式最小的 stride，沒有額外的填補位元組。
3.  只有當您需要存取記憶體時，才讓緩衝區保持鎖定。 藉由呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)來解除鎖定緩衝區。

如果緩衝區公開 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)，您應該一律避免呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) ，因為 **Lock** 方法可以強制緩衝區物件進入連續的記憶體區塊，然後再次返回。 另一方面，如果緩衝區不支援 **IMF2DBuffer**，則 **IMFMediaBuffer：： Lock** 可能不會產生複本。

計算媒體類型的最小 stride，如下所示：

-   最小 stride 可能儲存在 [**MF \_ MT \_ 預設 \_ stride**](mf-mt-default-stride-attribute.md) 屬性中。
-   如果未設定 **MF \_ MT \_ 預設 \_ STRIDE** 屬性，請呼叫 [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) 函式來計算最常見影片格式的 STRIDE。
-   如果 [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) 函式無法辨識格式，您必須根據格式的定義來計算 stride。 在此情況下，不會有一般規則;您必須知道格式定義的詳細資料。

下列程式碼顯示如何取得最常見影片格式的預設 stride。


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



視您的應用程式而定，您可能會事先知道指定的媒體緩衝區是否支援 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (例如，如果您已建立緩衝區) 。 否則，您必須準備好使用兩個緩衝區介面中的任一個。

下列範例顯示的 helper 類別會隱藏部分詳細資料。 此類別具有 LockBuffer 方法，可呼叫 [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 或 [**鎖定**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) ，並將指標傳回至第一個資料列的開頭。  (此行為符合 **Lock2D** 方法。 ) LockBuffer 方法會採用預設 stride 做為輸入參數，並傳回實際的 stride 作為輸出參數。


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[影像 Stride](image-stride.md)
</dt> <dt>

[媒體緩衝區](media-buffers.md)
</dt> </dl>

 

 



