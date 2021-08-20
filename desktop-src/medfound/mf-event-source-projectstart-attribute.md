---
description: 指定區段拓撲的開始時間。
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: 'MF_EVENT_SOURCE_PROJECTSTART 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e3d386b90a45d1ba06d0d0c1641b97544ca1d2422dd1d2d6f7762f93cf4ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060693"
---
# <a name="mf_event_source_projectstart-attribute"></a>MF \_ 事件 \_ 來源 \_ PROJECTSTART 屬性

指定區段拓撲的開始時間。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **LONGLONG** 值。

## <a name="remarks"></a>備註

這個屬性會與 [MESourceStarted](mesourcestarted.md) 事件一起使用。 當目前區段拓撲具有 [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 屬性時，sequencer 來源會設定這個屬性。 這兩個屬性具有相同的值。

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

 

 




