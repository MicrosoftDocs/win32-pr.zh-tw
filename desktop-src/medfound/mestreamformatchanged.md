---
description: 當資料流程的媒體類型變更時，由媒體資料流程引發。
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: 'MEStreamFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848533"
---
# <a name="mestreamformatchanged-event"></a>MEStreamFormatChanged 事件

當資料流程的媒體類型變更時，由媒體資料流程引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | 新媒體類型之 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

您可以使用此事件來通知資料流程中的格式變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




