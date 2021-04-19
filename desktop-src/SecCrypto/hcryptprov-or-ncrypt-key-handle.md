---
description: 用來作為 CryptoAPI 密碼編譯服務提供者的控制碼， (CSP) 或 CNG CSP。
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: 'HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988929"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>HCRYPTPROV \_ 或 \_ NCRYPT \_ 金鑰 \_ 控制碼

**HCRYPTPROV \_ 或 NCRYPT \_ 索引 \_ 鍵 \_ 控制碼** 資料類型是用來作為 CryptoAPI [*密碼編譯服務提供者*](../secgloss/c-gly.md)的控制碼， (CSP) 或 CNG csp。 這個控制碼必須是使用 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)函式所建立的 [**HCRYPTPROV**](hcryptprov.md)控制碼，或使用 [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey)函式建立的 **NCRYPT 索引 \_ 鍵 \_ 控制碼** 控制碼。 新的應用程式應該一律將 **NCRYPT \_ 金鑰 \_ 控制碼** 控制碼傳入 CNG CSP。


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



 

 
