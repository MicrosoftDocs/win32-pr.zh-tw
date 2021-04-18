---
description: 步驟3B。
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: 步驟3B。 執行 GetMediaType 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514328"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>步驟3B。 執行 GetMediaType 方法

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3b。

> [!Note]  
> 衍生自 **CTransInPlaceFilter** 的篩選不需要此步驟。

 

[**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md)方法會傳回其中一個篩選器慣用的輸出類型，並依索引編號參考。 除非已經連接篩選的輸入釘選，否則永遠不會呼叫這個方法。 因此，您可以從上游連接使用媒體類型來判斷慣用的輸出類型。

編碼器通常會提供代表目標格式的單一慣用類型。 這些解碼器通常支援一系列的輸出格式，並以遞減品質或效率的順序提供這些格式。 例如，清單可能是 UYVY、Y211、RGB-24、RGB-565、RGB-555 和 RGB-8 （依該順序）。 效果篩選可能需要輸出格式和輸入格式之間完全相符。

下列範例會傳回單一輸出型別，這個輸出型別是藉由修改輸入類型來指定 RLE8 壓縮來建立的：


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



在此範例中，此方法會呼叫 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) ，以從輸入的 pin 取得輸入類型。 然後，它會變更一些欄位以表示壓縮格式，如下所示：

-   它會指派新的子類型 GUID，此 GUID 是使用 [**FOURCCMap**](fourccmap.md) 類別，從 FOURCC 程式碼 ' MRLE ' 所建立。
-   它會呼叫 [**CMediaType：： SetVariableSize**](cmediatype-setvariablesize.md) 方法，它會將 **bFixedSizeSamples** 旗標設為 **FALSE** ，並將 **lSampleSize** 成員設定為零，以指出可變大小的範例。
-   它會呼叫 [**CMediaType：： SetTemporalCompression**](cmediatype-settemporalcompression.md) 方法，其值 **為 FALSE**，表示每個畫面格都是主要畫面格。  (此欄位僅供參考，所以您可以放心地忽略它。 ) 
-   它會將 **biCompression** 欄位設定為 BI \_ RLE8。
-   它會將 **biSizeImage** 欄位設定為影像大小。

下一 [步：步驟3c：執行 CheckTransform 方法](step-3c--implement-the-checktransform-method.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



