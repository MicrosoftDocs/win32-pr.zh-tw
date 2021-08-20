---
title: 'TB_SETBUTTONSIZE 訊息 (Commctrl .h) '
description: 設定工具列上的按鈕大小。
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b0b957ad6328515da7aee2f978870662801aa6aba81133e9e4bc22ee7d9c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167731"
---
# <a name="tb_setbuttonsize-message"></a>TB \_ SETBUTTONSIZE 訊息

設定工具列上的按鈕大小。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定按鈕的寬度（以圖元為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定按鈕的高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

**TB \_** 您通常應該在加入按鈕之後呼叫 SETBUTTONSIZE。

使用 [ [**TB] \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) 可設定按鈕在新增之前允許的最大寬度和最小值。 使用 **TB \_ SETBUTTONSIZE** 來設定按鈕的實際大小。

## <a name="examples"></a>範例

下列程式碼範例會將按鈕的寬度設定為80圖元，並將高度設定為30圖元。


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

