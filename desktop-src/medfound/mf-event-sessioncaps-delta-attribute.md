---
description: 包含旗標，這些旗標會根據目前的簡報，指出媒體會話中的哪些功能已變更。
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: 'MF_EVENT_SESSIONCAPS_DELTA 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714838"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>MF \_ 事件 \_ SESSIONCAPS \_ DELTA 屬性

包含旗標，這些旗標會根據目前的簡報，指出媒體會話中的哪些功能已變更。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此屬性包含一個位元遮罩，指出哪些功能旗標已變更。 如需可能旗標的清單，請參閱 [**IMFMediaSession：： GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities)。 在位元遮罩中的位會設定為1，原因如下：

-   對應的功能位已從0變更為1。
-   對應的功能位從1變更為0。
-   對應的功能位保持為1，但功能的詳細資料已變更。 例如，最大播放速率已變更。

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

 

 




