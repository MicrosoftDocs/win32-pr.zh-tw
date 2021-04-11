---
title: 'WM_DESTROYCLIPBOARD 訊息 (Winuser .h) '
description: 當 EmptyClipboard 函式的呼叫清空剪貼簿時，傳送給剪貼簿擁有者。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- WM_DESTROYCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935105"
---
# <a name="wm_destroyclipboard-message"></a>WM \_ DESTROYCLIPBOARD 訊息

當 [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) 函式的呼叫清空剪貼簿時，傳送給剪貼簿擁有者。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_DESTROYCLIPBOARD             0x0307
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

如果應用程式處理此訊息，它應該會傳回零。

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

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

