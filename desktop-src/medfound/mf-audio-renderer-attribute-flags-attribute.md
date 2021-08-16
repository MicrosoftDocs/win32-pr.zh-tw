---
description: 包含用來設定音訊轉譯器的旗標。
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1146ce4e363dca63819badd96abcd9d9e91051419df3b5007c237a002bb39d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105004"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 旗標屬性

包含用來設定音訊轉譯器的旗標。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是下列旗標的位 **or** 。



| 值                                                   | 描述                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 旗標 \_ CROSSPROCESS** | 音訊轉譯器使用跨進程音訊會話。 這個旗標可讓多個進程中的音訊轉譯器共用相同的音訊會話，以及相關聯的磁片區和原則控制項。<br/> 如果未設定此旗標，其他進程中的音訊轉譯器無法共用音訊會話。<br/> |
| **MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 旗標 \_ NOPERSIST**    | Windows 音訊會話 API (WASAPI) 將不會保存此音訊會話的屬性，例如會話量。<br/> 如果未設定此旗標，WASAPI 會保存音訊會話屬性。<br/>                                                                                                       |



 

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 




