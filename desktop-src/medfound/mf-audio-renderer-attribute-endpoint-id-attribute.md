---
description: 指定音訊端點裝置的識別碼。
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dd99a42442342e25c748e12f8af84a03f2322b8c3dd24bb915b50b57952d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941128"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 端點 \_ 識別碼屬性

指定音訊端點裝置的識別碼。

## <a name="data-type"></a>資料類型

寬字元字串

## <a name="remarks"></a>備註

您可以使用這個屬性來設定音訊轉譯器。 使用方式取決於您呼叫來建立音訊轉譯器的函式：

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。 呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。

音訊端點裝置是一種硬體裝置，位於音訊資料路徑的一端，例如耳機或喇叭。 若要取得音訊端點識別碼，請使用下列核心音訊 Api：

-   您可以使用 [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面來列舉系統上的裝置。
-   呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 來取得裝置的識別碼。

如需詳細資訊，請參閱 [核心音訊](../coreaudio/core-audio-apis-in-windows-vista.md) API 檔。 如果未設定此屬性，音訊轉譯器會使用預設端點裝置。

如果設定這個屬性，請勿設定 [ [**MF 音訊轉譯 \_ 器 \_ 屬性 \_ ] \_ 端點 \_ 角色**](mf-audio-renderer-attribute-endpoint-role-attribute.md) 屬性。 如果同時設定了這兩個屬性，則在建立音訊轉譯器時將會發生失敗。

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

[**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
