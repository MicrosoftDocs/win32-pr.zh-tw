---
description: 指定增強型影片轉譯器 (EVR) 的影片混音器來源矩形。 來源矩形是混音器 blits 至目的地介面之影片框架的一部分。
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: 'VIDEO_ZOOM_RECT 屬性 (Evr) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969241"
---
# <a name="video_zoom_rect-attribute"></a>影片 \_ 縮放 \_ 矩形屬性

指定 [增強型影片](enhanced-video-renderer.md) 轉譯器 (EVR) 的影片混音器來源矩形。 來源矩形是混音器 blits 至目的地介面之影片框架的一部分。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) 結構。

來源矩形的定義是相對於正規化座標系統，其中的整個影片畫面格都會佔用座標 {0，0，1，1} 的矩形。 來源矩形必須放在影片框架內;來源矩形的座標範圍 (0 ... 1) 。

標準 EVR 展示者會在混音器上設定此屬性。 若要設定屬性，請執行下列動作：

1.  在混音器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ，以取得混音器的屬性存放區。
2.  呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) ，以在混音器上設定 **影片 \_ 縮放 \_ RECT** 屬性。 此值為 [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) 結構。

在自訂 EVR 展示者中，您可以使用這個屬性來執行 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 方法。 如需詳細資訊，請參閱 [來源和目的地矩形](how-to-write-an-evr-presenter.md)。

這個屬性的 GUID 常數是從 strmiids 匯出。

## <a name="examples"></a>範例

下列範例會設定混音器上的來源矩形。


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Evr。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[增強的影片轉譯器屬性](enhanced-video-renderer-attributes.md)
</dt> <dt>

[如何撰寫 EVR 展示者](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




