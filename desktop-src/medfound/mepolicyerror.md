---
description: 如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: 'MEPolicyError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980759"
---
# <a name="mepolicyerror-event"></a>MEPolicyError 事件

如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。

如果媒體會話收到此事件，它會停止播放並將事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

從 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) 取出的可能值包括下列各項。



| 值                      | 描述                                                    |
|----------------------------|----------------------------------------------------------------|
| \_ \_ 不支援 MF E 原則 \_ | 受信任的輸出不支援目前的輸出原則。 |



 

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

 

 




