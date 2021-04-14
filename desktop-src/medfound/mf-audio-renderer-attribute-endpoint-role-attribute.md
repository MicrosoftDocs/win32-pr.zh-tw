---
description: 指定音訊轉譯器的音訊端點角色。
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944590"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 端點 \_ 角色屬性

指定音訊轉譯器的音訊端點角色。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

您可以使用這個屬性來設定音訊轉譯器。 使用方式取決於您呼叫來建立音訊轉譯器的函式：

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。 呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。

音訊端點裝置是一種硬體裝置，位於音訊資料路徑的一端，例如耳機或喇叭。

如果設定此屬性，音訊轉譯器會針對指定的角色使用預設音訊裝置。 這個屬性的值是 **ERole** 列舉的成員，定義于標頭檔 mmdeviceapi 中。 如需詳細資訊，請參閱核心音訊 API 檔。 如果未設定此屬性，音訊轉譯器會使用預設端點裝置。

如果設定這個屬性，請勿設定 [ [**MF 音訊轉譯 \_ 器 \_ \_ 屬性 \_ 端點 \_ 識別碼**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ] 屬性。 如果同時設定了這兩個屬性，則在建立音訊轉譯器時將會發生失敗。

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

[音訊轉譯器屬性](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 




