---
title: 'EM_SETUIANAME 訊息 (Richedit .h) '
description: 針對消費者介面自動化 (UIA) 設定 rich edit 控制項的名稱。
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603d59b7bf246ee8ed7987d42399281ac1b0520ef27e206f2f8eeddf8f363d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412323"
---
# <a name="em_setuianame-message"></a>EM \_ SETUIANAME 訊息

針對消費者介面自動化 (UIA) 設定 rich edit 控制項的名稱。


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束之名稱字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功設定 UIA 的名稱，則為 TRUE，否則為 FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





