---
description: 當媒體接收變成無效時引發。
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: 'MESinkInvalidated 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191522"
---
# <a name="mesinkinvalidated-event"></a>MESinkInvalidated 事件

當媒體接收變成無效時引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                    | 描述                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**MF \_ 事件 \_ 輸出 \_ 節點**](mf-event-output-node-attribute.md)<br/> | 識別此媒體接收器的拓撲節點。<br/> <br/> |



## <a name="remarks"></a>備註

如果媒體會話接收到來自媒體接收器的下列任何事件，就會引發這個事件：

-   [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)

-   [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)

-   [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)

-   [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)

-   [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)

媒體接收器也可以引發這個事件，在這種情況下，媒體會話會設定事件的 [**MF \_ 事件 \_ 輸出 \_ 節點**](mf-event-output-node-attribute.md) 屬性，並將事件轉送到應用程式。

如果應用程式收到此事件，則必須重新建立媒體接收器，然後將拓撲重新排入佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




