---
description: 表示一組物件識別碼的控制碼， (OID) 可安裝的函式。
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: 'HCRYPTOIDFUNCSET (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3926b78359450b780a9952aeae9d957157ebb56973a7f428824b07cbb43e9a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006466"
---
# <a name="hcryptoidfuncset"></a>HCRYPTOIDFUNCSET

**HCRYPTOIDFUNCSET** 資料類型代表一組 [*物件識別碼*](../secgloss/o-gly.md)的控制碼， (OID) 可安裝的函式。 [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)、 [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)、 [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)和 [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)函數會使用此資料類型。


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
