---
title: 'LB_GETCOUNT 訊息 (Winuser .h) '
description: 取得清單方塊中的專案數。
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- LB_GETCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466805"
---
# <a name="lb_getcount-message"></a>LB \_ GETCOUNT 訊息

取得清單方塊中的專案數。

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

傳回值是清單方塊中的專案數，如果發生錯誤，則為 LB \_ ERR。

## <a name="remarks"></a>備註

傳回的計數大於最後一個專案的索引值， (索引是以零為基底的) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETCOUNT**](lb-setcount.md)
</dt> </dl>

 

 





