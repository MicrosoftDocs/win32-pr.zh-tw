---
title: 'WM_CAP_DRIVER_GET_VERSION 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式版本資訊。 您可以使用 capDriverGetVersion 宏明確地傳送此訊息。'
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970000"
---
# <a name="wm_cap_driver_get_version-message"></a>WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本訊息

[ **WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本** ] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式版本資訊。 您可以使用 [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) 宏明確地傳送此訊息。


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**SzVer** 所參考的應用程式定義緩衝區大小（以位元組為單位）。

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

應用程式定義的緩衝區指標，用來以 null 終止字串的形式傳回版本資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

版本資訊是取自驅動程式資源區域的文字字串。 應用程式應該為此字串配置大約40個位元組。 如果版本資訊無法使用，則會傳回 **Null** 字串。

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

 

 





