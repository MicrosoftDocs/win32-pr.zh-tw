---
description: 由媒體來源引發，以要求新的播放速率。 應用程式應該以要求的速率呼叫 IMFRateControl：： SetRate。 如果媒體來源無法以目前的速率繼續播放，可能會引發此事件。
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: 'MESourceRateChangeRequested 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191905"
---
# <a name="mesourceratechangerequested-event"></a>MESourceRateChangeRequested 事件

由媒體來源引發，以要求新的播放速率。 應用程式應該以要求的速率呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 。 如果媒體來源無法以目前的速率繼續播放，可能會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | Description                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | 要求的新播放速率。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                    | 描述                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ DO \_ THINNING**](mf-event-do-thinning-attribute.md)<br/> | 指定媒體來源是否也要求 thinning。<br/> <br/> |



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

 

 




