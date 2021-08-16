---
description: 指定 h.264 視頻串流支援的同步處理框架類型。
ms.assetid: A2E548F1-A5FA-4110-AD07-46BE9D7DC4A5
title: 'MF_MT_H264_SUPPORTED_SYNC_FRAME_TYPES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f6b6d00b3914ebcf55952baf372c139d43a02689605f800628df58b2d71395b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113738"
---
# <a name="mf_mt_h264_supported_sync_frame_types-attribute"></a>MF \_ MT \_ H264 \_ 支援的 \_ 同步處理 \_ 畫面 \_ 類型屬性

指定 h.264 視頻串流支援的同步處理框架類型。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。 值會對應至 UVC 1.5 h.264 視頻格式描述項中的 **bmSupportedSyncFrameTypes** 欄位。

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




