---
description: HCRYPTHASH 資料類型是用來表示雜湊物件的控制碼。
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: 'HCRYPTHASH (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b2d20d7aeb46adda162f8d5ec380143164690bad8ee88139f9653753f1e290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006556"
---
# <a name="hcrypthash"></a>HCRYPTHASH

**HCRYPTHASH** 資料類型是用來表示 [*雜湊物件*](../secgloss/h-gly.md)的控制碼。 這些控點會向 CSP 模組指出特定作業中使用的雜湊。 CSP 模組不允許直接操作雜湊值。 相反地，使用者會透過雜湊控制碼來操控雜湊值。


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
