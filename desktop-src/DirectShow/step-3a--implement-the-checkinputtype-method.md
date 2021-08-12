---
description: 步驟3A。
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: 步驟3A。 執行 CheckInputType 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692175e0def453f86b618a355044e4a117a4343fed56f029704091134e8bc31f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652138"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>步驟3A。 執行 CheckInputType 方法

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3a。

當上游篩選準則向轉換篩選器提出媒體類型時，就會呼叫 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法。 這個方法會採用 [**CMediaType**](cmediatype.md) 物件的指標，這是 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的精簡型包裝函式。 在這個方法中，您應該檢查 **AM \_ 媒體 \_ 類型** 結構的每個相關欄位，包括格式區塊中的欄位。 您可以使用 **CMediaType** 中定義的存取子方法，或直接參考結構成員。 如果有任何欄位無效，則傳回 \_ \_ \_ 不接受的 VFW E 類型 \_ 。 如果整個媒體類型都有效，請返回 \_ [確定]。

例如，在 RLE 編碼器篩選器中，輸入類型必須是8位或4位未壓縮的 RGB 影片。 由於篩選準則必須將它們轉換成較低的位深度，而 DirectShow 已經為該用途提供[色彩空間轉換器](color-space-converter-filter.md)篩選，因此不支援其他輸入格式，例如16或24位 RGB。 下列範例假設編碼器支援8位的影片，但不支援4位的影片：


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



在此範例中，方法會先檢查主要類型和子類型。 然後，它會檢查格式類型，以確保格式區塊是 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。 篩選也可以支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)，但在此情況下，將沒有真正的好處。 **VIDEOINFOHEADER2** 結構新增了交錯和非正方形圖元的支援，這些圖元不太可能與8位的影片相關。

如果格式類型正確，此範例會檢查 **VIDEOINFOHEADER** 結構的 **biBitCount** 和 **biCompression** 成員，以確認格式為8位未壓縮的 RGB。 如這個範例所示，您必須強制轉換


```C++
pbFormat
```



以格式類型為基礎的正確結構指標。 在轉換指標之前，請務必先檢查格式類型 GUID (**formattype**) 和格式區塊 (**cbFormat**) 的大小。

此範例也會確認調色板專案的數目與位深度相容，而且格式區塊夠大，足以容納調色板專案。 如果上述所有資訊都正確無誤，則方法會傳回 S \_ OK。

下一 [步：步驟3b：執行 GetMediaType 方法](step-3b--implement-the-getmediatype-method.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



