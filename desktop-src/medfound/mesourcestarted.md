---
description: 媒體來源啟動但未搜尋時引發。
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: 'MESourceStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512836"
---
# <a name="mesourcestarted-event"></a>MESourceStarted 事件

媒體來源啟動但未搜尋時引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。 開始時間是從目前的位置開始。<br/> <br/>                            |
| VT \_ I8<br/>    | 相對於樣本上時間戳記的開始時間，以 100-毫微秒單位為單位。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                     | 描述                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**](mf-event-source-actual-start-attribute.md)<br/> | 開始時間。 媒體來源會設定這個屬性（如果它目前的位置重新開機的話）。<br/> <br/>                     |
| [**MF \_ 事件 \_ 來源 \_ 假 \_ 開始**](mf-event-source-fake-start-attribute.md)<br/>     | 指定目前區段拓撲是否為空白。 Sequencer 來源會設定這個屬性。<br/> <br/>             |
| [**MF \_ 事件 \_ 來源 \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)<br/>  | 區段的開始時間，相對於簡報的開始時間。 Sequencer 來源會設定這個屬性。<br/> <br/> |



## <a name="remarks"></a>備註

當媒體來源從停止狀態開始，或從來源中相同位置的暫停狀態開始時，就會引發此事件。 如果 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法傳回 S OK，就會引發事件 \_ 。

如果媒體來源從目前位置開始，且來源的先前狀態為 [執行中] 或 [已暫停]，則事件資料可以空白 (VT \_ 空白) 。 如果事件資料是 VT \_ 空白，則媒體來源可能會以實際的開始時間設定 [**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**](mf-event-source-actual-start-attribute.md) 屬性。

如果媒體來源從新位置開始，或來源的先前狀態為 [已停止]，則事件資料必須是 (VT I8) 的開始時間 \_ 。

如果 [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法導致搜尋，媒體來源會傳送 [MESourceSeeked](mesourceseeked.md) 事件，而不是 MESourceStarted。

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

 

 




