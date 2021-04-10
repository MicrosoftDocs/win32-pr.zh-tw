---
description: 當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。 當最後一個區段完成時，sequencer 來源會引發 MEEndOfPresentation 事件。
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: 'MEEndOfPresentationSegment 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848542"
---
# <a name="meendofpresentationsegment-event"></a>MEEndOfPresentationSegment 事件

當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。 當最後一個區段完成時，sequencer 來源會引發 [MEEndOfPresentation](meendofpresentation.md) 事件。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[關於 Sequencer 來源](about-the-sequencer-source.md)
</dt> <dt>

[Sequencer 來源事件](sequencer-source-events.md)
</dt> </dl>

 

 




