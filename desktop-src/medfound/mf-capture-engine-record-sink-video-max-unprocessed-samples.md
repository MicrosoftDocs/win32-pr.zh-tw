---
description: 設定可在記錄接收影片路徑中緩衝處理的未處理樣本數上限。
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: 'MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f776dd795103fccf81da4c739b767131a03bf83245c3c79e724274dcb52dc0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956818"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>MF \_ CAPTURE \_ ENGINE \_ 記錄 \_ 接收 \_ 影片的 \_ 最大未處理 \_ \_ 樣本屬性

設定可在記錄接收影片路徑中緩衝處理的未處理樣本數上限。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

若要在「捕獲引擎」上設定此屬性，請在呼叫 [**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)時，將它加入至 *pAttributes* 參數。

這個屬性的最大值為17。

一旦記錄已緩衝處理的樣本數目上限（由 MF \_ 捕捉 \_ 引擎 \_ 記錄接收影片的最大未處理範例所指定） \_ \_ \_ \_ \_ ，則會卸載範例以捨棄畫面播放速率。

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

 

 




