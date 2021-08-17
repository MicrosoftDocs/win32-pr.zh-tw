---
description: 當 IMFOutputTrustAuthority：： SetPolicy 方法以非同步方式完成時，由輸出信任授權單位引發 (OTA) 。
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: 'MEPolicySet 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064cbb92e85e300aa2c2b7db28d08b01296834413ed92e36eb5b7ce88e5486c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877555"
---
# <a name="mepolicyset-event"></a>MEPolicySet 事件

當 [**IMFOutputTrustAuthority：： SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) 方法以非同步方式完成時，由輸出信任授權單位引發 (OTA) 。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |
| VT \_ UI4<br/> | 可以透過[MF_POLICY_ID](mf-policy-id.md)屬性在[IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)上設定的識別碼。<br/> <br/> |



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

 

 




