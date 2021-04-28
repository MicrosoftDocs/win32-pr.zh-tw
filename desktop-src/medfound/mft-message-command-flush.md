---
description: MFT_MESSAGE_COMMAND_FLUSH-要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: 'MFT_MESSAGE_COMMAND_FLUSH (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092736"
---
# <a name="mft_message_command_flush"></a>MFT \_ 訊息 \_ 命令排清 \_

要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。

## <a name="message-parameter"></a>Message 參數

無。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

傳送此訊息之後，MFT 可以接受新的輸入範例。 目前的媒體類型不會失效。

### <a name="implementation"></a>實作

所有 MFTs 都必須執行這則訊息。 當它接收到此訊息時，MFT 應捨棄它所持有的任何媒體範例。

[非同步 MFTs](asynchronous-mfts.md)：從用戶端接收到來自用戶端 [**\_ \_ \_ \_ 的 \_**](mft-message-notify-start-of-stream.md)訊息訊息通知時，mft 不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。

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

 

 




