---
description: 影片媒體類型的畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: 'MF_MT_FRAME_RATE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb49da7667286c17bfa500a8a90a9f7083e786483120e40ba2d635710668a4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113808"
---
# <a name="mf_mt_frame_rate-attribute"></a>MF \_ MT \_ 幀 \_ 速率屬性

影片媒體類型的畫面播放速率（以每秒畫面格數為單位）。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

畫面播放速率以比例表示。 屬性值的上方32位包含分子，而較低的32位則包含分母。 例如，如果畫面播放速率是每秒30個畫面格 (fps) ，則比率為30/1。 如果畫面播放速率是 29.97 fps，則比率為 30000/1001。

若要設定此值，請使用 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) 函數。 若要取得此值，請使用 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) 函數。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例

下列範例會設定影片媒體類型的畫面播放速率。


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



下列範例會從影片媒體類型取得畫面播放速率。


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




