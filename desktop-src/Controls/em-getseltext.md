---
title: 'EM_GETSELTEXT 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項中目前選取的文字。
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019496"
---
# <a name="em_getseltext-message"></a>EM \_ GETSELTEXT 訊息

抓取 rich edit 控制項中目前選取的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

接收選取文字之緩衝區的指標。 呼叫應用程式必須確定緩衝區夠大，足以容納選取的文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回復制的字元數，而不包含終止的 null 字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





