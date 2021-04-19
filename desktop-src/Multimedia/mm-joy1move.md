---
title: 'MM_JOY1MOVE 訊息 (Mmsystem .h) '
description: MM \_ JOY1MOVE 訊息會通知視窗，該視窗已捕捉到搖桿的位置已變更。
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78753bd55f6682b3ac3f1514356d93cb455d162
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969562"
---
# <a name="mm_joy1move-message"></a>MM \_ JOY1MOVE 訊息

**MM \_ JOY1MOVE** 訊息會通知視窗，該視窗已捕捉到搖桿的位置已變更。


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

識別按下的按鈕。 它可以是下列其中一個或多個值：



| 需求 | 值 |
|--------------|------------------------------------|
| 歡樂 \_ BUTTON1 | 第一個搖桿按鈕已按下。  |
| 歡樂 \_ BUTTON2 | 按下第二個操縱杆按鈕。 |
| 歡樂 \_ BUTTON3 | 按下第三個操縱杆按鈕。  |
| 歡樂 \_ BUTTON4 | 按第四個操縱杆按鈕。 |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

搖桿相對於工作區左上角的 x 座標。

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

操縱杆的 y 座標，相對於工作區的左上角。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[操縱 杆](joysticks.md)
</dt> <dt>

[多媒體操縱杆訊息](multimedia-joystick-messages.md)
</dt> </dl>

 

 





