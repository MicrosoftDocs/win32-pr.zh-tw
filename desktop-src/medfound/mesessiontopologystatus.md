---
description: 當拓撲的狀態變更時，由媒體會話引發。
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: 'MESessionTopologyStatus 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943797"
---
# <a name="mesessiontopologystatus-event"></a>MESessionTopologyStatus 事件

當拓撲的狀態變更時，由媒體會話引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 拓撲的 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面指標。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                            | 描述                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MF \_ 事件 \_ 拓撲 \_ 狀態**](mf-event-topology-status-attribute.md)<br/> | 指定拓撲的新狀態。<br/> <br/> |



## <a name="remarks"></a>備註

如需從事件中抓取 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 指標的程式碼範例，請參閱 [MESessionTopologySet](mesessiontopologyset.md) 事件。

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

 

 




