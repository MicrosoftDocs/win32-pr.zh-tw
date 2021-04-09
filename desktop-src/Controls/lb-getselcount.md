---
title: 'LB_GETSELCOUNT 訊息 (Winuser .h) '
description: 取得多重選取清單方塊中選取的專案總數。
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- LB_GETSELCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094316"
---
# <a name="lb_getselcount-message"></a>LB \_ GETSELCOUNT 訊息

取得多重選取清單方塊中選取的專案總數。

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

傳回值是清單方塊中已選取專案的計數。 如果清單方塊是單一選取清單方塊，則傳回值為 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





