---
title: 'CB_SETEXTENDEDUI 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETEXTENDEDUI 訊息，以針對具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式的下拉式方塊，選取預設的 ui 或擴充的 ui \_ 。
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b77e67e555628475b9e40e78b7b0391d0b631fd77e6ff7f549700a553fa507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414220"
---
# <a name="cb_setextendedui-message"></a>CB \_ SETEXTENDEDUI 訊息

應用程式會傳送 **CB \_ SETEXTENDEDUI** 訊息，以針對具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式的下拉式方塊，選取預設的 ui 或擴充的 ui。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**布林** 值，指定下拉式方塊是否使用擴充的 Ui (**TRUE**) 或預設的 ui (**FALSE**) 。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 CB \_ ok。 如果發生錯誤，則為 CB \_ 錯誤。

## <a name="remarks"></a>備註

依預設，F4 鍵會開啟或關閉清單，而向下箭號會變更目前的選取範圍。 在擴充的 UI 中，會停用 F4 鍵，而向下鍵則會開啟下拉式清單。 當設定擴充 UI 時，滑鼠滾輪（通常會在清單中的專案中滾動）沒有任何作用。

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

[**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
</dt> <dt>

**概念**
</dt> <dt>

[下拉式列示方塊功能](combo-box-features.md)
</dt> </dl>

 

 





