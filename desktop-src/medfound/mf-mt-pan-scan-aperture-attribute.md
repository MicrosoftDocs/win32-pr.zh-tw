---
description: 定義平移/掃描光圈，也就是要在移動 \# 流覽/掃描模式中顯示的 4&215; 3 區域的影片。
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: 'MF_MT_PAN_SCAN_APERTURE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996616"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>MF \_ MT \_ 平移 \_ 掃描 \_ 光圈屬性

定義平移/掃描光圈，也就是應該以移動流覽/掃描模式顯示的影片4×3區域。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

屬性值是 [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) 結構。

這個屬性是用來將寬螢幕影片裁剪為4:3 的外觀比例。 移動流覽/掃描光圈只適用于移動流覽/掃描模式，其可透過將 [ [**MF \_ MT \_ 掃視 \_ 掃描 \_ 已啟用**](mf-mt-pan-scan-enabled-attribute.md) ] 屬性設定為 [ **TRUE**] 來啟用。

如果未啟用 [移動流覽]/[掃描] 模式，請使用 [顯示光圈] （由 [ [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) ] 屬性指定）。

如果未設定此屬性，則會假設平移/掃描光圈是整個影片畫面。

這個屬性的 GUID 常數是從 mfuuid 匯出。

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

[媒體類型屬性](media-type-attributes.md)
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

[**MF \_ MT \_ 幾何 \_ 光圈**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_已啟用 MF MT \_ PAN \_ 掃描 \_**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




