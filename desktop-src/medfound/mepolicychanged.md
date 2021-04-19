---
description: 當資料流程的輸出原則變更時，由管線元件引發。 此事件僅適用于受保護的內容。
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: 'MEPolicyChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974589"
---
# <a name="mepolicychanged-event"></a>MEPolicyChanged 事件

當資料流程的輸出原則變更時，由管線元件引發。 此事件僅適用于受保護的內容。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 資料流程之新原則的 [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) 介面指標。<br/> <br/> |



## <a name="remarks"></a>備註

所有信任的輸出都必須處理這個事件。 媒體基礎轉換 (MFTs) 透過 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) 方法接收此事件。 媒體接收器會透過 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 方法收到此事件。

受信任的輸出必須套用新的原則，或傳回不受支援的錯誤碼 MF \_ E \_ 原則 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




