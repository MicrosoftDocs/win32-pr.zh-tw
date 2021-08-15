---
description: 標記資料流程中的點。 此訊息只適用于非同步 MFTs。
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: 'MFT_MESSAGE_COMMAND_MARKER (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc55a96ae9680b37d83ec776c66848ed04f4a30b62d1d0378035c88823d2c19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872168"
---
# <a name="mft_message_command_marker"></a>MFT \_ 訊息 \_ 命令 \_ 標記

標記資料流程中的點。 此訊息只適用于 [非同步 MFTs](asynchronous-mfts.md)。

## <a name="message-parameter"></a>Message 參數

任意值。 在 [METransformMarker](metransformmarker.md) 事件中，MFT 會將值傳回給用戶端。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

MFT 會回應此 messageas，如下所示：

1.  MFT 會從現有的輸入資料產生任意數量的輸出範例，並為每個輸出範例傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。
2.  產生所有輸出之後，MFT 會傳送 [METransformMarker](metransformmarker.md) 事件。 此事件必須在所有 [METransformHaveOutput](metransformhaveoutput.md) 事件之後傳送。

用戶端不需要傳送此訊息，而且應該只傳送此訊息給非同步 MFTs。 同步的 MFT 不會傳送 [METransformMarker](metransformmarker.md) 事件以回應此訊息。

### <a name="implementation"></a>實作

非同步 MFTs 必須如所述回應此訊息。 同步 MFTs 應該忽略此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




