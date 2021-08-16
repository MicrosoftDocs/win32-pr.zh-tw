---
title: 'EM_EXLINEFROMCHAR 訊息 (Richedit .h) '
description: 判斷哪一行在 rich edit 控制項中包含指定的字元。
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c41f5fbe540a4d765a48292d4ffd5b4af5849681dd1a82f4512b79348a6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915638"
---
# <a name="em_exlinefromchar-message"></a>EM \_ EXLINEFROMCHAR 訊息

判斷哪一行在 rich edit 控制項中包含指定的字元。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

以零為基底的字元索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這則訊息會傳回以零為基底的索引行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





