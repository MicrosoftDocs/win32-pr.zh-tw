---
title: 'WM_SIZECLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿包含 CF \_ OWNERDISPLAY 格式的資料，而剪貼簿檢視器的工作區已變更時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685998"
---
# <a name="wm_sizeclipboard-message"></a>WM \_ SIZECLIPBOARD 訊息

當剪貼簿包含 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的資料，而剪貼簿檢視器的工作區已變更時，由剪貼簿檢視器視窗傳送給剪貼簿擁有者。


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

剪貼簿檢視器視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

全域記憶體物件的控制碼，其中包含 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構。 結構會指定剪貼簿檢視器工作區的新維度。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

當剪貼簿檢視器視窗即將終結或調整大小時，會以 null 矩形傳送 **WM \_ SIZECLIPBOARD** 訊息 (0、0、0、0) 作為新的大小。 這可讓剪貼簿擁有者釋放其顯示資源。

剪貼簿擁有者必須使用 [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) 函式來鎖定包含 [**RECT**](/previous-versions//dd162897(v=vs.85))的記憶體物件。 在傳回之前，剪貼簿擁有者必須使用 [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) 函數來解除鎖定物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

