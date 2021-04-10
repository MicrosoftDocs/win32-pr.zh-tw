---
description: 定義影片媒體類型的幾何光圈。
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: 'MF_MT_GEOMETRIC_APERTURE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943782"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>MF \_ MT \_ 幾何 \_ 光圈屬性

定義影片媒體類型的幾何光圈。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) 結構。

圖片外觀比例的計算相對於幾何光圈，使用下列公式：圖片外觀比例 = (幾何光圈寬度/幾何光圈高度) ×圖元外觀比例。

如果未設定此屬性，則會假設幾何光圈是整個影片畫面。 只有當媒體類型描述具有定義之作用中區域的影片標準時，才應該設定這個屬性。

例如，在 NTSC 電視中，影片畫面是720×480，其使用區域為704×480和10:11 圖元外觀比例。 產生的圖片具有 (704/480) × (10/11) = 4:3 的外觀比例。

> [!Note]  
> [增強型影片](enhanced-video-renderer.md)轉譯器的預設展示器 (EVR) 顯示影片的幾何光圈（如有指定）。

 

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[圖片外觀比例](picture-aspect-ratio.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




