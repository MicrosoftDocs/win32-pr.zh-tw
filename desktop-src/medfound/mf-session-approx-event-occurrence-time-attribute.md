---
description: 媒體會話引發事件的大約時間。
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: 'MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6cbaa7d12cebe14b015c4d568b36b081930ef4b302797dba76fc728e92cf01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740022"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>MF \_ 會話 \_ 大約 \_ 發生事件 \_ 發生 \_ 時間屬性

媒體會話引發事件的大約時間。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **LONGLONG** 值。

## <a name="remarks"></a>備註

媒體會話中的某些事件有此屬性。 此值會提供引發事件時的大約呈現時間。

這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[事件屬性](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




