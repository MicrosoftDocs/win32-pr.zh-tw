---
title: 'BM_SETCHECK 訊息 (Winuser .h) '
description: 設定選項按鈕或核取方塊的核取狀態。 您可以明確地傳送此訊息，或使用按鈕 \_ SetCheck 宏來傳送。
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024676"
---
# <a name="bm_setcheck-message"></a>BM \_ SETCHECK 訊息

設定選項按鈕或核取方塊的核取狀態。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

檢查狀態。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ 已核取**</dt> </dl>                   | 將按鈕狀態設定為 [已檢查]。<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ 不定**</dt> </dl> | 將按鈕狀態設為灰色，表示不定的狀態。 只有當按鈕具有 [**BS \_ 3STATE**](button-styles.md) 或 [**BS \_ AUTO3STATE**](button-styles.md) 樣式時，才使用此值。<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**未核取 BST \_**</dt> </dl>             | 將按鈕狀態設定為 [已清除]。<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息一律會傳回零。

## <a name="remarks"></a>備註

**BM \_ SETCHECK** 訊息不會影響推送按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**BM \_ GETCHECK**](bm-getcheck.md)
</dt> <dt>

[**BM \_ >GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





