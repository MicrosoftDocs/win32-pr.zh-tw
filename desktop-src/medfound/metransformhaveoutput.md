---
description: 當從 MFT 提供新的輸出資料時，由非同步媒體基礎轉換 (MFT) 。
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: 'METransformHaveOutput 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972253"
---
# <a name="metransformhaveoutput-event"></a>METransformHaveOutput 事件

當從 MFT 提供新的輸出資料時，由非同步媒體基礎轉換 (MFT) 。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> |



## <a name="attributes"></a>屬性

未定義此事件的屬性。

## <a name="remarks"></a>備註

非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。 同步 MFTs 不會傳送此事件。

當 MFT 用戶端收到此事件時，它應該呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 來取得輸出。

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

 

 




