---
title: 'TBM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取指派給的提示（如果有的話）之工具提示控制項的控制碼。
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078062"
---
# <a name="tbm_gettooltips-message"></a>TBM \_ GETTOOLTIPS 訊息

抓取指派給的提示（如果有的話）之工具提示控制項的控制碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指派給的提示之工具提示控制項的控制碼，如果工具提示不在使用中，則傳回 **Null** 。 如果 [執行程式] 控制項未使用 [ [**tb] \_ 工具提示**](trackbar-control-styles.md) 樣式，則傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





