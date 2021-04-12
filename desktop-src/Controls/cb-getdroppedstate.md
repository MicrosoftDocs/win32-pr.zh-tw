---
title: 'CB_GETDROPPEDSTATE 訊息 (Winuser .h) '
description: 決定下拉式方塊的清單方塊是否已中斷。
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE message Windows 控制項
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
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025510"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)
</dt> </dl>

 

 





