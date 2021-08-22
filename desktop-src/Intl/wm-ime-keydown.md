---
description: 由 IME 傳送至應用程式，以通知應用程式按鍵，並保留訊息順序。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: 'WM_IME_KEYDOWN 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beed8bb074e1bae300d52c52867cc8d1f26b84bb8abf358ad2858df7356a0a0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535308"
---
# <a name="wm_ime_keydown-message"></a>WM \_ 輸入法 \_ KEYDOWN 訊息

由 IME 傳送至應用程式，以通知應用程式按鍵，並保留訊息順序。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
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

[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、[先前的金鑰狀態旗標] 和 [轉換狀態] 旗標，如下表



| bit   | 意義                                                                     |
|-------|-----------------------------------------------------------------------------|
| 0-15  | 重複計數。                                                               |
| 16-23 | 掃描程式碼。                                                                  |
| 24    | 擴充金鑰。 如果這個值是擴充索引鍵，則此值為1。 否則，它是0。 |
| 25-28 | 未使用。                                                                   |
| 29    | 內容程式碼。 這個值一定是 0。                                       |
| 30    | 先前的金鑰狀態。 如果機碼已關閉，則此值為1，如果已啟動則為0。    |
| 31    | 轉換狀態。 這個值一定是 0。                                   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該會傳回0。

## <a name="remarks"></a>備註

應用程式可處理此訊息，或將其傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  函式，以產生相符的 [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> </dl>

 

 
