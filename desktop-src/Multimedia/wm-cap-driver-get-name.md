---
title: 'WM_CAP_DRIVER_GET_NAME 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式名稱。 您可以使用 capDriverGetName 宏明確地傳送此訊息。'
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc44efae992f2967cb069c0866fbb7f9febed51ea73f94853a1b017bc57a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369679"
---
# <a name="wm_cap_driver_get_name-message"></a>WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱訊息

[ **WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱** ] 訊息會傳回連接至 [捕獲] 視窗的捕獲驅動程式名稱。 您可以使用 [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) 宏明確地傳送此訊息。


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**>Szname** 所參考的緩衝區大小（以位元組為單位）。

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

應用程式定義的緩衝區指標，用來將裝置名稱傳回為以 null 結束的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

名稱是取自驅動程式資源區域的文字字串。 應用程式應該為此字串配置大約80個位元組。 如果驅動程式未包含名稱資源，則會傳回登錄或 SYSTEM.INI 檔中所列之驅動程式的完整路徑名稱。

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

 

 





