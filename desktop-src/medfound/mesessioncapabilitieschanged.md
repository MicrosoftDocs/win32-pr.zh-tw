---
description: 當會話功能變更時由媒體會話引發。
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: 'MESessionCapabilitiesChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97cb5168957f34cc029a982447c6d4775075ea6f9b9b250ce7b9fd7f1791d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464868"
---
# <a name="mesessioncapabilitieschanged-event"></a>MESessionCapabilitiesChanged 事件

當會話功能變更時由媒體會話引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件包含下列屬性。



| 屬性                                                                     | 描述                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ 事件 \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)              | 新的會話功能旗標。                  |
| [**MF \_ 事件 \_ SESSIONCAPS \_ 差異**](mf-event-sessioncaps-delta-attribute.md) | 指出哪些功能旗標已變更。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




