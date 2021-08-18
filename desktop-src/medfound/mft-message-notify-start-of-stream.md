---
description: 通知媒體基礎轉換 (MFT) 第一個範例即將處理。
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: 'MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973027"
---
# <a name="mft_message_notify_start_of_stream"></a>MFT \_ 訊息 \_ 通知 \_ 開始 \_ \_ 資料流程

通知媒體基礎轉換 (MFT) 第一個範例即將處理。

## <a name="message-parameter"></a>Message 參數

無。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

針對同步 MFTs，您可以選擇是否要傳送此訊息。

針對非同步 MFTs，用戶端必須傳送此訊息。

### <a name="implementation"></a>實作

不需要同步的 MFT 來回應訊息。

非同步 MFT 必須依照 [非同步 MFTs](asynchronous-mfts.md)中的說明，執行這則訊息。

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

 

 




