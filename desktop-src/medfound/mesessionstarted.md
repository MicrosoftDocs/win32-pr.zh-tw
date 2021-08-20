---
description: 當 IMFMediaSession：： Start 方法以非同步方式完成時引發。
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: 'MESessionStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cf1b461017ce9cdcbaeb57e7c327a7b12b80a63c181dbe1f50f223977c5095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061718"
---
# <a name="mesessionstarted-event"></a>MESessionStarted 事件

當 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法以非同步方式完成時引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                               | 描述                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**](mf-event-presentation-time-offset-attribute.md)<br/> | 呈現時間與媒體來源時間戳記之間的位移。<br/> <br/> |



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

 

 




