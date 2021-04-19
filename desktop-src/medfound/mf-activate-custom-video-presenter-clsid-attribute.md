---
description: 增強影片轉譯器 (EVR) 媒體接收器的自訂影片呈現者 CLSID。
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_CLSID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981431"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ CLSID 屬性

增強影片轉譯器 (EVR) 媒體接收器的自訂影片呈現者 CLSID。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

如果您是透過啟用物件建立 EVR，您可以使用這個屬性，在 EVR 上設定自訂的影片展示者。 使用此屬性，如下所示：

1.  呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 函數，以建立 EVR 的啟用物件。 函數會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。

2.  藉由呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)，在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定此屬性。 屬性的值是應用程式自訂影片展示者的 CLSID。

如果設定此屬性，EVR 就會使用指定的 CLSID 來呼叫 **CoCreateInstance** ，以建立自訂的影片展示者。 影片展示者必須公開 [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) 介面。 系統會將簡報者建立為同進程 COM 伺服器。

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

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[啟用物件](activation-objects.md)
</dt> <dt>

[如何撰寫 EVR 展示者](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




