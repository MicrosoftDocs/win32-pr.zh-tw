---
title: 'CBEM_GETITEM 訊息 (Commctrl .h) '
description: 取得指定之 ComboBoxEx 專案的專案資訊。
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcf4dadf72a9f1fab679599c01c8fd0c6ca3541f2f77a5e8c52a740828966034
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528058"
---
# <a name="cbem_getitem-message"></a>CBEM \_ GETITEM 訊息

取得指定之 ComboBoxEx 專案的專案資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的指標，此結構會接收專案資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

傳送訊息時，必須設定結構的 **iItem** 和 **mask** 成員，以表示目標專案的索引，以及要抓取的資訊類型。 其他成員則會視需要設定。 例如，若要取出文字，您必須 \_ 在 **mask** 中設定 CBEIF 文字旗標，並將值指派給 **cchTextMax**。 將 **iItem** 成員設定為-1，將會抓取編輯控制項中顯示的專案。

如果在 \_ [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **MASK** 成員中設定 CBEIF 文字旗標，控制項可能會變更結構的 **pszText** 成員以指向新的文字，而不是以要求的文字填滿緩衝區。 應用程式不應假設文字一定會放在要求的緩衝區中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEM \_GETITEMW** (Unicode) 和 **CBEM \_ GETITEMA** (ANSI) <br/>                 |



 

 





