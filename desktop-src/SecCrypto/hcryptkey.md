---
description: HCRYPTKEY 資料類型是用來代表密碼編譯金鑰的控制碼。
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: 'HCRYPTKEY (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78d50f7fb005d877f6520172631b4546b8d498c415de58502defd26831c65fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006436"
---
# <a name="hcryptkey"></a>HCRYPTKEY

**HCRYPTKEY** 資料類型是用來代表 [*密碼編譯金鑰*](../secgloss/c-gly.md)的控制碼。 這些控制碼可用來向 CSP 模組指出特定作業中所使用的金鑰。 CSP 模組不允許直接存取金鑰值。 相反地，使用者會透過金鑰控制碼使用索引鍵值來執行函數。


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
