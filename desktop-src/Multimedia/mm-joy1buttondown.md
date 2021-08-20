---
title: 'MM_JOY1BUTTONDOWN 訊息 (Mmsystem .h) '
description: MM \_ JOY1BUTTONDOWN 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID1 已按下按鈕。
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2399eca0de21014b97c9156e6a16349fc5b0b5407b64b022eb077fd59d0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137189"
---
# <a name="mm_joy1buttondown-message"></a>MM \_ JOY1BUTTONDOWN 訊息

**MM \_ JOY1BUTTONDOWN** 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID1 已按下按鈕。


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

識別已變更狀態的按鈕和已按下的按鈕。 可以是下列其中一項：



| 需求 | 值 |
|-----------------|-------------------------------------------|
| 歡樂 \_ BUTTON1CHG | 第一個搖桿按鈕的狀態已變更。  |
| 歡樂 \_ BUTTON2CHG | 第二個操縱杆按鈕已變更狀態。 |
| 歡樂 \_ BUTTON3CHG | 第三個搖桿按鈕的狀態已變更。  |
| 歡樂 \_ BUTTON4CHG | 第四個操縱杆按鈕的狀態已變更。 |



 

以及下列一或多項：



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
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[操縱 杆](joysticks.md)
</dt> <dt>

[多媒體操縱杆訊息](multimedia-joystick-messages.md)
</dt> </dl>

 

 





