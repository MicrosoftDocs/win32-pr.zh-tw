---
title: 'WM_QUERYUISTATE 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ QUERYUISTATE 訊息來取得視窗的 UI 狀態。
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969825"
---
# <a name="wm_queryuistate-message"></a>WM \_ QUERYUISTATE 訊息

應用程式會傳送 **WM \_ QUERYUISTATE** 訊息來取得視窗的 UI 狀態。


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為0。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果焦點指標和鍵盤快速鍵是可見的，則傳回值為 **Null** 。 否則，傳回值可以是下列一或多個值。



| 傳回碼/值                                                                                                                                       | Description                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_現用**</dt> <dt>0x4</dt> </dl>    | 控制項應以用於作用中控制項的樣式來繪製。<br/> |
| <dl> <dt>**UISF \_HIDEACCEL**</dt> <dt>0x2</dt> </dl> | 鍵盤快捷為隱藏。<br/>                                |
| <dl> <dt>**UISF \_HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | 焦點指標是隱藏的。<br/>                                     |



 

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

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ UPDATEUISTATE**](wm-updateuistate.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 

 





