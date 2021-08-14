---
title: 'EM_SETIMESTATUS 訊息 (Winuser .h) '
description: 設定狀態旗標，以決定編輯控制項如何與輸入方法編輯器互動 (IME) 。
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5a3e5413c577fcecd89ebb27bc61e5fff31f7e71b3ec7e6da67523d6ee9392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412395"
---
# <a name="em_setimestatus-message"></a>EM \_ SETIMESTATUS 訊息

設定狀態旗標，以決定編輯控制項如何與輸入方法編輯器互動 (IME) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定的狀態類型。 此參數可為下列值。



| 值                                                                                                                                                                                       | 意義                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | 設定處理撰寫字串的行為。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

狀態類型的特定資料。 如果 *wParam* 是 **EMSIS \_ COMPOSITIONSTRING**，則這個參數可以是下列其中一個或多個值。



| 值                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | 如果設定此旗標，則編輯控制項會將 *lParam* 設定為 gc RESULTSTR 的 [**WM \_ IME \_ 組合**](/windows/desktop/Intl/wm-ime-composition)訊息進行攔截， \_ 並立即傳回結果字串。 如果未設定此旗標，則編輯控制項會將 **wm \_ IME \_ 組合** 訊息傳遞至預設視窗程式，並處理來自 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息的結果字串，這是編輯控制項的預設行為。<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | 如果設定此旗標，則編輯控制項會在收到 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息時取消撰寫字串。 如果未設定此旗標，則編輯控制項不會取消撰寫字串;這是編輯控制項的預設行為。<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | 如果設定此旗標，則編輯控制項會在收到 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) 訊息時完成組合字元串。 如果未設定此旗標，則編輯控制項不會完成組合字元串;這是編輯控制項的預設行為。<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 *lParam* 參數的先前值。

## <a name="remarks"></a>備註

**Rich Edit：** 不支援 **EM \_ SETIMESTATUS** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETIMESTATUS**](em-getimestatus.md)
</dt> </dl>

 

