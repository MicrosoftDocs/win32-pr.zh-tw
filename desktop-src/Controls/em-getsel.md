---
title: 'EM_GETSEL 訊息 (Winuser .h) '
description: 取得 (在編輯控制項中目前選取範圍的 TCHARs) 中的開始和結束字元位置。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca5f3cf1fdaa3c40dd1bb25ebbabb672474e76ae621a05cf52247c216adca17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048798"
---
# <a name="em_getsel-message"></a>EM \_ GETSEL 訊息

取得 **TCHAR** 的開始和結束字元位置 (在編輯控制項中目前選取範圍的) 。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** 值的指標，此值會接收選取範圍的開始位置。 此參數可以是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** 值的指標，此值會接收選取範圍結尾之後第一個未選取字元的位置。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是以零為起始的值，其中包含選取範圍在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))中的開始位置，以及 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中最後一個選取的 **TCHAR** 之後的第一個 **TCHAR** 位置。 如果其中一個值超過65535，則傳回值為-1。

最好使用 *wParam* 和 *lParam* 中傳回的值，因為它們是完整的32位值。

## <a name="remarks"></a>備註

如果沒有選取專案，開始和結束值都是插入號的位置。

**Rich edit 控制項：** 您也可以使用 [**EM \_ EXGETSEL**](em-exgetsel.md) 訊息來取得相同的資訊。 **EM \_EXGETSEL** 也會傳回開頭和結尾字元位置做為32位值。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[**EM \_ EXGETSEL**](em-exgetsel.md)
</dt> <dt>

[**EM \_ SETSEL**](em-setsel.md)
</dt> </dl>

 

