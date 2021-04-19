---
description: 要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: 'MFT_MESSAGE_COMMAND_DRAIN (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992440"
---
# <a name="mft_message_command_drain"></a>MFT \_ 訊息 \_ 命令 \_ 清空

要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。

## <a name="message-parameter"></a>Message 參數

無。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

傳送此訊息之後，指定的輸入資料流程不接受輸入，直到 MFT 處理來自先前呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)的所有資料為止。

在同步 MFTs 與非同步 MFTs 之間，清空程式會稍有不同：

**同步 MFTs**

1.  用戶端傳送此訊息之後，它會在迴圈中呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ，直到 **ProcessOutput** 傳回錯誤碼 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入**。
2.  只要 MFT 仍有要處理的資料， [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 的後續呼叫就會失敗。 MFT 會繼續產生輸出，直到它使用所有儲存的資料為止。 MFT 會捨棄無法處理為完整輸出範例的任何資料。  (例如，它應該卸載部分影片框架。 ) 

**非同步 MFTs**

1.  MFT 會繼續傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件，直到它沒有其他要處理的資料為止。 它不會在這段時間內傳送 [METransformNeedInput](metransformneedinput.md) 事件。
2.  在 MFT 傳送最後一個 [METransformHaveOutput](metransformhaveoutput.md) 事件之後，它會傳送 [METransformDrainComplete](metransformdraincomplete.md) 事件。
3.  完成清空之後，除非從用戶端接收到來自用戶端 [**\_ \_ \_ \_ 的 \_ 訊息訊息通知**](mft-message-notify-start-of-stream.md)，否則 mft 不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。

在用戶端清空 MFT 之後，用戶端就可以傳送更多輸入資料。 清空作業之後的第一個範例必須具有不連續屬性 ([**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) 不連續屬性) 。

> [!Note]  
> 本檔的先前版本指出 *ulParam* 事件參數是 [**\_ MFT \_ 清空 \_ 類型**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type)列舉的成員。 不正確。 *UlParam* 包含資料流程識別碼。

 

### <a name="implementation"></a>實作

非同步 MFT 在 [METransformDrainComplete](metransformdraincomplete.md) 之後必須一律傳回。

如果下列條件成立，同步的 MFT 可以忽略此訊息並傳回 S \_ OK：

-   此 MFT 一次絕不會儲存一個以上的輸入範例。
-   每個輸入範例都會產生單一輸出範例。

否則，同步的 MFT 必須執行此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




