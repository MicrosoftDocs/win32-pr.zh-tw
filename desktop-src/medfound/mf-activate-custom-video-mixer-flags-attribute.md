---
description: 指定如何建立增強型影片轉譯器的自訂混音器 (EVR) 。
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_MIXER_FLAGS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd536328bf454a70b35376aca3b7c6a0cea9ec7e0e2408a05cd6d0e8da0854ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957088"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ 旗標屬性

指定如何建立增強型影片轉譯器的自訂混音器 (EVR) 。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

您可以在從 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函數取得的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定這個屬性。 這個屬性的值是下列值的位 **or** 。



| 值                                      | 描述                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ 啟用 \_ 自訂 \_ 混音器 \_ ALLOWFAIL** | 如果 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法無法建立應用程式的自訂混音器，則會改為使用預設的 EVR 混音器。 根據預設，如果 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 物件嘗試建立自訂混音器時失敗， **ActivateObject** 方法就會失敗。 |



 

應用程式可以使用 [**MF \_ 啟用 \_ 自訂 \_ 視頻 \_ 混音器 \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) 屬性來指定 EVR 的自訂混音器。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[啟用物件](activation-objects.md)
</dt> </dl>

 

 




