---
title: 'WM_CAP_SET_USER_DATA 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 使用者資料訊息會將 \_ 長的 \_ PTR 資料值與捕捉視窗產生關聯。 您可以使用 capSetUserData 宏明確地傳送此訊息。
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106109"
---
# <a name="wm_cap_set_user_data-message"></a>WM \_ CAP \_ 設定 \_ 使用者 \_ 資料訊息

**WM \_ CAP \_ 設定 \_ 使用者 \_ 資料** 訊息會將長的 **\_ PTR** 資料值與捕捉視窗產生關聯。 您可以使用 [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

與捕捉視窗相關聯的資料值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉正在進行，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息通常是用來指向與捕捉視窗相關聯的資料區塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 





