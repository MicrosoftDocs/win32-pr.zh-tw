---
description: 當清空作業完成時，由非同步媒體基礎轉換 (MFT) 傳送。
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: 'METransformDrainComplete 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5ab03ac5027d1dc7549e7b7f0b8494cd8066b07afb64c5df17415a4986866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974027"
---
# <a name="metransformdraincomplete-event"></a>METransformDrainComplete 事件

當清空作業完成時，由非同步媒體基礎轉換 (MFT) 傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述               |
|----------------------|---------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                        | 描述                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼](mf-event-mft-input-stream-id.md)<br/> | 已清空的資料流程識別碼。<br/>*需要 ()*<br/> |



## <a name="remarks"></a>備註

非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。 同步 MFTs 不會傳送此事件。

若要清空 MFT，請使用 **mft \_ 訊息 \_ 命令 \_ 清空** 訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。 指定要在 *ulParam* 參數中清空的輸入資料流程。 清空作業完成時，非同步 MFT 會傳送 METransformDrainComplete 事件。 事件的 [MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_](mf-event-mft-input-stream-id.md) 識別碼屬性包含 *ulParam* 參數中提供的資料流程識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




