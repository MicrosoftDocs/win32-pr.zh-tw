---
description: 由媒體來源引發，該媒體來源透過 IMFMediaSourceTopologyProvider 介面（例如 sequencer 來源）提供拓撲。 來源會在有新的簡報時引發事件。 媒體會話將此事件轉送到應用程式。
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: 'MENewPresentation 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191912"
---
# <a name="menewpresentation-event"></a>MENewPresentation 事件

由媒體來源引發，該媒體來源透過 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 介面（例如 sequencer 來源）提供拓撲。 來源會在有新的簡報時引發事件。 媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 新簡報之呈現描述項的 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面指標。<br/> <br/> |



## <a name="remarks"></a>備註

應用程式可以藉由呼叫媒體來源上的 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) ，取得對應至展示描述項的拓撲。 然後，應用程式可以藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上將新的拓撲排入佇列。

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

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 




