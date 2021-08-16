---
description: 通知媒體基礎轉換 (MFT) 輸入資料流程已結束。
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: 'MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951337fb91a26f1498b2aa82d42754fb2954ab649b4a021d37d42047be331ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872158"
---
# <a name="mft_message_notify_end_of_stream"></a>MFT \_ 訊息 \_ 通知 \_ 結束 \_ \_ 資料流程

通知媒體基礎轉換 (MFT) 輸入資料流程已結束。

## <a name="message-parameter"></a>Message 參數

*UlParam* 參數包含輸入資料流程的識別碼，指定為 **DWORD** 值。 在64位應用程式中，將此值放在 **ULONG \_ PTR** 的較低32位。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

用戶端不需要傳送此訊息。

資料流程結束後，用戶端可以再次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，以傳送該資料流程的新資料。 如果是的話，用戶端必須在資料流程結束後的第一個輸入範例中，將不中斷屬性 (MFSampleExtension 不中斷屬性) 。 [**\_**](mfsampleextension-discontinuity-attribute.md)  (用戶端應該一律在資料流程結束後的第一個新範例上設定此屬性，不論用戶端是否傳送了 **訊息 \_ 通知的訊息 \_ 通知 \_ 結尾 \_ \_** 。 如需處理不連續的詳細資訊，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。 ) 

針對每個輸入資料流程傳送此訊息之後，用戶端通常會傳送 **MFT \_ 訊息 \_ 命令 \_ 清空** 命令，然後收集剩餘的輸出。 不過，用戶端不需要清空 MFT。 如果用戶端未清空 MFT，則在下次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)時，MFT 通常會捨棄任何未處理的資料（當偵測到資料流程不連續時）。 或者，用戶端可能會在呼叫 **ProcessInput** 之前排清 MFT。

此訊息不會移除輸入資料流程或重設媒體類型。

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

 

 




