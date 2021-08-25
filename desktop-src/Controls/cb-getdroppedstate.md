---
title: 'CB_GETDROPPEDSTATE 訊息 (Winuser .h) '
description: 決定下拉式方塊的清單方塊是否已中斷。
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1674406b4dc5a4dd5e7985ba497fce8ef93e7c3480c050db0420b541c6d2ab6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089248"
---
# <a name="cb_getdroppedstate-message"></a>CB \_ GETDROPPEDSTATE 訊息

決定下拉式方塊的清單方塊是否已中斷。

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

如果清單方塊是可見的，則傳回值為 **TRUE**;否則為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)
</dt> </dl>

 

 





