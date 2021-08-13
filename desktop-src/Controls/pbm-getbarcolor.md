---
title: 'PBM_GETBARCOLOR 訊息 (Commctrl .h) '
description: 取得進度列的色彩。
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312438"
---
# <a name="pbm_getbarcolor-message"></a>PBM \_ GETBARCOLOR 訊息

取得進度列的色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回進度列的色彩。

## <a name="remarks"></a>備註

這是 [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) 訊息所設定的色彩。 預設值是 CLR \_ default，定義于 commctrl 中。

此函式只會影響傳統模式，而不會影響任何視覺效果樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





