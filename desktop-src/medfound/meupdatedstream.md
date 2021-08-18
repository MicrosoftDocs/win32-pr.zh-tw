---
description: 當媒體來源重新開機或搜尋已在使用中的資料流程時引發。
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: 'MEUpdatedStream 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5746b619f885ab7648110cbe58b66b7897c839031202d811becd33e1c84991a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974017"
---
# <a name="meupdatedstream-event"></a>MEUpdatedStream 事件

當媒體來源重新開機或搜尋已在使用中的資料流程時引發。

在媒體來源上呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法時，媒體來源會為每個選取的資料流程傳送一個事件：

-   如果未在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 [MENewStream](menewstream.md)事件，或這是在此媒體來源上 **開始** 的第一次呼叫。

-   如果已在先前的 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫中選取資料流程，則來源會傳送 MEUpdatedStream 事件。

未選取的資料流程不會傳送任何事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | 描述                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 資料流程 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

在啟動資料流程的第一次呼叫 [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 時，媒體來源會傳送資料流程的 [MENewStream](menewstream.md) 事件。 在後續呼叫 **開始** 時，媒體來源會傳送 MEUpdatedStream 事件，直到取消選取資料流程為止。

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

 

 




