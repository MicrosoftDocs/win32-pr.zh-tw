---
description: 當媒體來源要求新的播放速率時，這個屬性會指定來源是否也要求 thinning。 如需 thinning 的定義，請參閱關於速率控制。
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: 'MF_EVENT_DO_THINNING 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943544"
---
# <a name="mf_event_do_thinning-attribute"></a>MF \_ 事件 \_ DO \_ THINNING 屬性

當媒體來源要求新的播放速率時，這個屬性會指定來源是否也要求 thinning。 如需 thinning 的定義，請參閱 [關於速率控制](about-rate-control.md)。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性會與 [MESourceRateChangeRequested](mesourceratechangerequested.md) 事件一起使用。 如果值為 **TRUE**，表示媒體來源要求切換至 thinned 播放。

預設值為 **FALSE**。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




