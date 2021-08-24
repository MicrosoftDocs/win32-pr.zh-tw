---
description: 通知媒體基礎轉換 (MFT) 資料流程即將開始。
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491f84ee2dee752cccc251187c43bd497723a64ae6601954051f2aebab34ef85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848060"
---
# <a name="mft_message_notify_begin_streaming"></a>MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流

通知媒體基礎轉換 (MFT) 資料流程即將開始。

## <a name="message-parameter"></a>Message 參數

無。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

用戶端不需要傳送此訊息。 如果用戶端傳送此訊息，則必須在設定所有在 MFT 上的媒體類型之後，以及在呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)之前這麼做。 MFT 可透過配置緩衝區或其他資源來回應。 如果用戶端未傳送此訊息，則在第一次呼叫 **ProcessInput** 時，MFT 會配置資源。 因此，傳送此訊息可減少串流開始時的初始延遲。

### <a name="implementation"></a>實作

不需要使用 MFT 來回應此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




