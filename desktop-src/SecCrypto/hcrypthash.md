---
description: HCRYPTHASH 資料類型是用來表示雜湊物件的控制碼。
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: 'HCRYPTHASH (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851296"
---
# <a name="hcrypthash"></a>HCRYPTHASH

**HCRYPTHASH** 資料類型是用來表示 [*雜湊物件*](../secgloss/h-gly.md)的控制碼。 這些控點會向 CSP 模組指出特定作業中使用的雜湊。 CSP 模組不允許直接操作雜湊值。 相反地，使用者會透過雜湊控制碼來操控雜湊值。


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
