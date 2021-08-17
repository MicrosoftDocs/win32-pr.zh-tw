---
title: 'IPM_SETRANGE 訊息 (Commctrl .h) '
description: 在 IP 位址控制項中，設定指定之欄位的有效範圍。
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d599619fa9a065a27a9721b890f6d52c496bf646504009e1950b7ca1279f8a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434468"
---
# <a name="ipm_setrange-message"></a>IPM \_ SETRANGE 訊息

在 IP 位址控制項中，設定指定之欄位的有效範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的欄位索引，將套用此範圍。

</dd> <dt>

*lParam* 
</dt> <dd>

**文字** 值，包含低序位位元組中範圍的下限，以及高序位位元組的上限。 這兩個值都包含在內。 [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)宏也可以用來建立範圍。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

如果使用者在此範圍外的欄位中輸入值，控制項將會傳送具有所輸入值的 [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) 通知。 如果值在傳送通知之後仍超出範圍，控制項將嘗試將輸入的值變更為最接近的範圍限制。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





