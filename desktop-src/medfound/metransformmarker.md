---
description: 由非同步媒體基礎轉換 (MFT) 傳送，以回應 MFT \_ 訊息 \_ 命令 \_ 標記訊息。
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: 'METransformMarker 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974588"
---
# <a name="metransformmarker-event"></a>METransformMarker 事件

由非同步媒體基礎轉換 (MFT) 傳送，以回應 **MFT \_ 訊息 \_ 命令 \_ 標記** 訊息。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                      | 描述                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MF \_ 事件 \_ MFT \_ 內容](mf-event-mft-context.md)<br/> | 來自 **MFT \_ 訊息 \_ 命令 \_ 標記** 訊息的 *ulParam* 參數值。<br/>*需要 ()*<br/> |



## <a name="remarks"></a>備註

非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。 同步 MFTs 不會傳送此事件。

非同步 MFT 的用戶端可以藉由呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 與 **MFT \_ 訊息 \_ 命令 \_ 標記** 訊息，將標記放置於資料流程中。 *UlParam* 參數包含應用程式定義的資料。

當 MFT 完成處理 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 呼叫時可用的所有輸入資料時，mft 會將 METransformMarker 事件排在佇列中。 事件的 [MF \_ 事件 \_ MFT \_ 上下文](mf-event-mft-context.md) 屬性包含 *ulParam* 參數的值。 如需詳細資訊，請參閱 [非同步 MFTs](asynchronous-mfts.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




