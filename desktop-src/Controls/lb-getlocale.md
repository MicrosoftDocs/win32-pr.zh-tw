---
title: 'LB_GETLOCALE 訊息 (Winuser .h) '
description: 取得清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有磅 \_ 排序樣式) 的清單方塊，以及 LB ADDSTRING 訊息所加入的文字 \_ 。
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544518"
---
# <a name="lb_getlocale-message"></a>LB \_ GETLOCALE 訊息

取得清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有 [**磅 \_ 排序**](list-box-styles.md) 樣式) 的清單方塊，以及 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息所加入的文字。

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

傳回值會指定清單方塊的目前地區設定。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含國家/地區代碼，而 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含語言識別項。

## <a name="remarks"></a>備註

語言識別項包含子語言識別項和主要語言識別項。 使用 [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) 宏將主要語言識別項從傳回值的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中解壓縮，並使用 [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) 宏來解壓縮語言識別項。

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

