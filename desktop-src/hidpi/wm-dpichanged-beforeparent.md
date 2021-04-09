---
title: 'WM_DPICHANGED_BEFOREPARENT 訊息 (Winuser .h) '
description: '針對每個監視器 v2 的最上層視窗，此訊息會傳送至正在進行 DPI 變更之視窗的子 HWDN 樹狀目錄中的所有 Hwnd。 |WM_DPICHANGED_BEFOREPARENT 訊息 (Winuser .h) '
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT 訊息高 DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16641916cb16b789f2349a53b09dbd2af5f520f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946000"
---
# <a name="wm_dpichanged_beforeparent-message"></a>WM \_ DPICHANGED \_ BEFOREPARENT 訊息

針對 [每個監視器 v2](dpi-awareness-context.md) 的最上層視窗，此訊息會傳送至正在進行 DPI 變更之視窗的子 HWDN 樹狀目錄中的所有 hwnd。 這則訊息會在最上層視窗接收到 [**WM \_ DPICHANGED**](wm-dpichanged.md)之前發生，並從底部往上往下遍歷子樹狀結構。


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

此值未使用且將為零。

</dd> <dt>

*lParam* 
</dt> <dd>

此值未使用且將為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

系統不會使用並忽略此值。

## <a name="remarks"></a>備註

在 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)中沒有這則訊息的預設處理方式。

只有在最上層視窗具有 PMv2 的 DPI 感知內容時，才會傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ DPICHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ DPICHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)
</dt> </dl>

 

