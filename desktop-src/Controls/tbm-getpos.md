---
title: 'TBM_GETPOS 訊息 (Commctrl .h) '
description: 抓取捲軸中滑杆的目前邏輯位置。 邏輯位置是在最小至最大滑杆位置的 [最大值] 範圍內的整數值。
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ed3b8afed7b96e657984a437ff54b1099f196b8dc3d0035468835152b5a841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078082"
---
# <a name="tbm_getpos-message"></a>TBM \_ GETPOS 訊息

抓取捲軸中滑杆的目前邏輯位置。 邏輯位置是在最小至最大滑杆位置的 [最大值] 範圍內的整數值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回32位值，這個值會指定目前的捲軸滑杆的邏輯位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TBM \_ SETPOS**](tbm-setpos.md)
</dt> </dl>

 

 





