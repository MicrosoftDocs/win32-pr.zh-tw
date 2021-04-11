---
description: 指定啟用物件，此物件會為增強的影片轉譯器 (EVR) 媒體接收器，建立自訂的影片呈現者。
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_ACTI加值稅E 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318819"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a>MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ 啟用屬性

指定啟用物件，此物件會為增強的影片轉譯器 (EVR) 媒體接收器，建立自訂的影片呈現者。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

如果您是透過啟用物件建立 EVR，您可以使用這個屬性，在 EVR 上設定自訂的影片展示者。 使用此屬性，如下所示：

1.  呼叫 [_ *MFCreateVideoRendererActivate* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函式來建立 EVR 的啟用物件。 函數會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。
2.  藉由呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)，在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定此屬性。 屬性（attribute）的值（attribute）是呼叫端所執行之啟用物件的指標。 呼叫端的啟用物件必須公開 **IMFActivate** 介面。

如果設定此屬性，EVR 會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立自訂的影片展示者。 影片展示者必須公開 [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) 介面。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
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
</dt> <dt>

[如何撰寫 EVR 展示者](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




