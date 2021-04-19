---
description: 當 IMFSequencerSource：： UpdateTopology 方法以非同步方式完成時，由 sequencer 來源引發。
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: 'MESequencerSourceTopologyUpdated 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981483"
---
# <a name="mesequencersourcetopologyupdated-event"></a>MESequencerSourceTopologyUpdated 事件

當 [**IMFSequencerSource：： UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) 方法以非同步方式完成時，由 sequencer 來源引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE            | Description                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UI4<br/> | 正在更新之拓撲的 Sequencer 元素識別碼。 應用程式會在 [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology)方法的 *dwId* 參數中指定此值。<br/> <br/> |



## <a name="remarks"></a>備註

此事件表示 sequencer 來源已更新拓撲，但並不表示拓撲已準備好可供播放。 應用程式應該等候 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件。

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

 

 




