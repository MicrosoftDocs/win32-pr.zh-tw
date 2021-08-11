---
description: 設定可在記錄接收音訊路徑中緩衝處理之已處理樣本的最大數目。
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: 'MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b4478ebecfc873c612e8deb0106cba5462e77cd56d5d818b03d74e88679c8b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245036"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 音訊 \_ 最大 \_ 處理 \_ 樣本屬性

設定可在記錄接收音訊路徑中緩衝處理之已處理樣本的最大數目。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

若要在「捕獲引擎」上設定此屬性，請在呼叫 [**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)時，將它加入至 *pAttributes* 參數。

這個屬性的最大值是100。

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

 

 




