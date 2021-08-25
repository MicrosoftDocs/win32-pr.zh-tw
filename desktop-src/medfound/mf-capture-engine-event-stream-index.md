---
description: 識別哪個資料流程產生了捕捉事件。
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: 'MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7e8f5f78c6364c27cc4efc2296e7fd1b79a923b0a10f4dd0242d8157882a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060808"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a>MF \_ CAPTURE \_ ENGINE \_ 事件 \_ 資料流程 \_ 索引屬性

識別哪個資料流程產生了捕捉事件。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

## <a name="remarks"></a>備註

這個屬性會出現在 capture 引擎的某些事件上。 若要取得這個屬性，請在事件物件上呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 。 事件物件會透過 [**IMFCaptureEngineOnEventCallback：： OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) 方法傳遞給應用程式。

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

[**IMFCaptureEngineOnEventCallback：： OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




