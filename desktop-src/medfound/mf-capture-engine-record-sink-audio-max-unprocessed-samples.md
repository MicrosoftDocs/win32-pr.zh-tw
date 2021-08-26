---
description: 設定可在記錄接收音訊路徑中緩衝處理的未處理樣本數上限。
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: 'MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5f6d2a2bcd592d5a6991028af90af008a827940903084054933558ed7088c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060828"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 音訊 \_ 最大未處理 \_ \_ 樣本屬性

設定可在記錄接收音訊路徑中緩衝處理的未處理樣本數上限。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

若要在「捕獲引擎」上設定此屬性，請在呼叫 [**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)時，將它加入至 *pAttributes* 參數。

這個屬性的最大值是100。

一旦記錄已緩衝處理的樣本數目上限（由 MF \_ 捕捉 \_ 引擎 \_ 記錄接收音訊的最大未處理範例所指定） \_ \_ \_ \_ \_ ，它會卸載範例以捨棄畫面播放速率。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




