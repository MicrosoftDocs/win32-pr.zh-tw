---
description: 指定串流音訊轉譯器的音訊串流類別 (SAR) 。
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971709"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 資料流程 \_ 類別目錄屬性

指定 [串流音訊](streaming-audio-renderer.md) 轉譯器的音訊串流類別 (SAR) 。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

您可以使用這個屬性來設定音訊轉譯器。 使用方式取決於您所呼叫用來建立音訊轉譯器的函式。



| 函式                                                               | 如何設定屬性                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | 使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)指標。                                                                                          |
| [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | 使用 *ppActivate* 參數中所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標。 呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。 |



 

屬性的值是 [**音訊 \_ 串流 \_ 類別**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) 列舉的成員。 當多個應用程式同時播放音訊時，音訊服務會使用串流類別來判斷音訊原則。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
