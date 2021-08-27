---
title: 'TDM_NAVIGATE_PAGE 訊息 (Commctrl .h) '
description: 以新的內容重新建立工作對話方塊，模擬多頁 wizard 的功能。
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7894bdc5831af2c1fe2e779679aaab38eab94f976cf9c586dfe64d26a051b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104628"
---
# <a name="tdm_navigate_page-message"></a>TDM \_ 導覽 \_ 頁面訊息

以新的內容重新建立工作對話方塊，模擬多頁 wizard 的功能。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

未使用。 必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

描述要建立之工作對話方塊的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) 結構指標。 呼叫的應用程式必須配置此結構並設定其成員。 成員的值會根據使用者流覽至的頁面類型而有所不同。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

若要啟動嚮導工作對話方塊，請使用 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) 函式。 當使用者使用嚮導流覽時，請將此訊息傳送至工作對話方塊以顯示下一個頁面。 新的工作對話方塊 (看起來就像新的頁面) 是使用 *lParam* 所指向的結構中指定的元素所建立。 建立時，會終結並重建對話方塊框架的整個內容。 如此一來，控制項所持有的任何狀態資訊 (例如，會遺失對話方塊中的進度列、expando 按鈕或驗證核取方塊) 。

工作對話方塊的版面配置可能會失敗，而且不會反映在傳回值中。 \_[確定] 的傳回值只會反映工作對話方塊收到的訊息，並嘗試進行處理。 如果工作對話方塊的配置失敗 (工作對話方塊無法顯示) ，對話方塊將會關閉，並且會在註冊的回呼函式傳回 **HRESULT** 程式碼。 如需回呼函數語法的詳細資訊，請參閱 [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

