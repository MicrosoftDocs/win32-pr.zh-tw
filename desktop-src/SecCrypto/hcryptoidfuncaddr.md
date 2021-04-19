---
description: 代表物件識別碼的控制碼， (OID) 可安裝的函式。
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: 'HCRYPTOIDFUNCADDR (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984648"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

**HCRYPTOIDFUNCADDR** 資料類型代表 [*物件識別碼*](../secgloss/o-gly.md)的控制碼， (OID) 可安裝的函式。 [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)、 [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)和 [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)函數以及 [**CERT \_ STORE \_ >prov \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info)結構都會使用此資料類型。


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
