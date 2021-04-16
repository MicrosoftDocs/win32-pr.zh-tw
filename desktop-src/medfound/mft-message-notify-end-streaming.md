---
description: 要求媒體基礎轉換 (MFT) 至該資料流程即將結束。
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: 'MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512604"
---
# <a name="mft_message_notify_end_streaming"></a>MFT \_ 訊息 \_ 通知 \_ 結束 \_ 資料流程

要求媒體基礎轉換 (MFT) 至該資料流程即將結束。

## <a name="message-parameter"></a>Message 參數

無。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

用戶端不需要傳送此訊息，即使用戶端先前傳送的是 **MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流** 訊息也是如此。

### <a name="implementation"></a>實作

藉由釋放緩衝區和其他資源，此 MFT 可以回應此訊息。 在回應此訊息時，MFT 不會排清輸入資料或重設媒體類型。 不需要使用 MFT 來回應此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




