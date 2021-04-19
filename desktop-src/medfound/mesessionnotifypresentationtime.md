---
description: 當新的簡報開始時，由媒體會話引發。 此事件表示簡報開始的時間，以及呈現時間與來源時間之間的位移。
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: 'MESessionNotifyPresentationTime 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993041"
---
# <a name="mesessionnotifypresentationtime-event"></a>MESessionNotifyPresentationTime 事件

當新的簡報開始時，由媒體會話引發。 此事件表示簡報開始的時間，以及呈現時間與來源時間之間的位移。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                                                   | 描述                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ 開始 \_ 簡報 \_ 時間**](mf-event-start-presentation-time-attribute.md)<br/>                       | 簡報的開始時間。<br/> <br/>                                                      |
| [**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**](mf-event-presentation-time-offset-attribute.md)<br/>                     | 呈現時間與媒體來源時間戳記之間的位移。<br/> <br/>                 |
| [**MF \_ 事件 \_ \_ \_ \_ 在輸出時開始展示時間 \_**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | 當媒體接收器轉譯新拓撲的第一個範例時的呈現時間。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




