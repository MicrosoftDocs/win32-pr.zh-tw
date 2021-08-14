---
title: 'CB_GETEDITSEL 訊息 (Winuser .h) '
description: 取得下拉式方塊的編輯控制項中目前選取範圍的開始和結束字元位置。
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- CB_GETEDITSEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 220750e96e08455eb36e6b6d698fb99056ad3dca6dfbb51054c6cd7cc33fd7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171603"
---
# <a name="cb_geteditsel-message"></a>CB \_ GETEDITSEL 訊息

取得下拉式方塊的編輯控制項中目前選取範圍的開始和結束字元位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** 值的指標，此值會接收選取範圍的開始位置。 此參數可以是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** 值的指標，此值會接收選取範圍的結束位置。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是以零為起始的 **DWORD** 值，其中包含在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中選取範圍的開始位置，以及在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中最後一個選取的字元之後的第一個字元結束位置。

## <a name="examples"></a>範例

下列程式碼範例顯示兩種方法來抓取目前的選取範圍。


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ SETEDITSEL**](cb-seteditsel.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

