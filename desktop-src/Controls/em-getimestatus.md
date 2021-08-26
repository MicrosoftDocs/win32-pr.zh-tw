---
title: 'EM_GETIMESTATUS 訊息 (Winuser .h) '
description: 取得一組狀態旗標，指出編輯控制項如何與輸入方法編輯器互動 (IME) 。
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a8251a62aa9cf48bcc6476af27e4c3a5dbbb82dd0ce76ca21ae094225a3e46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048988"
---
# <a name="em_getimestatus-message"></a>EM \_ GETIMESTATUS 訊息

取得一組狀態旗標，指出編輯控制項如何與輸入方法編輯器互動 (IME) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出的狀態類型。 此參數可為下列值。



| 值                                                                                                                                                                                       | 意義                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | 設定處理組合字元串的行為。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

要抓取之狀態類型的特定資料。 針對 *status* 的 **EMSIS \_ COMPOSITIONSTRING** 值，此傳回值是下列其中一個或多個值。



| 傳回碼                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | 如果設定此旗標，則編輯控制項會將 *fFlags* 設定為 gc RESULTSTR 的 [**WM \_ IME \_ 組合**](/windows/desktop/Intl/wm-ime-composition)訊息進行攔截， \_ 並立即傳回結果字串。 如果未設定此旗標，則編輯控制項會將 **wm \_ IME \_ 組合** 訊息傳遞至預設視窗程式，並處理來自 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息的結果字串，這是編輯控制項的預設行為。<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | 如果設定此旗標，則編輯控制項會在收到 [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) 訊息時取消撰寫字串。 如果未設定此旗標，則編輯控制項不會取消撰寫字串;這是編輯控制項的預設行為。<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | 如果設定此旗標，則編輯控制項會在收到 [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) 訊息時完成組合字元串。 如果未設定此旗標，則編輯控制項不會完成組合字元串;這是編輯控制項的預設行為。<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>備註

**Rich Edit：** 不支援 **EM \_ GETIMESTATUS** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETIMESTATUS**](em-setimestatus.md)
</dt> </dl>

 

