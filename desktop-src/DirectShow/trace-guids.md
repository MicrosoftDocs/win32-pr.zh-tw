---
description: 下列 Guid 用於 DirectShow 中的事件追蹤。
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: '追蹤 Guid (PerfStruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 89465996c57e1f1f97f2c101c8dfee99a00219f992a4e68681f76465d21bef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951547"
---
# <a name="trace-guids"></a>追蹤 Guid

下列 Guid 用於 DirectShow 中的事件追蹤。



| GUID                                                                                                                                                                   | Description                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <dt>**GUID \_ AUDIOBREAK**</dt> </dl>    | 音訊中斷事件。 此類型的事件會針對事件資料使用 [**PERFINFO \_ DSHOW \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) 結構。<br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <dt>**GUID \_ DSHOW \_ CTL**</dt> </dl>      | DirectShow 事件提供者。<br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <dt>**GUID \_ STREAMTRACE**</dt> </dl> | 一般串流事件。 此類型的事件會針對事件資料使用 [**PERFINFO \_ DSHOW \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) 結構。<br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <dt>**GUID \_ VIDEOREND**</dt> </dl>       | 影片呈現事件。 此類型的事件會針對事件資料使用 [**PERFINFO \_ DSHOW \_ AVREND**](perfinfo-dshow-avrend.md) 結構。<br/>             |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PerfStruct。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 中的事件追蹤](event-tracing-in-directshow.md)
</dt> </dl>

 

 




