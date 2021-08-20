---
title: 'MCIWNDM_GETERROR 訊息 (Vfw .h) '
description: MCIWNDM \_ GETERROR 訊息會捕獲最後發生的 MCI 錯誤。 您可以使用 MCIWndGetError 宏明確地傳送此訊息。
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b748aec6cf686ecf47baf8deae621514e620971f5e1da667f8e4f0aae708ab80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137719"
---
# <a name="mciwndm_geterror-message"></a>MCIWNDM \_ GETERROR 訊息

**MCIWNDM \_ GETERROR** 訊息會捕獲最後發生的 MCI 錯誤。 您可以使用 [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*萊恩*
</dt> <dd>

錯誤緩衝區的大小（以位元組為單位）。

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

用來傳回錯誤字串之應用程式定義緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回整數誤差值。

## <a name="remarks"></a>備註

如果 *lp* 是有效的指標，則會在緩衝區中傳回對應至錯誤的以 null 終止的字串。 如果錯誤字串的長度超過緩衝區，MCIWnd 會將它截斷。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





