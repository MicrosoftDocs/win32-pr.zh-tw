---
description: 當媒體來源啟動新的資料流程時引發。
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: 'MENewStream 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980760"
---
# <a name="menewstream-event"></a>MENewStream 事件

當媒體來源啟動新的資料流程時引發。

在媒體來源上呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法時，媒體來源會為每個選取的資料流程傳送一個事件：

-   如果未在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 MENewStream 事件，或這是在此媒體來源上 **開始** 的第一次呼叫。

-   如果已在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 [MEUpdatedStream](meupdatedstream.md)事件。

未選取的資料流程不會傳送任何事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 包含資料流程 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 介面的指標。<br/> <br/> |



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

 

 




