---
title: 'EM_SETUIANAME 訊息 (Richedit .h) '
description: 針對消費者介面自動化 (UIA) 設定 rich edit 控制項的名稱。
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- EM_SETUIANAME message Windows 控制項
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
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934542"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





