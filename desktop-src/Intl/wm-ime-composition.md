---
description: 當 IME 將組合狀態變更為擊鍵結果時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: 'WM_IME_COMPOSITION 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945420"
---
# <a name="wm_ime_composition-message"></a>WM \_ IME \_ 組合訊息

當 IME 將組合狀態變更為擊鍵結果時，傳送至應用程式。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
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

表示組合字元串之最新變更的 DBCS 字元。

</dd> <dt>

*lParam* 
</dt> <dd>

指定組合字元串或字元變更方式的值。 這個參數可以是下列一或多個值。 如需這些值的詳細資訊，請參閱 [IME 組合字元串值](ime-composition-string-values.md)。

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**GC \_ COMPATTR**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**GC \_ COMPCLAUSE**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**GC \_ COMPREADSTR**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**GC \_ COMPREADATTR**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**GC \_ COMPREADCLAUSE**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**GC \_ COMPSTR**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**GC \_ CURSORPOS**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**GC \_ DELTASTART**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**GC \_ RESULTCLAUSE**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**GC \_ RESULTREADCLAUSE**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**GC \_ RESULTREADSTR**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**GC \_ RESULTSTR**
</dt> </dl>

*LParam* 參數也可以具有下列一或多個值。



| 值                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**CS \_ INSERTCHAR**</dt> </dl>    | 在目前的插入點插入 *wParam* 組合字元。 如果應用程式處理此訊息，則應該顯示組合字元。<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**CS \_ NOMOVECARET**</dt> </dl> | 請勿移動插入號位置，因為處理訊息的結果。 例如，如果 IME 指定 CS \_ INSERTCHAR 和 cs NOMOVECARET 的組合 \_ ，應用程式應該在目前的插入號位置插入指定的字元，但不應該將插入號移到下一個位置。 \_具有 gc RESULTSTR 的後續 WM IME \_ 組合訊息 \_ 將會取代此字元。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

如果應用程式顯示覆合字元本身，就應該處理此訊息。 否則，它應該會將訊息傳送至 IME 視窗。

如果應用程式已建立 IME 視窗，則應該將此訊息傳遞至該視窗。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將此訊息傳遞至預設的 IME 視窗來進行處理。 IME 視窗會根據指定的變更旗標來更新其外觀，以處理此訊息。 應用程式可以呼叫 [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) 來取得新的組合狀態。

如果未設定任何 GC \_ 值，訊息會指出目前的組合已取消，而繪製組合字元串的應用程式應刪除字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                                                      |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
