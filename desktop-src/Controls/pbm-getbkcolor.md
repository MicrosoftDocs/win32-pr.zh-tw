---
title: 'PBM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 取得進度列的背景色彩。
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843932"
---
# <a name="pbm_getbkcolor-message"></a>PBM \_ GETBKCOLOR 訊息

取得進度列的背景色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回進度列的背景色彩。

## <a name="remarks"></a>備註

這是 [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md) 訊息所設定的色彩。 預設值是 CLR \_ default，定義于 commctrl 中。

此函式只會影響傳統模式，而不會影響任何視覺效果樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





