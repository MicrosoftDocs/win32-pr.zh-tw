---
description: 指定媒體來源的目前特性。
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: 'MF_EVENT_SOURCE_CHARACTERISTICS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974071"
---
# <a name="mf_event_source_characteristics-attribute"></a>MF \_ 事件 \_ 來源 \_ 特性屬性

指定媒體來源的目前特性。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)列舉中的位 **or** of 旗標。

這個屬性會與 [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) 事件一起使用。

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

 

 




