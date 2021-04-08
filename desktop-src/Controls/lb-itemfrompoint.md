---
title: 'LB_ITEMFROMPOINT 訊息 (Winuser .h) '
description: 取得最接近清單方塊中指定點之專案的以零為基底的索引。
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT message Windows 控制項
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
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686288"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

