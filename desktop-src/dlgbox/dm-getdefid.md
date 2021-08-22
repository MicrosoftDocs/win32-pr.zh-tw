---
title: 'DM_GETDEFID 訊息 (Winuser .h) '
description: 抓取對話方塊的預設按鈕控制項識別碼。
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID 訊息對話方塊
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6898ed6484a66e1c0d5fa498b0352498c0a57fbe91a74f738e2c6438511aef21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785820"
---
# <a name="dm_getdefid-message"></a>DM \_ GETDEFID 訊息

抓取對話方塊的預設按鈕控制項識別碼。


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果預設的 [推送] 按鈕存在，則傳回值的高序位文字會包含值 **DC \_ HASDEFID** ，而低序位單字則包含控制項識別碼。 否則，傳回值為零。

## <a name="remarks"></a>備註

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)函式會處理此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ SETDEFID**](dm-setdefid.md)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> </dl>

 

 





