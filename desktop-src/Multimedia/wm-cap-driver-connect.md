---
title: 'WM_CAP_DRIVER_CONNECT 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式連線 \_ ] 訊息會將捕獲視窗連接至 capture 驅動程式。 您可以使用 capDriverConnect 宏明確地傳送此訊息。'
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384470"
---
# <a name="wm_cap_driver_connect-message"></a>WM \_ CAP \_ 驅動程式 \_ 連接訊息

[ **WM \_ CAP \_ 驅動程式連線 \_ ]** 訊息會將捕獲視窗連接至 capture 驅動程式。 您可以使用 [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) 宏明確地傳送此訊息。


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Capture 驅動程式的索引。 索引的範圍可以從0到9。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果指定的捕獲驅動程式無法連接到捕捉視窗，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

將捕獲驅動程式連接到「捕獲」視窗，會自動中斷任何先前連線的捕獲驅動程式。

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

 

 





