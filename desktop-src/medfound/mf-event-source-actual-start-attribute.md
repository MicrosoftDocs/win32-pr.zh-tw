---
description: 包含媒體來源從其目前位置重新開機的開始時間。
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: 'MF_EVENT_SOURCE_ACTUAL_START 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ce39e8a9f90ad0cd7f0cbd590b32719ab10dbd8e498c396e86772ce333e94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104834"
---
# <a name="mf_event_source_actual_start-attribute"></a>MF \_ 事件 \_ 來源 \_ 實際 \_ 開始屬性

包含媒體來源從其目前位置重新開機的開始時間。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **LONGLONG** 值。

## <a name="remarks"></a>備註

這個屬性會與 [MESourceStarted](mesourcestarted.md) 事件一起使用。 當事件資料為空白 (**VT \_ 空白**) （表示媒體來源從目前的播放位置開始）時，屬性就會相關。 在此情況下， **MF \_ 事件 \_ 來源 \_ 實際 \_ 開始** 屬性會指定實際的開始時間。 如果事件資料是 **VT \_ 空** 的，而且未設定此屬性，則開始時間會假設為零。

當 [MESourceStarted](mesourcestarted.md) 的事件資料包含開始時間 (**VT \_ I8**) 時，不應設定這個屬性。

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

 

 




