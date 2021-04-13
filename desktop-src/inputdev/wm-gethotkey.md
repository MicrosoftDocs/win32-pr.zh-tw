---
title: 'WM_GETHOTKEY 訊息 (Winuser .h) '
description: 傳送以判斷與視窗相關聯的快速鍵。
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- WM_GETHOTKEY 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464936"
---
# <a name="wm_gethotkey-message"></a>WM \_ GETHOTKEY 訊息

傳送以判斷與視窗相關聯的快速鍵。


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是快速鍵的虛擬機器碼和修飾詞，如果沒有任何熱鍵與視窗相關聯，則為 **Null** 。 虛擬機器碼是在傳回值的低位元組內，而修飾詞是在高位元組中。 修飾詞可以是下列 CommCtrl 旗標的組合。



| 傳回碼/值                                                                                                                                         | Description             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**HOTKEYF \_ALT**</dt> <dt>0x04</dt> </dl>     | ALT 鍵<br/>      |
| <dl> <dt>**HOTKEYF \_控制**</dt> <dt>0x02</dt> </dl> | CTRL 鍵<br/>     |
| <dl> <dt>**HOTKEYF \_EXT**</dt> <dt>0x08</dt> </dl>     | 擴充金鑰<br/> |
| <dl> <dt>**HOTKEYF \_SHIFT**</dt> <dt>0x01</dt> </dl>   | SHIFT 鍵<br/>    |



 

## <a name="remarks"></a>備註

這些快速鍵與 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函式所設定的熱鍵無關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 

