---
description: HCRYPTKEY 資料類型是用來代表密碼編譯金鑰的控制碼。
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: 'HCRYPTKEY (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985031"
---
# <a name="hcryptkey"></a>HCRYPTKEY

**HCRYPTKEY** 資料類型是用來代表 [*密碼編譯金鑰*](../secgloss/c-gly.md)的控制碼。 這些控制碼可用來向 CSP 模組指出特定作業中所使用的金鑰。 CSP 模組不允許直接存取金鑰值。 相反地，使用者會透過金鑰控制碼使用索引鍵值來執行函數。


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
