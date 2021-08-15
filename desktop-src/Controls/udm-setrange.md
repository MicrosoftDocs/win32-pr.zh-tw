---
title: 'UDM_SETRANGE 訊息 (Commctrl .h) '
description: 設定上下按鈕 (範圍) 的最小和最大位置。
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60499c960b7f2e496dc4317229865a8838013fc5d78c194072bee27e761ba4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408053"
---
# <a name="udm_setrange-message"></a>UDM \_ SETRANGE 訊息

設定上下按鈕 (範圍) 的最小和最大位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是指定上下按鈕控制項最大位置的 **短**，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))則是指定最小位置的 **簡短**。 這兩個位置都不能大於 UD \_ MAXVAL 值或小於 ud \_ MINVAL 值。 此外，兩個位置之間的差異不能超過 UD \_ MAXVAL。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

最大位置可能小於最小位置。 按一下向上箭號按鈕，將目前的位置向下移動到最大位置，然後按一下向下箭號按鈕移至最小位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM \_ SETRANGE**](udm-setrange.md)
</dt> </dl>

 

