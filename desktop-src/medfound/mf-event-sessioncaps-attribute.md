---
description: 包含根據目前的簡報定義媒體會話功能的旗標。
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: 'MF_EVENT_SESSIONCAPS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175c81d1cc231204060a63a90ffe9e2432b73bdec35c7885dea203416995ea92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973787"
---
# <a name="mf_event_sessioncaps-attribute"></a>MF \_ 事件 \_ SESSIONCAPS 屬性

包含根據目前的簡報定義媒體會話功能的旗標。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性包含零或多個旗標的位 **or** 。 如需可能旗標的清單，請參閱 [**IMFMediaSession：： GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities)。

這個屬性會與 [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) 事件一起使用。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




