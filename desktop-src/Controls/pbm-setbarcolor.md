---
title: 'PBM_SETBARCOLOR 訊息 (Commctrl .h) '
description: 在進度列控制項中設定進度指標列的色彩。
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babff5ad74d943d64f5ad61354447498e91e1325c99c82b32183fbc62eabafdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830199"
---
# <a name="pbm_setbarcolor-message"></a>PBM \_ SETBARCOLOR 訊息

在進度列控制項中設定進度指標列的色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF** 值，指定新的進度指標列色彩。 指定 CLR \_ 預設值會使進度列使用其預設的進度指示器列色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回上一個進度指標列色彩，或 \_ 如果進度指示器列色彩是預設色彩，則為 CLR 預設值。

## <a name="remarks"></a>備註

啟用視覺化樣式時，此訊息不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





