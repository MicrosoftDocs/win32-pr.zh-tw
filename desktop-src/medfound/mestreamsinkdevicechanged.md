---
description: 由增強影片轉譯器的串流接收器引發 (EVR) 如果影片裝置變更。
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: 'MEStreamSinkDeviceChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb760a45125ae7434ff2a58d43f087d2ec3c030cb29351ea4d2113ca8fe10c0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061008"
---
# <a name="mestreamsinkdevicechanged-event"></a>MEStreamSinkDeviceChanged 事件

由增強影片轉譯器的串流接收器引發 (EVR) 如果影片裝置變更。 例如，當 EVR 收到「 [**EC \_ 顯示器」 \_ 變更**](../directshow/ec-display-changed.md) 事件時，會引發此事件。

媒體基礎管線會在裝置變更時重新提交所有失敗的範例要求，以回應此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> </dl>

 

 
