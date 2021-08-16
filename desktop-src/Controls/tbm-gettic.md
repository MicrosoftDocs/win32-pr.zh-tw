---
title: 'TBM_GETTIC 訊息 (Commctrl .h) '
description: 捕獲刻度中刻度標記的邏輯位置。 邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7cdd2c28f9add787c41da3cde3fabc3a5dff33812b3dd9c07a26a603d3a79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829602"
---
# <a name="tbm_gettic-message"></a>TBM \_ GETTIC 訊息

捕獲刻度中刻度標記的邏輯位置。 邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，識別刻度。 有效索引的範圍介於0到2之間，小於 [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) 訊息所傳回的滴答計數。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定刻度的邏輯位置; 如果 *wParam* 未指定有效的索引，則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





