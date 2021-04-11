---
title: 'EM_NOSETFOCUS 訊息 (Commctrl .h) '
description: 防止單一行編輯控制項接收鍵盤焦點。 您可以使用 [編輯 NoSetFocus] 宏明確地傳送此訊息 \_ 。
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105102"
---
# <a name="em_nosetfocus-message"></a>EM \_ NOSETFOCUS 訊息

\[適用于內部用途;不建議在應用程式中使用。 未來的 Windows 版本可能不支援此訊息。\]

防止單一行編輯控制項接收鍵盤焦點。 您可以使用 [ [**編輯 \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) ] 宏明確地傳送此訊息。

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

未使用傳回值。

## <a name="security-considerations"></a>安全性考量

使用此訊息可能會危害程式的安全性。

## <a name="remarks"></a>備註

如果編輯控制項不是單行編輯控制項，則會忽略此訊息。

傳送此訊息之後，效果會是永久性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**編輯 \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ TAKEFOCUS**](em-takefocus.md)
</dt> </dl>

 

 





