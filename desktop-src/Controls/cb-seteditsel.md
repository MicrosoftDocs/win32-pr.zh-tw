---
title: 'CB_SETEDITSEL 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETEDITSEL 訊息，以選取下拉式方塊編輯控制項中的字元。
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465252"
---
# <a name="cb_seteditsel-message"></a>CB \_ SETEDITSEL 訊息

應用程式會傳送 **CB \_ SETEDITSEL** 訊息，以選取下拉式方塊編輯控制項中的字元。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

*LParam* 的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定開始位置。 如果 **LOWORD** 為-1，則會移除選取範圍（如果有的話）。

*LParam* 的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定結束位置。 如果 **HIWORD** 為-1，則會選取從開始位置到編輯控制項中最後一個字元的所有文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為 **TRUE**。 如果訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) 樣式的下拉式方塊，則為 CB \_ ERR。

## <a name="remarks"></a>備註

這些位置以零為基底。 編輯控制項的第一個字元位於零位置。 最後一個選取的字元之後的第一個字元是在結束位置。 例如，若要選取編輯控制項的前四個字元，請使用0和結束位置4的開始位置。

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

[**CB \_ GETEDITSEL**](cb-geteditsel.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

