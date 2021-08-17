---
description: 如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: 'MEPolicyError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1f0d05b73ea295ea3282af5950d4a9a61f833f61463cd095848563e3858c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877545"
---
# <a name="mepolicyerror-event"></a>MEPolicyError 事件

如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。

如果媒體會話收到此事件，它會停止播放並將事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




