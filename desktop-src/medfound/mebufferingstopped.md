---
description: 表示媒體來源已停止緩衝處理資料。
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: 'MEBufferingStopped 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e953ae5d7a79c04c33f4d0b4f9c87faa1e5798ed95d2d3bae29dbd0fab8b12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878078"
---
# <a name="mebufferingstopped-event"></a>MEBufferingStopped 事件

表示媒體來源已停止緩衝處理資料。

媒體來源會在傳送 [MEBufferingStarted](mebufferingstarted.md) 事件之後停止緩衝資料時傳送。

執行 [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) 介面的位元組資料流程也會傳送此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

當媒體會話收到此事件時，它會重新開機表示時鐘。 媒體會話也會將事件轉送到應用程式。

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

 

 




