---
title: 'MM_JOY2BUTTONUP 訊息 (Mmsystem .h) '
description: MM \_ JOY2BUTTONUP 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID2 已釋放按鈕。
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f94a1761686bd2e3ac7c470268427a213d54cdb4b8a58d54fdd6961427c2377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557308"
---
# <a name="mm_joy2buttonup-message"></a>MM \_ JOY2BUTTONUP 訊息

**MM \_ JOY2BUTTONUP** 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID2 已釋放按鈕。


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>參數

<dl> <dt>

**fwButtons** 
</dt> <dd>

識別已變更狀態的按鈕和已按下的按鈕。 可以是下列其中一項：



| 值                                                                                                                                                            | 意義                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**歡樂 \_ BUTTON1CHG**</dt> </dl> | 第一個搖桿按鈕的狀態已變更。<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**歡樂 \_ BUTTON2CHG**</dt> </dl> | 第二個操縱杆按鈕已變更狀態。<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**歡樂 \_ BUTTON3CHG**</dt> </dl> | 第三個搖桿按鈕的狀態已變更。<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**歡樂 \_ BUTTON4CHG**</dt> </dl> | 第四個操縱杆按鈕的狀態已變更。<br/> |



 

以及下列一或多項：



| 值                                                                                                                                                   | 意義                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**歡樂 \_ BUTTON1**</dt> </dl> | 第一個搖桿按鈕已按下。<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**歡樂 \_ BUTTON2**</dt> </dl> | 按下第二個操縱杆按鈕。<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**歡樂 \_ BUTTON3**</dt> </dl> | 按下第三個操縱杆按鈕。<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**歡樂 \_ BUTTON4**</dt> </dl> | 按第四個操縱杆按鈕。<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

搖桿相對於工作區左上角的 x 座標。

</dd> <dt>

**yPos** 
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

 

 





