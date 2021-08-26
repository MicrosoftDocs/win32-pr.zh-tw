---
description: 當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。 當最後一個區段完成時，sequencer 來源會引發 MEEndOfPresentation 事件。
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: 'MEEndOfPresentationSegment 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b82f646ca76dbb6cc3cd8dc9e95dbaca2c55c504af261924918dbf790411e7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013698"
---
# <a name="meendofpresentationsegment-event"></a>MEEndOfPresentationSegment 事件

當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。 當最後一個區段完成時，sequencer 來源會引發 [MEEndOfPresentation](meendofpresentation.md) 事件。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                               | 描述                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_已取消 MF 事件 \_ 來源 \_ 拓撲 \_**](mf-event-source-topology-canceled-attribute.md)<br/> | 指定 sequencer 來源是否取消此區段。<br/> <br/> |



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

[關於 Sequencer 來源](about-the-sequencer-source.md)
</dt> <dt>

[Sequencer 來源事件](sequencer-source-events.md)
</dt> </dl>

 

 




