---
description: 當使用者選擇新的輸入語言時，會使用鍵盤控制台應用程式中所指定的熱鍵 () 或從系統工作列上的指標，張貼至視窗。
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: 'WM_INPUTLANGCHANGEREQUEST 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644fa4764c5172edc34f16509c6a6b00be6356b80c460a08233be8aa64ef69c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056058"
---
# <a name="wm_inputlangchangerequest-message"></a>WM \_ INPUTLANGCHANGEREQUEST 訊息

當使用者選擇新的輸入語言時，會使用鍵盤控制台應用程式中所指定的熱鍵 () 或從系統工作列上的指標，張貼至視窗。 應用程式可以藉由將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式或拒絕變更 (來接受變更，並使其無法在不) 的情況下立即返回。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新的輸入地區設定。 這個參數可以是下列旗標的組合。



| 值                                                                                                                                                                                                                                                            | 意義                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_反向**</dt> <dt>0x0004</dt> </dl>       | 快速鍵是用來在已安裝的輸入地區設定清單中，選擇先前的輸入地區設定。 此旗標不可與 INPUTLANGCHANGE 轉寄旗標一起使用 \_ 。<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_轉寄**</dt> <dt>0x0002</dt> </dl>          | 快速鍵是用來選擇已安裝之輸入地區設定清單中的下一個輸入地區設定。 此旗標不可與 INPUTLANGCHANGE 回溯旗標一起使用 \_ 。<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_SYSCHARSET**</dt> <dt>0x0001</dt> </dl> | 新輸入地區設定的鍵盤配置可以搭配系統字元集使用。<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

輸入地區設定識別碼。 如需詳細資訊，請參閱 [語言、地區設定和鍵盤配置](../inputdev/about-keyboard-input.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

這則訊息會張貼至應用程式，而不會傳送給應用程式，因此會忽略傳回值。 若要接受變更，應用程式應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。 若要拒絕變更，應用程式應該在不呼叫 **DefWindowProc** 的情況下傳回零。

## <a name="remarks"></a>備註

當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式收到 **WM \_ INPUTLANGCHANGEREQUEST** 訊息時，它會啟用新的輸入地區設定，並藉由傳送 [**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md) 訊息來通知應用程式變更。

只有當您已安裝多個鍵盤配置，且已使用鍵盤 [控制台] 應用程式啟用指標時，才會在工作列上顯示語言指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
