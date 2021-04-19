---
description: 由 IME 傳送至應用程式，以通知應用程式金鑰版本並保持訊息順序。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: 'WM_IME_KEYUP 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973071"
---
# <a name="wm_ime_keyup-message"></a>WM \_ 輸入法 \_ KEYUP 訊息

由 IME 傳送至應用程式，以通知應用程式金鑰版本並保持訊息順序。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*wParam* 
</dt> <dd>

金鑰的虛擬按鍵碼。

</dd> <dt>

*lParam* 
</dt> <dd>

重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的金鑰狀態旗標和轉換狀態旗標，如下所示。



| bit   | 意義                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | 重複計數。 這個值一律是 1。                                       |
| 16-23 | 掃描程式碼。                                                                  |
| 24    | 擴充金鑰。 如果這個值是擴充索引鍵，則此值為1。 否則，它是0。 |
| 25-28 | 未使用。                                                                   |
| 29    | 內容程式碼。 這個值一定是 0。                                       |
| 30    | 先前的金鑰狀態。 這個值一律是 1。                                 |
| 31    | 轉換狀態。 這個值一律是 1。                                   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該會傳回0。

## <a name="remarks"></a>備註

應用程式可處理此訊息，或將其傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  函式，以產生相符的 [**WM \_ KEYUP**](../inputdev/wm-keyup.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> </dl>

 

 
