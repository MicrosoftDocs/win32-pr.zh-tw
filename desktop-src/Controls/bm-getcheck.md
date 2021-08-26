---
title: 'BM_GETCHECK 訊息 (Winuser .h) '
description: 取得選項按鈕或核取方塊的檢查狀態。 您可以明確地傳送此訊息，或使用按鈕 \_ GetCheck 宏。
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5eb87d98752bd0cd447d48c648bc4a55e93c3f8eb418a81a07e04113a86633a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921288"
---
# <a name="bm_getcheck-message"></a>BM \_ GETCHECK 訊息

取得選項按鈕或核取方塊的檢查狀態。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

使用 [**BS \_ AUTOCHECKBOX**](button-styles.md)、 [**BS \_ AUTORADIOBUTTON**](button-styles.md)、 [**BS \_ AUTO3STATE**](button-styles.md)、 [**BS \_ CHECKBOX**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕或 [**BS \_ 3STATE**](button-styles.md) 樣式所建立之按鈕的傳回值可以是下列其中一項。



| 傳回碼                                                                                       | 描述                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ 已核取**</dt> </dl>       | 按鈕已核取。<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ 不定**</dt> </dl> | 按鈕會呈現灰色，表示只有在按鈕具有 [**BS \_ 3STATE**](button-styles.md) 或 [**BS \_ AUTO3STATE**](button-styles.md) 樣式) 時，才會套用不定狀態 (。<br/> |
| <dl> <dt>**未核取 BST \_**</dt> </dl>     | 已清除按鈕<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>備註

如果按鈕的樣式不是列出的，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**BM \_ >GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





