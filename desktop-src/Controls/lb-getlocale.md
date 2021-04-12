---
title: 'LB_GETLOCALE 訊息 (Winuser .h) '
description: 取得清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有磅 \_ 排序樣式) 的清單方塊，以及 LB ADDSTRING 訊息所加入的文字 \_ 。
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE message Windows 控制項
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
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465689"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



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

 

