---
title: 'CBEM_SETITEM 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項中專案的屬性。
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM message Windows 控制項
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
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686382"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEM \_SETITEMW** (Unicode) 和 **CBEM \_ SETITEMA** (ANSI) <br/>                 |



 

 





