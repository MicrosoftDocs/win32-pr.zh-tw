---
title: 'BM_GETSTATE 訊息 (Winuser .h) '
description: 抓取按鈕或核取方塊的狀態。 您可以明確地傳送此訊息，或使用按鈕 \_ >getstate 宏。
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933969"
---
# <a name="bm_getstate-message"></a>BM \_ >getstate 訊息

抓取按鈕或核取方塊的狀態。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ >getstate**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) 宏。

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

傳回值會指定按鈕的目前狀態。 它是下列值的組合。



| 傳回碼                                                                                        | Description                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ 已核取**</dt> </dl>        | 按鈕已核取。<br/>                                                                                                                                                                                        |
| <dl> <dt>**BST \_ DROPDOWNPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md)。 按鈕處於下拉式狀態。 僅適用于按鈕具有 [ [**TBSTYLE \_ ] 下拉式**](toolbar-control-and-button-styles.md) 樣式時。<br/> |
| <dl> <dt>**BST \_ 焦點**</dt> </dl>          | 按鈕具有鍵盤焦點。<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ 熱**</dt> </dl>            | 按鈕是經常性的;也就是滑鼠停留在其上方。<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ 不定**</dt> </dl>  | 按鈕的狀態為不定。 只有在按鈕具有 [**BS \_ 3STATE**](button-styles.md) 或 [**BS \_ AUTO3STATE**](button-styles.md) 樣式時才適用。<br/>                    |
| <dl> <dt>**BST \_ 推送**</dt> </dl>         | 此按鈕會顯示為已推送的狀態。<br/>                                                                                                                                                                |
| <dl> <dt>**未核取 BST \_**</dt> </dl>      | 沒有特殊狀態。 相當於零。<br/>                                                                                                                                                                         |



 

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

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





