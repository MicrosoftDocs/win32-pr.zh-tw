---
description: 指定目前區段拓撲是否為空白。
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: 'MF_EVENT_SOURCE_FAKE_START 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b026811330443a3fb5e7c9671a7f6a3de8580985b6be4c6ba149a2d4dc196325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973767"
---
# <a name="mf_event_source_fake_start-attribute"></a>MF \_ 事件 \_ 來源 \_ 假 \_ 開始屬性

指定目前區段拓撲是否為空白。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性會與 [MESourceStarted](mesourcestarted.md) 事件一起使用。

如果目前區段拓撲是空的，sequencer 來源會將這個屬性設定為 **TRUE** 。 如果此屬性為 **TRUE**，表示尚未開始播放。 這個屬性的預設值為 **FALSE**。

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

 

 




