---
description: 增強型影片轉譯器的自訂視頻混音器 CLSID (EVR) 媒體接收器。
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_MIXER_CLSID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318555"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ CLSID 屬性

增強型影片轉譯器的自訂視頻混音器 CLSID (EVR) 媒體接收器。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

如果您是透過啟用物件建立 EVR，您可以使用此屬性在 EVR 上設定自訂的視頻混音器。 使用此屬性，如下所示：

1.  呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 函數，以建立 EVR 的啟用物件。 函數會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。

2.  藉由呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)，在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定此屬性。 屬性的值是應用程式自訂視頻混音器的 CLSID。

如果設定此屬性，EVR 就會使用指定的 CLSID 來呼叫 **CoCreateInstance** ，以建立自訂的視頻混音器。 影片混音器必須公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面。 混音器會建立為同進程 COM 伺服器。

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
</dt> </dl>

 

 




