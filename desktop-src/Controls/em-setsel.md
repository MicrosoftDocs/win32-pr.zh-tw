---
title: 'EM_SETSEL 訊息 (Winuser .h) '
description: 選取編輯控制項中的字元範圍。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464896"
---
# <a name="em_setsel-message"></a>EM \_ SETSEL 訊息

選取編輯控制項中的字元範圍。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

選取範圍的起始字元位置。

</dd> <dt>

*lParam* 
</dt> <dd>

選取範圍的結束字元位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

開始值可以大於結束值。 這兩個值的下限會指定選取範圍中第一個字元的字元位置。 較高的值會指定選取範圍之外第一個字元的位置。

開始值是選取範圍的錨點，而結束值是使用中的端點。 如果使用者使用 SHIFT 鍵來調整選取範圍的大小，則現用端點可以移動，但錨點會維持不變。

如果 [開始] 為0且結尾為-1，則會選取 [編輯] 控制項中的所有文字。 如果啟動為-1，則會取消選取任何目前的選取範圍。

**編輯控制項：** 不論開始和結束的相對值為何，控制項會在結束位置顯示閃爍的插入號。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

如果編輯控制項具有 [**ES \_ NOHIDESEL**](edit-control-styles.md) 樣式，不論控制項是否有焦點，都會反白顯示選取的文字。 如果沒有 **ES \_ NOHIDESEL** 樣式，只有在編輯控制項具有焦點時，才會反白顯示選取的文字。

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

[**EM \_ GETSEL**](em-getsel.md)
</dt> <dt>

[**EM \_ REPLACESEL**](em-replacesel.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**EM \_ EXSETSEL**](em-exsetsel.md)
</dt> </dl>

 

 





