---
title: 'MCIWNDM_SENDSTRING 訊息 (Vfw .h) '
description: MCIWNDM \_ SENDSTRING 訊息會以字串形式將 MCI 命令傳送給與 MCIWnd 視窗相關聯的裝置。 您可以使用 MCIWndSendString 宏明確地傳送此訊息。
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98ee008346821c2d489b19d01bb372c37cd3d541380fd8dae3b72bf613051f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037928"
---
# <a name="mciwndm_sendstring-message"></a>MCIWNDM \_ SENDSTRING 訊息

**MCIWNDM \_ SENDSTRING** 訊息會以字串形式將 MCI 命令傳送給與 MCIWnd 視窗相關聯的裝置。 您可以使用 [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) 宏明確地傳送此訊息。


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*深圳*
</dt> <dd>

要傳送至 MCI 裝置的字串命令。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

**MCIWNDM \_ SENDSTRING** 的訊息處理常式會將裝置別名附加至您傳送至裝置的 MCI 命令。 因此，您不應該在使用 **MCIWNDM \_ SENDSTRING** 發出的 MCI 命令中使用任何別名。

若要取得包含命令結果的傳回字串，請傳送 [**MCIWNDM \_ RETURNSTRING**](mciwndm-returnstring.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[多媒體命令字串](multimedia-command-strings.md)
</dt> </dl>

 

 





