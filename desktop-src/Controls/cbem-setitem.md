---
title: 'CBEM_SETITEM 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項中專案的屬性。
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1010c090283a47404ee93ef5f3bc1cf2d5ffe71a646d6d734cb443152bdd64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527928"
---
# <a name="cbem_setitem-message"></a>CBEM \_ SETITEM 訊息

設定 ComboBoxEx 控制項中專案的屬性。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的指標，其中包含要設定的專案資訊。 傳送訊息時，必須設定結構的 **遮罩** 成員，以指出哪些屬性有效，且 **iItem** 成員必須指定要修改之專案的以零為基底的索引。 將 **iItem** 成員設定為-1，將會修改編輯控制項中顯示的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEM \_SETITEMW** (Unicode) 和 **CBEM \_ SETITEMA** (ANSI) <br/>                 |



 

 





