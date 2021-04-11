---
description: 呈現時間與媒體來源時間戳記之間的位移。
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: 'MF_EVENT_PRESENTATION_TIME_OFFSET 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848211"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移屬性

呈現時間與媒體來源時間戳記之間的位移。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

位移的計算方式如下： offset = presentation time − source time。 這個屬性會搭配下列事件使用：

-   [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)
-   [MESessionStarted](mesessionstarted.md)

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
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

 

 




