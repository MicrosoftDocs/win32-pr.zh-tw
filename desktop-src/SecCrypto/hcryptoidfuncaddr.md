---
description: 代表物件識別碼的控制碼， (OID) 可安裝的函式。
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: 'HCRYPTOIDFUNCADDR (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb36bdd98332842d89533c9c34a880aecdc8555cd64bb03888c0bd146cea3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006546"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

**HCRYPTOIDFUNCADDR** 資料類型代表 [*物件識別碼*](../secgloss/o-gly.md)的控制碼， (OID) 可安裝的函式。 [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)、 [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)和 [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)函數以及 [**CERT \_ STORE \_ >prov \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info)結構都會使用此資料類型。


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
