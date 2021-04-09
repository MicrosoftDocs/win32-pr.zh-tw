---
title: 'EM_SETTEXTMODE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的文字模式或復原層級。 如果控制項包含任何文字，則訊息會失敗。
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934543"
---
# <a name="em_settextmode-message"></a>EM \_ SETTEXTMODE 訊息

設定 rich edit 控制項的文字模式或復原層級。 如果控制項包含任何文字，則訊息會失敗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)列舉型別中的一或多個值。 這些值會指定控制項的文字模式和復原層級參數的新設定。

指定下列其中一個值來設定文字模式參數。 如果您未指定文字模式值，文字模式會維持在其目前的設定中。 

| 值                                          | 意義                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ 純文字**](/windows/win32/api/richedit/ne-richedit-textmode) | 表示純文字模式，在此模式中，控制項類似于標準編輯控制項。 如需純文字模式的詳細資訊，請參閱下列備註一節。 |
| [**TM \_ RICHTEXT**](/windows/win32/api/richedit/ne-richedit-textmode)   | 指出 rich text 模式，其中控制項具有標準的豐富編輯功能。 Rich text 模式是預設設定。                                           |



 

指定下列其中一個值來設定復原層級參數。 如果您沒有指定復原層級值，復原層級會維持在其目前的設定中。 

| 值                                                      | 意義                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | 控制項可讓使用者只復原可以復原的最後一個動作。                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | 控制項支援多個復原作業。 這是預設值。 使用 [**EM \_ SETUNDOLIMIT**](em-setundolimit.md) 訊息來設定復原動作的最大數目。 |



 

指定下列其中一個值來設定字碼頁參數。 如果您未指定字碼頁的值，字碼頁會維持在其目前的設定中。 

| 值                                                    | 意義                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | 控制項只允許與預設字元集對應的英文鍵盤和鍵盤。 例如，您可以有希臘文和英文。 請注意，這可防止 Unicode 文字輸入控制項。 例如，如果 Rich Edit 控制項必須限制為 ANSI 文字，請使用此值。 |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | 控制項允許在控制項中有多個字碼頁和 Unicode 文字。 這是預設值。                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為零。

如果訊息失敗，則傳回值為非零值。

## <a name="remarks"></a>備註

在豐富的文字模式中，豐富的編輯控制項具有標準的豐富編輯功能。 不過，在純文字模式中，控制項類似于標準編輯控制項：

-   純文字控制項中的文字只能有一個格式 (例如粗體、10pt 的 Arial) 。
-   使用者無法將 rich text (格式（例如 rtf) 或内嵌物件）貼入純文字控制項。
-   Rich text 模式控制項一律會有預設的檔結束記號或換行字元，以格式化段落。 另一方面，純文字控制項則不需要預設的檔結束記號，因此會省略。

當控制項收到 **EM \_ SETTEXTMODE** 訊息時，不能包含任何文字。 若要確定沒有任何文字，請將包含空字串 ( "" ) 傳送至 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETTEXTMODE**](em-gettextmode.md)
</dt> <dt>

[**EM \_ SETUNDOLIMIT**](em-setundolimit.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

