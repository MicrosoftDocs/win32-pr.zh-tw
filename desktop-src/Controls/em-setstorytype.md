---
title: 'EM_SETSTORYTYPE 訊息 (Richedit .h) '
description: 設定案例類型。
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e09c62c50441857aac6f4018800de7a145081d64de49cdf7e9ca673a5370db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062878"
---
# <a name="em_setstorytype-message"></a>EM \_ SETSTORYTYPE 訊息

設定案例類型。


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

故事索引。

</dd> <dt>

*lParam* 
</dt> <dd>

新的案例類型。 如需故事類型的清單，請參閱 [**EM \_ GETSTORYTYPE**](em-getstorytype.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

已設定的案例類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





