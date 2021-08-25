---
title: 'EM_EXSETSEL 訊息 (Richedit .h) '
description: 在 Microsoft Rich Edit 控制項中，選取 (COM) 物件的字元或元件物件模型範圍。
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e35840e404f295b7d3ed6ddd5dddf4c77076c236eb3260f6f719b152cef207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915648"
---
# <a name="em_exsetsel-message"></a>EM \_ EXSETSEL 訊息

在 Microsoft Rich Edit 控制項中，選取 (COM) 物件的字元或元件物件模型範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

指定選取範圍的 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是實際設定的選取專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





