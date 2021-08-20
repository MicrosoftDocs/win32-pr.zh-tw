---
description: 當下游格式變成失效且必須重新協商時，由資料流程接收器傳送。
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: 'MEStreamSinkFormatInvalidated 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04442aa9c00b5ab0099306007efaea967d2baced35c186af78e7b5d79854fce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061313"
---
# <a name="mestreamsinkformatinvalidated-event"></a>MEStreamSinkFormatInvalidated 事件

當下游格式變成失效且必須重新協商時，由資料流程接收器傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

若資料已排入目前播放位置之前的接收，則應該重新傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                                           |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




