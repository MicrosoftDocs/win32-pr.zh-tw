---
description: 指定影片媒體類型中色彩資訊的名義範圍。
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: 'MF_MT_VIDEO_NOMINAL_RANGE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876718"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>MF \_ MT \_ 影片 \_ 名義 \_ 範圍屬性

指定影片媒體類型中色彩資訊的名義範圍。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) 列舉的成員。

這個屬性的 GUID 常數是從 mfuuid 匯出。

**H.264/AVC 編碼器：**

在輸出媒體類型上，您 \_ \_ \_ \_ 可以使用 **MFNominalRange \_ 0 \_ 255** 和 **MFNominalRange \_ 16 \_ 235** 設定 MF MT 影片名義範圍。

H.264/AVC 編碼器應該將 **MFNominalRange \_ Unknown** 視為 **MFNominalRange \_ 16 \_ 235**。

當 MF \_ MT \_ \_ 的視頻名義 \_ 範圍設定為 **MFNominalRange \_ 48 \_ 208**、 **MFNominalRange \_ 64 \_ 127** 或 [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)未定義的任何其他值時，h.264/AVC 編碼器應拒絕輸出媒體類型。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[擴充的色彩資訊](extended-color-information.md)
</dt> </dl>

 

 




