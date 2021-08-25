---
description: 當資料流程的輸出原則變更時，由管線元件引發。 此事件僅適用于受保護的內容。
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: 'MEPolicyChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac87d3dae63b20d19c91f0fdef5471060753152901d9096b1be315cd76e9974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957408"
---
# <a name="mepolicychanged-event"></a>MEPolicyChanged 事件

當資料流程的輸出原則變更時，由管線元件引發。 此事件僅適用于受保護的內容。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | 描述                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 資料流程之新原則的 [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) 介面指標。<br/> <br/> |



## <a name="remarks"></a>備註

所有信任的輸出都必須處理這個事件。 媒體基礎轉換 (MFTs) 透過 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) 方法接收此事件。 媒體接收器會透過 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 方法收到此事件。

受信任的輸出必須套用新的原則，或傳回不受支援的錯誤碼 MF \_ E \_ 原則 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




