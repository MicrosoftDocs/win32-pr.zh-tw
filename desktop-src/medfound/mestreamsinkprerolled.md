---
description: 資料流程接收到足夠的向前復原資料以開始轉譯時，由資料流程接收器引發。 此事件是由支援 IMFMediaSinkPreroll 介面的媒體接收所引發。
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: 'MEStreamSinkPrerolled 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46c4c4e076651cb38318bb908df280c503c0880a256087f4192433ecdb5406a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464798"
---
# <a name="mestreamsinkprerolled-event"></a>MEStreamSinkPrerolled 事件

資料流程接收到足夠的向前復原資料以開始轉譯時，由資料流程接收器引發。 此事件是由支援 [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) 介面的媒體接收所引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> </dl>

 

 




