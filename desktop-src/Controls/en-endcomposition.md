---
title: 'EN_ENDCOMPOSITION (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗，指出使用者已輸入新資料，或在使用 IME 或文字服務架構時完成輸入資料。
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464424"
---
# <a name="en_endcomposition-notification-code"></a>EN \_ ENDCOMPOSITION 通知碼

通知 rich edit 控制項父視窗，指出使用者已輸入新資料，或在使用 IME 或 [文字服務架構](/windows/desktop/TSF/text-services-framework)時完成輸入資料。


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify)結構，可接收有關結束組合條件的資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

