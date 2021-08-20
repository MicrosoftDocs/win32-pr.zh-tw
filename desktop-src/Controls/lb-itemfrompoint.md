---
title: 'LB_ITEMFROMPOINT 訊息 (Winuser .h) '
description: 取得最接近清單方塊中指定點之專案的以零為基底的索引。
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddddd58780cb4b140501c567d699373cb1fa03cbf212332bea71611a4add3788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575928"
---
# <a name="lb_itemfrompoint-message"></a>LB \_ ITEMFROMPOINT 訊息

取得最接近清單方塊中指定點之專案的以零為基底的索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定某個點的 x 座標（相對於清單方塊的工作區左上角）。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定點的 y 座標（相對於清單方塊的工作區左上角）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值包含 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))中最接近專案的索引。 如果指定的點位於清單方塊的工作區中，則 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 為零，如果位於工作區之外，則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

