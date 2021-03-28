---
description: '\_當系統色彩設定有變更時，會將 WM SYSCOLORCHANGE 訊息傳送至所有最上層視窗。'
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: 'WM_SYSCOLORCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973768"
---
# <a name="wm_syscolorchange-message"></a>WM \_ SYSCOLORCHANGE 訊息

當系統色彩設定有變更時，會將 **WM \_ SYSCOLORCHANGE** 訊息傳送至所有最上層視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="remarks"></a>備註

系統會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至受系統色彩變更影響的任何視窗。

具有使用現有系統色彩之筆刷的應用程式應該刪除這些筆刷，然後使用新的系統色彩重新建立這些筆刷。

使用通用控制項的最上層視窗必須將 **WM \_ SYSCOLORCHANGE** 訊息轉寄給控制項; 否則，將不會通知控制項色彩變更。 這可確保您的通用控制項所使用的色彩與其他使用者介面物件所使用的色彩一致。 例如，工具列控制項會使用「3D 物件」色彩來繪製其按鈕。 如果使用者變更3D 物件色彩，但卻未將 **WM \_ SYSCOLORCHANGE** 訊息轉寄至工具列，則工具列按鈕會維持其原始色彩，而系統中其他按鈕的色彩也會變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[色彩總覽](colors.md)
</dt> <dt>

[色彩訊息](color-messages.md)
</dt> <dt>

[**WM \_ 油漆**](wm-paint.md)
</dt> </dl>

 

 
