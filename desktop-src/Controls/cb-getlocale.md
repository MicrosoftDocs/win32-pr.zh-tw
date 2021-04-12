---
title: 'CB_GETLOCALE 訊息 (Winuser .h) '
description: 取得下拉式方塊的目前地區設定。 地區設定是用來判斷下拉式方塊中顯示的文字， \_ 以及使用 CB ADDSTRING 訊息加入之 CBS 排序樣式和文字的正確排序次序 \_ 。
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025087"
---
# <a name="cb_getlocale-message"></a>CB \_ GETLOCALE 訊息

取得下拉式方塊的目前地區設定。 地區設定是用來判斷下拉式方塊中顯示的文字，以及使用 [**CB \_ ADDSTRING**](cb-addstring.md)訊息加入之 [**CBS \_ 排序**](combo-box-styles.md)樣式和文字的正確排序次序。

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

傳回值會指定下拉式方塊的目前地區設定。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含國家/地區代碼，而 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含語言識別項。

## <a name="remarks"></a>備註

語言識別項是由多語系識別碼和主要語言識別項所組成。 [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)宏會取得主要語言識別項，而 [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)宏會取得子語言識別項。

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ SETLOCALE**](cb-setlocale.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

