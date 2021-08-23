---
description: 指定音訊轉譯器的音訊原則類別。
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5830a3deeb32ca6a3f766bad1858a803948b7e2c07a36f1f1e3222d00ba6199a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104994"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 會話 \_ 識別碼屬性

指定音訊轉譯器的音訊原則類別。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

這個屬性會將音訊轉譯器與音訊原則類別產生關聯。 每個原則類別都有自己的磁片區和原則控制。 如果未設定此屬性，新的 SAR 會聯結應用程式的預設音訊會話。 如需詳細資訊，請參閱 core 音訊 API 檔中的 [**IAudioClient：： Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) 。

您可以使用這個屬性來設定音訊轉譯器。 使用方式取決於您呼叫來建立音訊轉譯器的函式：

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。 呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。

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

[音訊轉譯器屬性](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
