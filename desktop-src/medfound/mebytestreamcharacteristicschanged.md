---
description: 當位元組資料流程的特性變更時，由位元組資料流程傳送。
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: 'MEByteStreamCharacteristicsChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001348"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>MEByteStreamCharacteristicsChanged 事件

當位元組資料流程的特性變更時，由位元組資料流程傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ 空白 <br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件表示下列一或多個特性已變更：

-   功能旗標 ([**IMFByteStream：： GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities)) 
-   資料流程結尾旗標 ([**IMFByteStream：： IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream)) 
-   Length ([**IMFByteStream：： GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength)) 

並非所有的 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 執行都支援此事件。 若要接收事件，請查詢 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面的位元組資料流程物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




