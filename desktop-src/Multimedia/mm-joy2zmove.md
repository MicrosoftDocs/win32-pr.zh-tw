---
title: 'MM_JOY2ZMOVE 訊息 (Mmsystem .h) '
description: MM \_ JOY2ZMOVE 訊息會通知視窗，該視窗已捕捉至 Z 軸上的搖桿位置已變更的搖桿 JOYSTICKID2。
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998033"
---
# <a name="mm_joy2zmove-message"></a>MM \_ JOY2ZMOVE 訊息

**MM \_ JOY2ZMOVE** 訊息會通知視窗，該視窗已捕捉至 Z 軸上的搖桿位置已變更的搖桿 JOYSTICKID2。


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

識別按下的按鈕。 它可以是下列一或多個值。



| 需求 | 值 |
|--------------|------------------------------------|
| 歡樂 \_ BUTTON1 | 第一個搖桿按鈕已按下。  |
| 歡樂 \_ BUTTON2 | 按下第二個操縱杆按鈕。 |
| 歡樂 \_ BUTTON3 | 按下第三個操縱杆按鈕。  |
| 歡樂 \_ BUTTON4 | 按第四個操縱杆按鈕。 |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

搖桿的 z 座標。

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

 

 





