---
description: 當 IME 取得轉換結果的字元時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: 'WM_IME_CHAR 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337ca982cbd755e01f3dfab465d8b82948dfdbf053a4a7c03417a1d508bc42d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146781"
---
# <a name="wm_ime_char-message"></a>WM \_ IME \_ 字元訊息

當 IME 取得轉換結果的字元時，傳送至應用程式。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
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

**DBCS：** 單一位元組或雙位元組字元值。 若為雙位元組字元， (位元組)  (wParam >> 8) 包含前導位元組。 請注意，括弧是必要的，因為 cast 運算子的優先順序高於移位運算子。

**Unicode：** Unicode 字元值。

</dd> <dt>

*lParam* 
</dt> <dd>

重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的金鑰狀態旗標，以及轉換狀態旗標，其值如下所定義。



| bit   | 意義                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | 重複計數。 因為第一個位元組和第二個位元組是連續的，所以這一律為1。 |
| 16-23 | 掃描完整亞洲字元的程式碼。                                            |
| 24    | 擴充金鑰。                                                                        |
| 25-28 | 未使用。                                                                            |
| 29    | 內容程式碼。                                                                        |
| 30    | 先前的金鑰狀態。                                                                  |
| 31    | 轉換狀態。                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>備註

不同于非 Unicode 視窗的 [**WM \_ CHAR**](../inputdev/wm-char.md) 訊息，此訊息可以包含雙位元組和單一位元組字元值。 若為 Unicode 視窗，此訊息與 WM \_ 字元相同。

針對非 Unicode 視窗，如果 WM \_ IME \_ 字元訊息包含雙位元組字元，而且應用程式將此訊息傳遞給 [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，則 IME 會將此訊息轉換成兩個 WM \_ 字元訊息，每個字元都包含一個位元組的雙位元組字元。

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

 

 
