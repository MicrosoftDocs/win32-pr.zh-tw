---
description: 指定啟用物件，為增強型影片轉譯器 (EVR) 媒體接收器建立自訂的視頻混音器。
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_MIXER_ACTI加值稅E 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1966efe66efaba56c0206a9f6fac59aba30a1aea9d47100c4ce19a30af96a863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877295"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 啟動屬性

指定啟用物件，為增強型影片轉譯器 (EVR) 媒體接收器建立自訂的視頻混音器。

## <a name="data-type"></a>資料類型

**IUnknown\***

## <a name="remarks"></a>備註

如果您是透過啟用物件建立 EVR，您可以使用此屬性在 EVR 上設定自訂的視頻混音器。 使用此屬性，如下所示：

1.  呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 函數，以建立 EVR 的啟用物件。 函數會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。
2.  藉由呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)，在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定此屬性。 屬性（attribute）的值（attribute）是呼叫端所執行之啟用物件的指標。 呼叫端的啟用物件必須公開 **IMFActivate** 介面。

如果設定此屬性，EVR 會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立自訂的視頻混音器。 影片混音器必須公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[增強的影片轉譯器屬性](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[啟用物件](activation-objects.md)
</dt> </dl>

 

 




