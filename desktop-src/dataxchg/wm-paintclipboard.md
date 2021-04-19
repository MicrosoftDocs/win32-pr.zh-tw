---
title: 'WM_PAINTCLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿包含 CF \_ OWNERDISPLAY 格式的資料，而剪貼簿檢視器的工作區需要重新繪製時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966304"
---
# <a name="wm_paintclipboard-message"></a>WM \_ PAINTCLIPBOARD 訊息

當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而剪貼簿檢視器的工作區需要重新繪製時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

剪貼簿檢視器視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

全域記憶體物件的控制碼，其中包含 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構。 結構會定義要繪製之工作區的部分。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

若要判斷整個工作區或其中一部分是否需要重新繪製，剪貼簿擁有者必須將 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)的 **rcPaint** 成員中提供的繪圖區域尺寸，與最新的 [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md)訊息中提供的維度進行比較。

剪貼簿擁有者必須使用 [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) 函數來鎖定包含 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構的記憶體。 在傳回之前，剪貼簿擁有者必須使用 [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) 函數來解除鎖定該記憶體。

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

[**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

